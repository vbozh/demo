# Changelog — Sprint 262.43 (June 2026)

> **43 completed issues** · Sourced from YouTrack AIR project (fix version: 262.43 + sprint: {262.43})

---

## Features

- **Open in IDE (IJ-family) for local project & changes** ([AIR-3687](https://youtrack.jetbrains.com/issue/AIR-3687))  
  Enables opening a local project or its pending changes directly in JetBrains IDE family products.

- **Windows support** ([AIR-4132](https://youtrack.jetbrains.com/issue/AIR-4132))  
  Full Windows platform support delivered this sprint.

- **Linux Wayland: implement IME in editor** ([AIR-5610](https://youtrack.jetbrains.com/issue/AIR-5610))  
  Input Method Editor (IME) support for CJK and other complex scripts on Linux Wayland.

- **Linux X11: implement IME in editor** ([AIR-5611](https://youtrack.jetbrains.com/issue/AIR-5611))  
  Input Method Editor (IME) support for CJK and other complex scripts on Linux X11.

---

## Improvements

- **[Windows] Native-style buttons in update dialog** ([AIR-5755](https://youtrack.jetbrains.com/issue/AIR-5755))  
  Update available dialog now uses Windows-native button styling.

- **[Windows] Native caption buttons drawn with Compose** ([AIR-5600](https://youtrack.jetbrains.com/issue/AIR-5600))  
  Replaced KDT-drawn caption buttons with Compose-rendered native Windows caption buttons.

- **[Windows] Font rendering quality in editor** ([AIR-4755](https://youtrack.jetbrains.com/issue/AIR-4755))  
  Added subpixel antialiasing, grid fitting, and hinting for sharper text rendering on Windows.

- **[Windows] Air icon alignment on main toolbar** ([AIR-5608](https://youtrack.jetbrains.com/issue/AIR-5608))  
  Corrected icon alignment on the main toolbar for Windows.

- **Update Slash menu** ([AIR-5208](https://youtrack.jetbrains.com/issue/AIR-5208))  
  Refreshed Slash menu design and content.

- **Terminal commands shown as code snippets in archived tasks** ([AIR-3335](https://youtrack.jetbrains.com/issue/AIR-3335))  
  Terminal commands in archived task history are now rendered as formatted code snippets.

---

## Fixes

### Critical / Show-stoppers

- **Tasks and changes not loading after 262.34 update** ([AIR-5640](https://youtrack.jetbrains.com/issue/AIR-5640))  
  Fixed a show-stopping regression where tasks and changes panel failed to load entirely.

- **Chat messages invisible until task is stopped** ([AIR-5583](https://youtrack.jetbrains.com/issue/AIR-5583))  
  Chat messages are now visible in real time without requiring the task to stop first.

- **Folder mentioned in task copied into itself on Docker task run** ([AIR-5670](https://youtrack.jetbrains.com/issue/AIR-5670))  
  Prevented a critical data-corruption issue where a referenced folder was recursively copied into itself.

### Startup & Updates

- **Air cannot start after Toolbox update** ([AIR-5645](https://youtrack.jetbrains.com/issue/AIR-5645)) ✨ new  
  Fixed a `NullPointerException` in `RenderLoop.stopAndJoin` that prevented Air from starting when the render loop was not fully initialized during a Toolbox-triggered version update.

### Performance

- **CPU hog in idle** ([AIR-5812](https://youtrack.jetbrains.com/issue/AIR-5812))  
  Resolved excessive CPU usage when the application was sitting idle.

- **Scrolling is very slow** ([AIR-5233](https://youtrack.jetbrains.com/issue/AIR-5233))  
  Scroll performance significantly improved across the application.

### Windows

- **Kotlin LSP does not work on Windows** ([AIR-5760](https://youtrack.jetbrains.com/issue/AIR-5760))  
  Fixed `CreateProcessW` failure that prevented the Kotlin language server from starting on Windows.

- **[Windows] Copy does not work** ([AIR-5558](https://youtrack.jetbrains.com/issue/AIR-5558))  
  Clipboard copy operations now work correctly on Windows.

- **[Windows] Terminal stops working when window is minimized** ([AIR-5316](https://youtrack.jetbrains.com/issue/AIR-5316))  
  Terminal no longer freezes or becomes unresponsive after the window is minimized.

- **Can't run custom acp agent on Windows** ([AIR-5759](https://youtrack.jetbrains.com/issue/AIR-5759))  
  Fixed `%1 is not a valid Win32 application` error preventing custom agent execution on Windows.

- **Agent's final response sometimes missing from chat on Windows** ([AIR-5738](https://youtrack.jetbrains.com/issue/AIR-5738))  
  Ensured the final agent response is always appended to the chat history on Windows.

- **`window_get_screen_info` error when display device is not attached to desktop** ([AIR-5385](https://youtrack.jetbrains.com/issue/AIR-5385))  
  Handled the case where no display device is attached to the desktop, eliminating the crash.

### Linux

- **Arch KDE Wayland: resize stuck after drag** ([AIR-5571](https://youtrack.jetbrains.com/issue/AIR-5571))  
  Window resize no longer gets stuck after a drag operation on Arch Linux with KDE Wayland.

### Agent & Workspace

- **Invoking Review with Agent from active session deletes entire parent task** ([AIR-5570](https://youtrack.jetbrains.com/issue/AIR-5570))  
  Fixed destructive behavior that wiped the parent task when starting an agent review.

- **Agent launch blocked with "No Git Repository Found"** ([AIR-5565](https://youtrack.jetbrains.com/issue/AIR-5565))  
  Agent no longer fails to launch when the workspace path uses subst-mapped or symlinked drives.

- **Agent not starting when workspace was initially in "Safe Mode"** ([AIR-5525](https://youtrack.jetbrains.com/issue/AIR-5525))  
  Workspaces that started in Safe Mode can now successfully launch agents.

- **Uncommitted changes lost on "Implement in Worktree"** ([AIR-5484](https://youtrack.jetbrains.com/issue/AIR-5484))  
  Uncommitted changes are now correctly carried over when implementing a plan in a Worktree.

- **Uncommitted changes lost on "Implement in Docker"** ([AIR-5538](https://youtrack.jetbrains.com/issue/AIR-5538))  
  Uncommitted changes are now correctly carried over when implementing a plan in Docker.

- **Resume Docker task does not work correctly due to race condition** ([AIR-4270](https://youtrack.jetbrains.com/issue/AIR-4270))  
  Fixed a race condition that caused Docker task resume to fail intermittently.

- **Failed to parse Claude System "commands_changed"** ([AIR-5857](https://youtrack.jetbrains.com/issue/AIR-5857))  
  Agent no longer crashes when Claude emits an unrecognized `commands_changed` system event.

- **Gemini asks permission for AskUserQuestion tool** ([AIR-4606](https://youtrack.jetbrains.com/issue/AIR-4606)) ✨ new  
  Gemini-based agents no longer incorrectly prompt the user for permission before invoking the `AskUserQuestion` tool, which should not require explicit approval.

### Chat & UI

- **Alignment of messages broken in chat** ([AIR-5791](https://youtrack.jetbrains.com/issue/AIR-5791))  
  Chat message layout alignment is now consistent.

- **Table rendering and scroll in chat output** ([AIR-5045](https://youtrack.jetbrains.com/issue/AIR-5045))  
  Fixed table UI display and scroll behavior in agent chat output.

- **Junie approval view shows no content** ([AIR-4794](https://youtrack.jetbrains.com/issue/AIR-4794))  
  The Junie approval dialog now renders its content correctly.

- **Thinking level switcher missing from UI** ([AIR-5606](https://youtrack.jetbrains.com/issue/AIR-5606))  
  Restored the thinking level switcher control in the UI.

- **Application menu closes unexpectedly when moving mouse between options** ([AIR-5639](https://youtrack.jetbrains.com/issue/AIR-5639))  
  Application menu now stays open while moving the cursor between menu items.

- **Tooltip flicker on hover** ([AIR-5008](https://youtrack.jetbrains.com/issue/AIR-5008))  
  Eliminated tooltip flickering when hovering over elements that trigger multiple tooltips.

### Editor & Tools

- **Can't open files linked in agent markdown plans** ([AIR-5449](https://youtrack.jetbrains.com/issue/AIR-5449))  
  File links in agent-generated markdown plans are now clickable and open correctly.

- **Junie cannot use `mcp__Air__add_comment` tool in agent review** ([AIR-4097](https://youtrack.jetbrains.com/issue/AIR-4097))  
  Fixed MCP tool availability so Junie can properly post review comments.

- **Commits list not shown after Worktree plan implementation** ([AIR-5240](https://youtrack.jetbrains.com/issue/AIR-5240))  
  The Changes tool now correctly shows the commit list after a Worktree-based plan is implemented.

- **Commit message input missing in Diff view** ([AIR-5101](https://youtrack.jetbrains.com/issue/AIR-5101))  
  Commit message input field is no longer missing from the Changes tool diff view.

- **Edit and Revert buttons disappear on Diff view resize** ([AIR-5319](https://youtrack.jetbrains.com/issue/AIR-5319))  
  Edit and Revert buttons remain visible in the Diff view file list when the panel is resized.

### Authentication

- **Unable to login using "Login with JetBrains"** ([AIR-5465](https://youtrack.jetbrains.com/issue/AIR-5465))  
  Resolved an authentication failure affecting the JetBrains SSO login flow.

---

*Produced by Air Automation. Name: Generate Release Notes / Run: https://air.stgn.jetbrains.cloud/org/05cf1a7f-6ab5-713b-abd3-29d0c8a05e2d/automations/700dc751-f867-4758-aa14-92fd8704e23d?run=0a07fdf2-1d75-4053-8929-afc98c5264b1*
