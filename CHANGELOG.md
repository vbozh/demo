# Changelog

## Sprint 261.681 — May–June 2026

### Features

- **Multi-skill references in chat** ([AIR-7683096](https://youtrack.jetbrains.com/issue/AIR-7683096))
  You can now mention multiple skills in a single chat input, making it easier to combine capabilities without separate invocations.

- **Google Gemini 3.5 Flash support** ([AIR-7751816](https://youtrack.jetbrains.com/issue/AIR-7751816))
  Google Gemini 3.5 Flash is now available as a model option in Air.

- **Persistent permission mode selection** ([AIR-7418554](https://youtrack.jetbrains.com/issue/AIR-7418554))
  Air now remembers your last selected permission mode across sessions. New chats no longer reset to the default every time.

### Improvements

- **Context window display for active tasks** ([AIR-7348780](https://youtrack.jetbrains.com/issue/AIR-7348780))
  The UI now shows context window usage information for the currently running agent task, giving better visibility into model limits.

- **Junie model selector UI refresh** ([AIR-7438810](https://youtrack.jetbrains.com/issue/AIR-7438810))
  Junie's model selector has been updated to match the latest design spec.

- **Automated air-workspace image upload to S3** ([AIR-7663009](https://youtrack.jetbrains.com/issue/AIR-7663009))
  The air-workspace Docker image is now automatically uploaded to S3 after each build, removing a manual step from the Agent Spawner update workflow.

### Fixes

- **Cmd+Shift+P and Cmd+Shift+O shortcuts not working** ([AIR-7708897](https://youtrack.jetbrains.com/issue/AIR-7708897))
  Keyboard shortcuts that were registered but non-functional have been repaired. Cmd+P, Cmd+Shift+P, and related bindings now behave consistently.

- **Drag-and-drop broken for file paths with spaces on macOS** ([AIR-7739668](https://youtrack.jetbrains.com/issue/AIR-7739668))
  macOS clipboard URLs containing spaces were passed unencoded, causing drag-and-drop to fail. Spaces in paths are now correctly percent-encoded.

- **Docker tasks failing due to missing `unzip`** ([AIR-7746030](https://youtrack.jetbrains.com/issue/AIR-7746030))
  Running Docker-based agent tasks was blocked by a missing `unzip` dependency in the container. The dependency is now included.

- **Incorrect documentation link in Settings menu** ([AIR-7728668](https://youtrack.jetbrains.com/issue/AIR-7728668))
  The link to documentation from the Settings menu now correctly points to `jetbrains.com/help/air/getting-started.html`.

- **[Windows] Application fails to create a window on startup** ([AIR-7725634](https://youtrack.jetbrains.com/issue/AIR-7725634))
  A crash on Windows startup caused by a NUL byte in a display device name string has been resolved.

- **[Windows] Air opens a second window on local task creation** ([AIR-7725148](https://youtrack.jetbrains.com/issue/AIR-7725148))
  Creating a local task was incorrectly opening a new window instead of reusing the existing one.

- **Agent skips files when one pathspec is missing during `git add`** ([AIR-7715853](https://youtrack.jetbrains.com/issue/AIR-7715853))
  If a file in the staged set was missing (e.g., a deleted `__pycache__` entry), the entire `git add` command failed. The agent now handles partial pathspecs gracefully.

- **[Windows] Blank window after minimizing — ClassCastException** ([AIR-7712655](https://youtrack.jetbrains.com/issue/AIR-7712655))
  Restoring Air from a minimized state on Windows sometimes produced a blank window due to a shape casting error (`Outline$Rectangle` → `Outline$Rounded`). This has been fixed.

- **[Windows] Window content does not update after DPI change or monitor switch** ([AIR-7720096](https://youtrack.jetbrains.com/issue/AIR-7720096))
  Window content failed to relayout after a display resolution change, monitor reconnect, or RDP session on Windows. The layout now refreshes correctly.

- **[Windows] Window control buttons not visible** ([AIR-7701830](https://youtrack.jetbrains.com/issue/AIR-7701830))
  The minimize, maximize, and close buttons were invisible on Windows unless the frosted glass effect was enabled. They are now always visible regardless of transparency settings.

---

*Produced by Air Automation. Name: Generate Release Notes / Run: https://air.stgn.jetbrains.cloud/org/05cf1a7f-6ab5-713b-abd3-29d0c8a05e2d/automations/700dc751-f867-4758-aa14-92fd8704e23d?run=bec5fb3a-f98b-4246-9986-dcf718dde81f*
