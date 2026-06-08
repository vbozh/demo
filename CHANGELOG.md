# Changelog

## Sprint 261.681 — June 2026

### Features

- **Persistent permission mode selection** — Air now remembers the last selected permission mode across sessions. New chats no longer always revert to the default mode. ([AIR-3889](https://youtrack.jetbrains.com/issue/AIR-3889))

### Improvements

- **Junie model selector redesign** — The model selector UI in Junie has been updated to match the latest design spec, improving clarity and usability when switching between AI models. ([AIR-4007](https://youtrack.jetbrains.com/issue/AIR-4007))
- **ACP end-turn git revision info** — The ACP agent now returns the git starting revision in its end-turn payload, enabling clients to identify exactly which changes the agent made during a session. ([AIR-5426](https://youtrack.jetbrains.com/issue/AIR-5426))

### Fixes

- **UI freeze on project open** — Fixed an issue where Air's UI would freeze immediately after opening a project. ([AIR-5566](https://youtrack.jetbrains.com/issue/AIR-5566))
- **[Windows] Update failure for installer version** — Fixed Air updates not working when the app was installed via the standalone installer (as opposed to Toolbox). ([AIR-5406](https://youtrack.jetbrains.com/issue/AIR-5406))
- **Junie 401 Unauthorized error** — Resolved an authentication error that surfaced mid-session with no actionable message. Junie now handles and surfaces token expiry more clearly. ([AIR-4182](https://youtrack.jetbrains.com/issue/AIR-4182))
- **Gemini 3.0 Pro compatibility in Junie** — Junie no longer incorrectly reports Gemini 3.0 Pro as unsupported. ([AIR-3916](https://youtrack.jetbrains.com/issue/AIR-3916))
- **Missing icons in plan widget** — Fixed intermittent missing expand/collapse and action icons in the plan widget. ([AIR-4900](https://youtrack.jetbrains.com/issue/AIR-4900))
- **Cannot reopen projects from Workspaces menu** — Fixed an issue where certain projects could not be reopened from the Workspaces menu after being closed, requiring a force-quit to recover. ([AIR-4313](https://youtrack.jetbrains.com/issue/AIR-4313))
- **Agent stuck after internal Codex error** — Air can now recover from internal Codex errors without requiring a terminal workaround or app restart. ([AIR-4311](https://youtrack.jetbrains.com/issue/AIR-4311))
- **[macOS] Drag and drop with spaces in file path** — Fixed drag-and-drop failures caused by macOS clipboard URLs containing unencoded spaces. ([AIR-5331](https://youtrack.jetbrains.com/issue/AIR-5331))
- **Junie permission widget shows tool call ID** — The permission request widget in Junie now displays the human-readable tool name instead of the raw tool call ID. ([AIR-3950](https://youtrack.jetbrains.com/issue/AIR-3950))

---

*Produced by Air Automation. Name: Generate Release Notes / Run: https://air.stgn.jetbrains.cloud/org/05cf1a7f-6ab5-713b-abd3-29d0c8a05e2d/automations/700dc751-f867-4758-aa14-92fd8704e23d?run=3cb9bf75-a202-4169-bfb1-f687f11a2281*
