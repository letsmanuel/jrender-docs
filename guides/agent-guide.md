# Agent contribution guide

Read the relevant class and function pages before editing. Search call sites before adding abstractions. Preserve lifecycle ownership, parent-relative GUI layout, native-thread assumptions, fluent return types, and error visibility. Update documentation whenever public behavior changes. Run the smallest relevant Gradle validation, then the full build for public API or packaging changes.
