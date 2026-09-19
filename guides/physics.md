# Physics

The engine includes a lightweight rigid-body physics API with real gravity, velocity integration, collision shapes, static and dynamic bodies, impulse response, positional correction, and walkable ramps. It is dependency-free and intentionally small enough to extend from game code.

## Core model

Every `Scene` owns a `PhysicsWorld`. The engine advances the active scene's world automatically once per simulation frame. Do not call `step` from `GameLogic.update` unless you are running a separate, manually controlled world.

```java
private static final float BODY_MASS = 1f;
private static final float BODY_RADIUS = 0.35f;
private static final float BODY_HEIGHT = 1.8f;
private static final float STEP_HEIGHT = 0.35f;

PhysicsWorld physics = scene.physics()
        .setGravity(0f, -9.81f, 0f);
PhysicsBody player = physics.addBody()
        .setMass(BODY_MASS)
        .setShape(CollisionShape.capsule(BODY_RADIUS, BODY_HEIGHT))
        .setStepHeight(STEP_HEIGHT)
        .setPosition(0f, BODY_HEIGHT * 0.5f, 8f);

if (jumpPressed) {
    player.jump();
}
player.setHorizontalVelocity(horizontalX, horizontalZ);
```

The engine uses body-center positions. A standing capsule with height `1.8` and ground at `0` therefore starts at Y `0.9`. Static bodies use mass `0`.

Character bodies can set a small `stepHeight` for low obstacles. This is a local character-controller convenience, not baked-in terrain: larger obstacles still require normal collision response or a jump.

## Collision shapes and LOD

Collision geometry is independent from render geometry. Use a simple manual primitive when possible, or derive a shape from any render mesh:

```java
GameObject statue = scene.getObject("statue");
PhysicsBody collider = scene.physics().addStaticCollider(
        statue,
        CollisionLod.AUTO
);

PhysicsBody crate = scene.physics().addDynamicBody(
        scene.getObject("crate"),
        CollisionLod.BOX,
        4f
);
```

`AUTO` chooses a triangle mesh for small meshes and a convex-hull representation for larger meshes. `BOX`, `SPHERE`, `CAPSULE`, `CONVEX_HULL`, and `TRIANGLE_MESH` can be selected manually. The solver uses conservative AABB broad-phase checks, then uses oriented-box contacts for rotated box colliders so thin slopes do not become tall invisible walls.

## Ramps and multiple floors

Ramps are ordinary render objects with ordinary static collision bodies. There is no special height function and no position snapping. Build the ramp mesh, register it as a static collider, and let gravity and collision resolution determine the body's motion.

```java
GameObject ramp = scene.createObject("ramp", rampMesh, rampMaterial)
        .setPosition(0f, 1.5f, -6f)
        .setRotationDeg(18f, 0f, 0f);
scene.physics().addStaticCollider(ramp, CollisionLod.BOX);
```

Because the slope is just a rotated object, its collision follows the same transformed geometry. There is no ramp-specific height interpolation or snapping.

## Moving parts

Use a kinematic body for a platform or lift that should move on an authored path while remaining collidable:

```java
PhysicsBody lift = scene.physics()
        .addStaticCollider(platform, CollisionLod.BOX)
        .setMass(1f)
        .setKinematic(true);

lift.setPosition(pathX, pathY, pathZ);
```

Kinematic bodies are not integrated by gravity and cannot be pushed by dynamic bodies. Move their position from game code; the solver still includes them in collision detection.

## Assembling and disassembling physics

`physicsAssemble` turns a render object into a gravity-driven dynamic body.
The default overload calculates mass from the collision shape volume using a
density of `1`. Pass a different density for heavier or lighter materials:

```java
PhysicsBody crateBody = scene.physics()
        .physicsAssemble(crate, CollisionLod.BOX, 2.5f)
        .setRestitution(0.25f)
        .setFriction(0.75f);
```

Use the mass override when the physical weight should not follow the visual
size:

```java
PhysicsBody projectileBody = scene.physics()
        .physicsAssemble(projectile, CollisionLod.SPHERE, 1f, 4f);
```

Forces accumulate until the next physics step and therefore model continuous
pushes. An impulse changes velocity immediately and is useful for launches:

```java
crateBody.applyForce(0f, 35f, 0f);
projectileBody.applyImpulse(0f, 8f, -12f);
```

Remove a body from simulation with `physicsDisassemble`. The render object is
left in the scene and is no longer moved by physics:

```java
scene.physics().physicsDisassemble(crateBody);
```

## Gravity and forces

Gravity is a world vector and can be changed per scene. Bodies can scale it or receive one-frame forces:

```java
physics.setGravity(0f, -9.81f, 0f);
body.setGravityScale(0.5f);
body.addForce(0f, 120f, 0f);
```

The solver uses semi-implicit Euler integration with fixed maximum substeps, then resolves contacts using restitution, friction configuration, and positional correction. Dynamic bodies use a positive mass; mass `0` makes a body static.

## Frame-rate safety

The world subdivides large frame deltas into 1/60-second maximum steps. Keep movement speeds, masses, and gravity in world units and seconds.

## Common mistakes

- Treating `position()` as feet position; rigid bodies use their center.
- Registering a render object but forgetting to register its physics body.
- Using `TRIANGLE_MESH` for every object instead of selecting a cheaper LOD for dynamic bodies.
- Creating a visible ramp without adding a matching static collider.
- Adding a dynamic body with mass `0`; that makes it static by design.
