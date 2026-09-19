# Physics API

The physics API is a small rigid-body system owned by `Scene.physics()`.
`PhysicsWorld` manages bodies, gravity, fixed substeps, broad-phase overlap,
contact resolution, and the contact list from the last step.

## Main types

- `PhysicsWorld` — world settings, body creation/removal, stepping, bodies, and
  contacts.
- `PhysicsBody` — position, velocity, mass, gravity, forces, impulses, jumping,
  capsule dimensions, step height, and kinematic state.
- `CollisionShape` — box, sphere, capsule, convex hull, and triangle mesh data.
- `CollisionLod` — automatic or explicit mesh collider selection.
- `PhysicsContact` — bodies, point, normal, and penetration from the last step.

## Ownership and update rules

Scenes own their physics world and the engine calls `step` automatically. A
body linked to a `GameObject` synchronizes its simulated position back to that
object. Do not step an engine-managed world from `GameLogic.update`.

## Solver limitations

The solver uses semi-implicit Euler integration, maximum 1/60-second substeps,
normal impulses, positional correction, and oriented-box contacts for rotated
boxes. It does not currently simulate angular velocity, angular impulses, or
tangential friction impulses. `setFriction` is retained as material metadata.
