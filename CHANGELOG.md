# Changelog

## Sprint 262.43 — June 2026

24 completed issues · 2 features · 3 improvements · 19 fixes

---

### Features

- **Fast Mode support for Claude Opus 4.6 via API Billing** ([AIR-4630](https://youtrack.jetbrains.com/issue/AIR-4630))  
  Users can now activate Fast Mode for Claude Opus 4.6 when billing is handled via the API, enabling accelerated responses for supported plans.

- **Empty drafts are automatically removed** ([AIR-4083](https://youtrack.jetbrains.com/issue/AIR-4083))  
  Draft messages left empty are now cleaned up automatically, reducing clutter in the drafts list.

---

### Improvements

- **Update Slash menu** ([AIR-5208](https://youtrack.jetbrains.com/issue/AIR-5208))  
  The slash command menu has been updated with revised entries and improved discoverability.

- **[Windows] Air icon alignment in main toolbar** ([AIR-5608](https://youtrack.jetbrains.com/issue/AIR-5608))  
  Corrected the visual alignment of the Air icon in the main toolbar on Windows.

- **[Windows] Duplicate progress spinner during Apply Locally** ([AIR-5609](https://youtrack.jetbrains.com/issue/AIR-5609))  
  Removed a redundant progress spinner that appeared alongside the existing one when applying changes locally on Windows.

---

### Fixes

- **Tasks and changes not loading after 262.34 update** ([AIR-5640](https://youtrack.jetbrains.com/issue/AIR-5640)) *(show-stopper)*  
  Fixed a regression introduced in 262.34 that prevented tasks and change lists from loading on startup.

- **Air fails to start on certain configurations** ([AIR-5645](https://youtrack.jetbrains.com/issue/AIR-5645))  
  Resolved a startup failure affecting specific system configurations.

- **Folder mentioned in a task is copied into itself on Docker task run** ([AIR-5670](https://youtrack.jetbrains.com/issue/AIR-5670)) *(critical)*  
  Fixed a critical bug where mentioning a project folder in a Docker task caused the folder to be recursively copied into itself when the task ran.

- **Junie cannot use mcp__Air__add_comment tool in agent review** ([AIR-4097](https://youtrack.jetbrains.com/issue/AIR-4097))  
  Resolved a tool-access issue that prevented Junie from posting comments when acting as an agent reviewer, restoring its full agent review capability.

- **Chat messages invisible until task is stopped** ([AIR-5583](https://youtrack.jetbrains.com/issue/AIR-5583))  
  Chat messages now render correctly while a task is running, without requiring the task to be stopped first.

- **MCP servers list appears empty when servers are available** ([AIR-5561](https://youtrack.jetbrains.com/issue/AIR-5561))  
  Fixed a display issue where the MCP servers list showed as empty even when servers were connected and available.

- **Excessive warnings for unknown permission modes** ([AIR-5661](https://youtrack.jetbrains.com/issue/AIR-5661))  
  Suppressed noisy warning messages that were incorrectly triggered by unrecognised permission mode values.

- **Table rendering and scroll in Chat output** ([AIR-5045](https://youtrack.jetbrains.com/issue/AIR-5045))  
  Tables in Chat output now render and scroll correctly.

- **Junie approval view shows no content** ([AIR-4794](https://youtrack.jetbrains.com/issue/AIR-4794))  
  Resolved an issue where the Junie approval view was blank instead of displaying the relevant content.

- **Thinking level switcher missing from UI** ([AIR-5606](https://youtrack.jetbrains.com/issue/AIR-5606))  
  Restored the thinking level switcher control that had disappeared from the interface.

- **Uncommitted changes lost on Implement in Docker agent** ([AIR-5538](https://youtrack.jetbrains.com/issue/AIR-5538))  
  Uncommitted local changes are now preserved when running the Implement action inside a Docker agent.

- **Uncommitted changes lost on Implement in Worktree agent** ([AIR-5484](https://youtrack.jetbrains.com/issue/AIR-5484))  
  Uncommitted local changes are now preserved when running the Implement action inside a Worktree agent.

- **Commits list not shown after Worktree plan implementation** ([AIR-5240](https://youtrack.jetbrains.com/issue/AIR-5240))  
  The commits list is now displayed correctly after a plan is implemented using the Worktree agent.

- **Can't open files linked in agent markdown plans** ([AIR-5449](https://youtrack.jetbrains.com/issue/AIR-5449))  
  File links embedded in agent-generated markdown plans can now be opened directly from the plan view.

- **Commit message input missing in Diff view** ([AIR-5101](https://youtrack.jetbrains.com/issue/AIR-5101))  
  The commit message input field is now reliably visible in the Diff view.

- **Edit and Revert buttons disappear on Diff view resize** ([AIR-5319](https://youtrack.jetbrains.com/issue/AIR-5319))  
  The Edit and Revert action buttons in the Diff view remain visible when the panel is resized.

- **Chat banners not spanning full panel width** ([AIR-5530](https://youtrack.jetbrains.com/issue/AIR-5530))  
  Chat notification banners now correctly span the full width of the chat panel.

- **[Windows] Copy does not work** ([AIR-5558](https://youtrack.jetbrains.com/issue/AIR-5558))  
  Fixed a Windows-specific bug that prevented the copy action from functioning in certain contexts.

- **Tooltip flicker on hover** ([AIR-5008](https://youtrack.jetbrains.com/issue/AIR-5008))  
  Eliminated the flickering behaviour that occurred when hovering over elements with tooltips.

---

*Produced by Air Automation. Name: Generate Release Notes / Run: https://air.stgn.jetbrains.cloud/org/05cf1a7f-6ab5-713b-abd3-29d0c8a05e2d/automations/700dc751-f867-4758-aa14-92fd8704e23d?run=fb5df396-664f-4ed1-bf8a-db354f01a061*
