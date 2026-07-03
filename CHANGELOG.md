# Changelog

## Sprint 262.132 — July 2026

### Features (2)

- Context window and tokens display for Claude models ([AIR-5487](https://youtrack.jetbrains.com/issue/AIR-5487))
- Fast Mode support for Claude Opus via Anthropic API Billing ([AIR-4630](https://youtrack.jetbrains.com/issue/AIR-4630))

### Improvements (3)

- UX for preventing machine from sleeping during active tasks ([AIR-5191](https://youtrack.jetbrains.com/issue/AIR-5191))
- Codex agent mode now shows generated code output ([AIR-5287](https://youtrack.jetbrains.com/issue/AIR-5287))
- Fast Mode no longer locks when a Codex chat session starts ([AIR-5613](https://youtrack.jetbrains.com/issue/AIR-5613))

### Fixes (26)

- Air can't open chat and tasks panel on Windows ([AIR-5761](https://youtrack.jetbrains.com/issue/AIR-5761))
- [Windows] Drag and Drop not supported ([AIR-5138](https://youtrack.jetbrains.com/issue/AIR-5138))
- [Windows] Can't run custom acp agent — `%1 is not a valid Win32 application` ([AIR-5759](https://youtrack.jetbrains.com/issue/AIR-5759))
- Alignment of messages is broken in chat ([AIR-5791](https://youtrack.jetbrains.com/issue/AIR-5791))
- Table UI and scroll behavior in chat output ([AIR-5045](https://youtrack.jetbrains.com/issue/AIR-5045))
- Text search searched across all tasks instead of the current one ([AIR-5716](https://youtrack.jetbrains.com/issue/AIR-5716))
- File mentions were provided by all tasks instead of the current one ([AIR-5721](https://youtrack.jetbrains.com/issue/AIR-5721))
- Commands, skills and subagents were provided from all tasks ([AIR-5723](https://youtrack.jetbrains.com/issue/AIR-5723))
- Diff and Changes tools now support multi-repo scenarios ([AIR-5725](https://youtrack.jetbrains.com/issue/AIR-5725))
- Repo selector in History tool showed repos from all tasks ([AIR-5726](https://youtrack.jetbrains.com/issue/AIR-5726))
- Git-related actions now work with the current task's repository only ([AIR-5727](https://youtrack.jetbrains.com/issue/AIR-5727))
- Git header showed all repos and could display wrong current branch ([AIR-5728](https://youtrack.jetbrains.com/issue/AIR-5728))
- Chat mentions showed branches/commits from all tasks ([AIR-5729](https://youtrack.jetbrains.com/issue/AIR-5729))
- Agent requirements check now scoped to the current task only ([AIR-5730](https://youtrack.jetbrains.com/issue/AIR-5730))
- Changes and Diff tools showed files from all tasks ([AIR-5731](https://youtrack.jetbrains.com/issue/AIR-5731))
- Wrong file root shown in the "New Task" screen ([AIR-5724](https://youtrack.jetbrains.com/issue/AIR-5724))
- MCP settings showed servers from all tasks ([AIR-5718](https://youtrack.jetbrains.com/issue/AIR-5718))
- Settings showed all workspace roots for all tasks ([AIR-5719](https://youtrack.jetbrains.com/issue/AIR-5719))
- AI Docs were saved to the wrong project root when created ([AIR-5750](https://youtrack.jetbrains.com/issue/AIR-5750))
- Local history restore picked the wrong repository in multi-root workspaces ([AIR-5741](https://youtrack.jetbrains.com/issue/AIR-5741))
- Claude Fable incorrectly showed 200K context window instead of 1M ([AIR-6065](https://youtrack.jetbrains.com/issue/AIR-6065))
- Codex was asking for permissions in full access mode ([AIR-6010](https://youtrack.jetbrains.com/issue/AIR-6010))
- Unable to log in using JetBrains account ([AIR-5465](https://youtrack.jetbrains.com/issue/AIR-5465))
- MCP call panel not horizontally scrollable ([AIR-5849](https://youtrack.jetbrains.com/issue/AIR-5849))
- Chat banners did not span the full panel width ([AIR-5530](https://youtrack.jetbrains.com/issue/AIR-5530))
- Fixed git status normalization worker ([AIR-5709](https://youtrack.jetbrains.com/issue/AIR-5709))

---

## Sprint 262.43 — June 2026

### Features (2)

- Fast Mode support for Claude Opus 4.6 via API Billing ([AIR-4630](https://youtrack.jetbrains.com/issue/AIR-4630))
- Empty drafts are automatically removed ([AIR-4083](https://youtrack.jetbrains.com/issue/AIR-4083))

### Improvements (2)

- [Windows] Air icon alignment in main toolbar ([AIR-5608](https://youtrack.jetbrains.com/issue/AIR-5608))
- [Windows] Duplicate progress spinner during Apply Locally ([AIR-5609](https://youtrack.jetbrains.com/issue/AIR-5609))

### Fixes (17)

- Tasks and changes not loading after 262.34 update — show-stopper ([AIR-5640](https://youtrack.jetbrains.com/issue/AIR-5640))
- Air fails to start on certain configurations ([AIR-5645](https://youtrack.jetbrains.com/issue/AIR-5645))
- Chat messages invisible until task is stopped ([AIR-5583](https://youtrack.jetbrains.com/issue/AIR-5583))
- MCP servers list appears empty when servers are available ([AIR-5561](https://youtrack.jetbrains.com/issue/AIR-5561))
- Excessive warnings for unknown permission modes ([AIR-5661](https://youtrack.jetbrains.com/issue/AIR-5661))
- Table rendering and scroll in Chat output ([AIR-5045](https://youtrack.jetbrains.com/issue/AIR-5045))
- Junie approval view shows no content ([AIR-4794](https://youtrack.jetbrains.com/issue/AIR-4794))
- Thinking level switcher missing from UI ([AIR-5606](https://youtrack.jetbrains.com/issue/AIR-5606))
- Uncommitted changes lost on Implement in Docker agent ([AIR-5538](https://youtrack.jetbrains.com/issue/AIR-5538))
- Uncommitted changes lost on Implement in Worktree agent ([AIR-5484](https://youtrack.jetbrains.com/issue/AIR-5484))
- Commits list not shown after Worktree plan implementation ([AIR-5240](https://youtrack.jetbrains.com/issue/AIR-5240))
- Can't open files linked in agent markdown plans ([AIR-5449](https://youtrack.jetbrains.com/issue/AIR-5449))
- Commit message input missing in Diff view ([AIR-5101](https://youtrack.jetbrains.com/issue/AIR-5101))
- Edit and Revert buttons disappear on Diff view resize ([AIR-5319](https://youtrack.jetbrains.com/issue/AIR-5319))
- Chat banners not spanning full panel width ([AIR-5530](https://youtrack.jetbrains.com/issue/AIR-5530))
- [Windows] Copy does not work ([AIR-5558](https://youtrack.jetbrains.com/issue/AIR-5558))
- Tooltip flicker on hover ([AIR-5008](https://youtrack.jetbrains.com/issue/AIR-5008))
