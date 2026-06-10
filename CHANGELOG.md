# Changelog

## Sprint 262.43 — June 2026

This release is a focused bug-fix sprint. No new features or improvements were shipped; all resolved work addresses stability, UI correctness, and agent workflow issues.

### Fixes

- **Tasks and changes not loading after update to 262.34** ([AIR-5640](https://youtrack.jetbrains.com/issue/AIR-5640))
  Tasks and the Changes tool failed to load following an update to version 262.34. The affected views now load correctly after updating.

- **Junie approval view missing content** ([AIR-4794](https://youtrack.jetbrains.com/issue/AIR-4794))
  The Junie approval panel showed an empty view, preventing users from reviewing what Junie intended to do before approving. Content is now displayed as expected.

- **Thinking level switcher missing from the UI** ([AIR-5606](https://youtrack.jetbrains.com/issue/AIR-5606))
  The control for selecting the agent thinking level disappeared from the interface. It has been restored.

- **Uncommitted changes lost when using "Implement" in Docker agent** ([AIR-5538](https://youtrack.jetbrains.com/issue/AIR-5538))
  Choosing "Implement" in a Docker-based task discarded any uncommitted local changes. Uncommitted changes are now correctly carried over.

- **Uncommitted changes lost when using "Implement" in Worktree agent** ([AIR-5484](https://youtrack.jetbrains.com/issue/AIR-5484))
  Same issue as AIR-5538, specific to Worktree-based tasks. Uncommitted changes are now preserved when switching to "Implement" in a Worktree agent.

- **Commits list not shown in Changes tool after implementing a plan in Worktree** ([AIR-5240](https://youtrack.jetbrains.com/issue/AIR-5240))
  After implementing a plan inside a Worktree agent, the Changes tool showed no commits. The commits list is now populated correctly.

- **Commit message input missing in Changes tool Diff view** ([AIR-5101](https://youtrack.jetbrains.com/issue/AIR-5101))
  The text field for entering a commit message was absent from the Diff view in the Changes tool. The input is now present and functional.

- **Edit and Revert buttons disappear when resizing the Diff view** ([AIR-5319](https://youtrack.jetbrains.com/issue/AIR-5319))
  Resizing the Diff view caused the Edit and Revert buttons to vanish from the file list. The buttons now remain visible regardless of the panel size.

- **Chat banners not spanning full width** ([AIR-5530](https://youtrack.jetbrains.com/issue/AIR-5530))
  Informational banners in the chat panel did not stretch to the full width of the panel, resulting in a visually misaligned layout. Banners now fill the available width.

- **Tooltip flicker when hovering between items** ([AIR-5008](https://youtrack.jetbrains.com/issue/AIR-5008))
  Rapidly moving the cursor between items with tooltips caused visible flicker as tooltips rapidly appeared and disappeared. Tooltip display is now stable on hover.

---

*Produced by Air Automation. Name: Generate Release Notes / Run: https://air.stgn.jetbrains.cloud/org/05cf1a7f-6ab5-713b-abd3-29d0c8a05e2d/automations/700dc751-f867-4758-aa14-92fd8704e23d?run=2f33e800-0f29-4e3a-933c-698feb1dda85*
