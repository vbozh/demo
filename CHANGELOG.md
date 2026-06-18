# Changelog

## Sprint 262.43 — June 2026

25 completed issues · 3 features · 3 improvements · 19 fixes

---

### Features

- **Open in IDE (IJ-family) for local project & changes** ([AIR-3687](https://youtrack.jetbrains.com/issue/AIR-3687))  
  Users can now open a local project or its pending changes directly in any IntelliJ-family IDE from within Air.

- **Linux Wayland: implement IME in editor** ([AIR-5610](https://youtrack.jetbrains.com/issue/AIR-5610))  
  Input Method Editor (IME) support is now available in the editor on Linux Wayland, enabling correct input for CJK and other complex-script languages.

- **Linux X11: implement IME in editor** ([AIR-5611](https://youtrack.jetbrains.com/issue/AIR-5611))  
  Input Method Editor (IME) support is now available in the editor on Linux X11, enabling correct input for CJK and other complex-script languages.

---

### Improvements

- **[Windows] Font rendering quality in editor** ([AIR-4755](https://youtrack.jetbrains.com/issue/AIR-4755))  
  Text rendering on Windows now applies subpixel antialiasing, grid fitting, and hinting, resulting in sharper and more legible editor text.

- **[Windows] Native caption buttons drawn with Compose** ([AIR-5600](https://youtrack.jetbrains.com/issue/AIR-5600))  
  The minimize, maximize, and close caption buttons on Windows are now rendered natively using Compose, replacing the previous KDT-based approach for better visual consistency.

- **Update Slash menu** ([AIR-5208](https://youtrack.jetbrains.com/issue/AIR-5208))  
  The slash command menu has been updated with revised entries and improved discoverability.

---

### Fixes

- **Tasks and changes not loading after 262.34 update** ([AIR-5640](https://youtrack.jetbrains.com/issue/AIR-5640)) *(show-stopper)*  
  Fixed a regression introduced in 262.34 that prevented tasks and the change list from loading on startup.

- **Chat messages invisible until task is stopped** ([AIR-5583](https://youtrack.jetbrains.com/issue/AIR-5583)) *(critical)*  
  Chat messages now render correctly while a task is running, without requiring the task to be stopped first.

- **Folder mentioned in a task is copied into itself on Docker task run** ([AIR-5670](https://youtrack.jetbrains.com/issue/AIR-5670)) *(critical)*  
  Fixed a critical bug where mentioning a project folder in a Docker task caused the folder to be recursively copied into itself at runtime.

- **Invoking Review with Agent from active session deletes entire parent task** ([AIR-5570](https://youtrack.jetbrains.com/issue/AIR-5570))  
  Fixed a data-loss bug where triggering an agent review from within an active session would delete the parent task instead of launching the review.

- **Kotlin LSP does not work on Windows** ([AIR-5760](https://youtrack.jetbrains.com/issue/AIR-5760))  
  Resolved a Windows-specific failure where the Kotlin Language Server could not start due to a `CreateProcessW` error.

- **Junie cannot use mcp__Air__add_comment tool in agent review** ([AIR-4097](https://youtrack.jetbrains.com/issue/AIR-4097))  
  Resolved a tool-access issue that prevented Junie from posting comments when acting as an agent reviewer, restoring its full review capability.

- **Can't open files linked in agent markdown plans** ([AIR-5449](https://youtrack.jetbrains.com/issue/AIR-5449))  
  File links embedded in agent-generated markdown plans can now be opened directly from the plan view.

- **Uncommitted changes lost on Implement in Docker agent** ([AIR-5538](https://youtrack.jetbrains.com/issue/AIR-5538))  
  Uncommitted local changes are now correctly carried over when running the Implement action inside a Docker agent.

- **Uncommitted changes lost on Implement in Worktree agent** ([AIR-5484](https://youtrack.jetbrains.com/issue/AIR-5484))  
  Uncommitted local changes are now correctly carried over when running the Implement action inside a Worktree agent.

- **Thinking level switcher missing from UI** ([AIR-5606](https://youtrack.jetbrains.com/issue/AIR-5606))  
  Restored the thinking level switcher control that had disappeared from the interface.

- **Commits list not shown after Worktree plan implementation** ([AIR-5240](https://youtrack.jetbrains.com/issue/AIR-5240))  
  The commits list is now displayed correctly in the Changes tool after a plan is implemented using the Worktree agent.

- **Commit message input missing in Diff view** ([AIR-5101](https://youtrack.jetbrains.com/issue/AIR-5101))  
  The commit message input field is now reliably visible in the Diff view.

- **Junie approval view shows no content** ([AIR-4794](https://youtrack.jetbrains.com/issue/AIR-4794))  
  Resolved an issue where the Junie approval view was blank instead of displaying the relevant content for review.

- **Application menu closes unexpectedly when moving mouse between options** ([AIR-5639](https://youtrack.jetbrains.com/issue/AIR-5639))  
  The application menu no longer dismisses itself when the cursor moves between menu items.

- **Scrolling is very slow** ([AIR-5233](https://youtrack.jetbrains.com/issue/AIR-5233))  
  Resolved a performance regression that caused noticeably sluggish scroll behaviour.

- **"window_get_screen_info" error when display device is not attached to desktop** ([AIR-5385](https://youtrack.jetbrains.com/issue/AIR-5385))  
  Handled the edge case where a display device is present but not attached to the desktop, preventing a crash on screen-info lookup.

- **Arch KDE Wayland: resize stuck after drag** ([AIR-5571](https://youtrack.jetbrains.com/issue/AIR-5571))  
  Fixed a window-management bug on Arch Linux with KDE Wayland where dragging to resize would leave the window permanently in resize mode.

- **Edit and Revert buttons disappear on Diff view resize** ([AIR-5319](https://youtrack.jetbrains.com/issue/AIR-5319))  
  The Edit and Revert action buttons in the Diff view now remain visible when the panel is resized.

- **Tooltip flicker on hover** ([AIR-5008](https://youtrack.jetbrains.com/issue/AIR-5008))  
  Eliminated the flickering behaviour that occurred when hovering over elements with tooltips.

---

*Produced by Air Automation. Name: Generate Release Notes / Run: https://air.stgn.jetbrains.cloud/org/05cf1a7f-6ab5-713b-abd3-29d0c8a05e2d/automations/700dc751-f867-4758-aa14-92fd8704e23d?run=d035031f-f19e-4e61-b75a-a9c2e2b52261*
