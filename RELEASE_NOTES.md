## Release Notes

### Features
* **Plugin API & Virtual Lines**: Added an API for background processes and a system for virtual lines to allow plugin-driven persistent annotations. This enabled a new Git blame plugin with history navigation.
* **Editor**: Added a resizable file explorer, search options (case-sensitive, whole word, regex), and confirmation prompts for closing modified buffers and quitting.
* **Tooling**: The `bump-version` script was rewritten in Python and now includes release note generation.

### Bug Fixes
* **Display/Scrolling**: Fixed issues with mouse scroll, horizontal scrolling, viewport reset, view transform header visibility, and cursor visibility with ANSI codes. Corrected line number display for empty buffers/source lines.
* **Editing/Search**: Corrected auto-dedent behavior, fixed large file save corruption, ensured search highlights update, and stabilized suggestions/command palette widths.
* **Stability**: Fixed tab flicker, improved auto-revert (with debounce and scroll preservation), and temporarily ignored several unstable tests to stabilize CI.

### Internal Changes
* **Architecture**: Source code was reorganized into a layered architecture (`model`, `app`, `view`, etc.). Documentation was added for Buffer/View state separation and the Layout Layer.
* **CI/CD**: Switched to `cargo-nextest` for testing, added Linux platform support, and updated GitHub Actions dependencies.
