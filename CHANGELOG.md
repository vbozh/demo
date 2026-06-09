# Changelog

## Sprint 262.43 — June 2026

### Fixes

- **Tasks and changes not loading after update** — Fixed a regression introduced in version 262.34 where tasks and their associated changes failed to load, leaving the task list empty. ([AIR-5640](https://youtrack.jetbrains.com/issue/AIR-5640))
- **Junie approval view missing content** — Fixed an issue where users could not see the details of what Junie was requesting approval for, making it impossible to make an informed decision. ([AIR-4794](https://youtrack.jetbrains.com/issue/AIR-4794))
- **Thinking level switcher missing** — Restored the thinking level switcher that disappeared from the UI following a recent update. ([AIR-5606](https://youtrack.jetbrains.com/issue/AIR-5606))
- **Uncommitted changes lost on "Implement" in Docker** — Fixed a bug where uncommitted local changes were not carried over into the Docker environment when choosing the Implement action. ([AIR-5538](https://youtrack.jetbrains.com/issue/AIR-5538))
- **Uncommitted changes lost on "Implement" in Worktree** — Fixed the same uncommitted changes propagation issue for Worktree-based implementation. ([AIR-5484](https://youtrack.jetbrains.com/issue/AIR-5484))
- **Commits list not shown after plan implemented in Worktree** — Fixed the Changes tool failing to display the commit history after a plan was implemented using a Worktree. ([AIR-5240](https://youtrack.jetbrains.com/issue/AIR-5240))
- **Commit message input missing in Diff view** — Fixed the Changes tool not showing the commit message input field when viewing a diff, preventing users from composing a commit from that view. ([AIR-5101](https://youtrack.jetbrains.com/issue/AIR-5101))
- **Edit and Revert buttons disappear on Diff view resize** — Fixed a layout issue where the Edit and Revert action buttons would disappear from the file list in the Diff view when the panel was resized. ([AIR-5319](https://youtrack.jetbrains.com/issue/AIR-5319))
- **Chat banners not spanning full width** — Fixed chat notification banners being narrower than the chat panel, causing them to appear misaligned. ([AIR-5530](https://youtrack.jetbrains.com/issue/AIR-5530))
- **Tooltip flicker on hover** — Fixed tooltips flickering when moving the cursor between elements where a tooltip was already visible. ([AIR-5008](https://youtrack.jetbrains.com/issue/AIR-5008))
