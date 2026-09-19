# Agent contribution guide

Read the relevant class and function pages before editing. Search call sites
before adding abstractions. Preserve lifecycle ownership, parent-relative GUI
layout, native-thread assumptions, fluent return types, and error visibility.
Update documentation whenever public behavior changes.

## Documentation source of truth

Use `engine/src/main/java` and shader source as the behavioral source of truth.
Use `docs/overview` for workflows and `docs/api` for stable type references.
Root numbered markdown files are legacy generated output and are not canonical.

For every public API change:

1. Update the relevant overview guide.
2. Update the type README and signature pages when the generated API changes.
3. Add a runnable example with named values rather than unexplained literals.
4. Document ownership, threading, resource lifetime, coordinate conventions,
   defaults, and failure behavior.
5. Add at least one common mistake and one diagnostic technique.

Before publishing, compare public source types with `docs/SUMMARY.md`, verify
links, and run `gradlew build` after API or dependency changes.
