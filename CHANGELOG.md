# Changelog

## Sprint 262.132 — July 2026

> **59 completed items** (3 features, 11 improvements, 45 fixes) — sourced from YouTrack AIR project, fix version 262.132, as of 2026-07-31.

### Features (3)

- Context window and tokens display for Claude models ([AIR-5487](https://youtrack.jetbrains.com/issue/AIR-5487))
- Fast Mode support for Claude Opus via Anthropic API Billing ([AIR-4630](https://youtrack.jetbrains.com/issue/AIR-4630))
- Support Claude xhigh effort level (Fable, Opus, Sonnet 5) ([AIR-6205](https://youtrack.jetbrains.com/issue/AIR-6205))

### Improvements (11)

- UX for preventing machine from sleeping during active tasks ([AIR-5191](https://youtrack.jetbrains.com/issue/AIR-5191))
- Codex agent mode now shows generated code output ([AIR-5287](https://youtrack.jetbrains.com/issue/AIR-5287))
- Proposed diff now visible in the Editor tab ([AIR-5476](https://youtrack.jetbrains.com/issue/AIR-5476))
- Fast Mode no longer locks when a Codex chat session starts ([AIR-5613](https://youtrack.jetbrains.com/issue/AIR-5613))
- AI Quota widget added to settings popup ([AIR-5846](https://youtrack.jetbrains.com/issue/AIR-5846))
- `acp.json` shown as non-existing and empty file on first open ([AIR-6124](https://youtrack.jetbrains.com/issue/AIR-6124))
- Open in Web context actions added for Cloud tasks ([AIR-6080](https://youtrack.jetbrains.com/issue/AIR-6080))
- Chat file mentions show stale change count when file has no pending changes ([AIR-6160](https://youtrack.jetbrains.com/issue/AIR-6160))
- License texts updated on onboarding and login screens ([AIR-6217](https://youtrack.jetbrains.com/issue/AIR-6217))
- Gemini 3.6 Flash support added ([AIR-6444](https://youtrack.jetbrains.com/issue/AIR-6444))
- Environment variable interpolation supported in `.mcp.json` ([AIR-6583](https://youtrack.jetbrains.com/issue/AIR-6583))

### Fixes (45)

- Resume for worktree tasks does not work — task disappears from list after resume attempt ([AIR-6250](https://youtrack.jetbrains.com/issue/AIR-6250))
- Docker agent task hangs indefinitely at "Copying agent resources to the agent volume" — no timeout, no error, app must be force-quit ([AIR-6440](https://youtrack.jetbrains.com/issue/AIR-6440))
- OpenCode via acp.json does not answer ([AIR-6226](https://youtrack.jetbrains.com/issue/AIR-6226))
- Junie "Full Access" mode not working ([AIR-5380](https://youtrack.jetbrains.com/issue/AIR-5380))
- [Windows] Opening file from Explorer shows "Air Cannot Start: application_stop_event_loop already in progress" ([AIR-5478](https://youtrack.jetbrains.com/issue/AIR-5478))
- [Windows] Air can't open chat and tasks panel ([AIR-5761](https://youtrack.jetbrains.com/issue/AIR-5761))
- MCP Tool Call Widgets perform poorly in WASM ([AIR-6332](https://youtrack.jetbrains.com/issue/AIR-6332))
- Can't stop a task — agent does nothing and stop button does not work ([AIR-5715](https://youtrack.jetbrains.com/issue/AIR-5715))
- Crash (IndexOutOfBoundsException) when typing in "Add To Task Context" menu ([AIR-6121](https://youtrack.jetbrains.com/issue/AIR-6121))
- [Windows] Drag and Drop not supported ([AIR-5138](https://youtrack.jetbrains.com/issue/AIR-5138))
- [Windows] Can't run custom acp agent — `%1 is not a valid Win32 application` ([AIR-5759](https://youtrack.jetbrains.com/issue/AIR-5759))
- ACP tool call shows tool ID instead of tool name ([AIR-5890](https://youtrack.jetbrains.com/issue/AIR-5890))
- Air using Credits over API tokens ([AIR-6367](https://youtrack.jetbrains.com/issue/AIR-6367))
- Fast Mode toggle missing for OpenAI 5.6 models ([AIR-6389](https://youtrack.jetbrains.com/issue/AIR-6389))
- Custom agents not filtered for Docker task run ([AIR-6211](https://youtrack.jetbrains.com/issue/AIR-6211))
- Table UI and scroll behavior in chat output ([AIR-5045](https://youtrack.jetbrains.com/issue/AIR-5045))
- Alignment of messages is broken in chat ([AIR-5791](https://youtrack.jetbrains.com/issue/AIR-5791))
- Claude is not aware of skills in `.agents/skills` ([AIR-6141](https://youtrack.jetbrains.com/issue/AIR-6141))
- Claude Fable incorrectly showed 200K context window instead of 1M ([AIR-6065](https://youtrack.jetbrains.com/issue/AIR-6065))
- Codex was asking for permissions in full access mode ([AIR-6010](https://youtrack.jetbrains.com/issue/AIR-6010))
- Junie ignores permission level ([AIR-5722](https://youtrack.jetbrains.com/issue/AIR-5722))
- Unable to log in using JetBrains account ([AIR-5465](https://youtrack.jetbrains.com/issue/AIR-5465))
- MCP call panel not horizontally scrollable ([AIR-5849](https://youtrack.jetbrains.com/issue/AIR-5849))
- Claude compact summary & progress widget dropped on synthetic User events ([AIR-6289](https://youtrack.jetbrains.com/issue/AIR-6289))
- Agents not filtered for cloud task run ([AIR-6210](https://youtrack.jetbrains.com/issue/AIR-6210))
- Clear command doesn't work ([AIR-5599](https://youtrack.jetbrains.com/issue/AIR-5599))
- Error using Copilot via acp: attempted to query hidden partition ([AIR-6317](https://youtrack.jetbrains.com/issue/AIR-6317))
- "Auto-open task changes" does not work for Codex ([AIR-6450](https://youtrack.jetbrains.com/issue/AIR-6450))
- Git status normalization worker rewritten to fix incorrect state reporting ([AIR-5709](https://youtrack.jetbrains.com/issue/AIR-5709))
- Text search searched across all tasks instead of the current one ([AIR-5716](https://youtrack.jetbrains.com/issue/AIR-5716))
- File mentions were provided by all tasks instead of the current one ([AIR-5721](https://youtrack.jetbrains.com/issue/AIR-5721))
- Commands, skills and subagents were provided from all tasks ([AIR-5723](https://youtrack.jetbrains.com/issue/AIR-5723))
- Wrong file root shown in the "New Task" screen ([AIR-5724](https://youtrack.jetbrains.com/issue/AIR-5724))
- Diff and Changes tools now support multi-repo scenarios ([AIR-5725](https://youtrack.jetbrains.com/issue/AIR-5725))
- Repo selector in History tool showed repos from all tasks ([AIR-5726](https://youtrack.jetbrains.com/issue/AIR-5726))
- Git-related actions now work with the current task's repository only ([AIR-5727](https://youtrack.jetbrains.com/issue/AIR-5727))
- Git header showed all repos and could display wrong current branch ([AIR-5728](https://youtrack.jetbrains.com/issue/AIR-5728))
- Chat mentions showed branches/commits from all tasks ([AIR-5729](https://youtrack.jetbrains.com/issue/AIR-5729))
- Agent requirements check now scoped to the current task only ([AIR-5730](https://youtrack.jetbrains.com/issue/AIR-5730))
- Changes and Diff tools showed files from all tasks ([AIR-5731](https://youtrack.jetbrains.com/issue/AIR-5731))
- Local history restore picked the wrong repository in multi-root workspaces ([AIR-5741](https://youtrack.jetbrains.com/issue/AIR-5741))
- AI Docs were saved to the wrong project root when created ([AIR-5750](https://youtrack.jetbrains.com/issue/AIR-5750))
- MCP settings showed servers from all tasks ([AIR-5718](https://youtrack.jetbrains.com/issue/AIR-5718))
- Settings showed all workspace roots for all tasks ([AIR-5719](https://youtrack.jetbrains.com/issue/AIR-5719))
- Chat banners did not span the full panel width ([AIR-5530](https://youtrack.jetbrains.com/issue/AIR-5530))

---

## Sprint 262.43 — June 2026

> **31 completed items** (2 features, 6 improvements, 23 fixes) — sourced from YouTrack AIR project, fix version 262.43.

### Features (2)

- Open in IDE (IJ-family) for local project & changes ([AIR-3687](https://youtrack.jetbrains.com/issue/AIR-3687))
- Windows support ([AIR-4132](https://youtrack.jetbrains.com/issue/AIR-4132))

### Improvements (6)

- Slash menu updated ([AIR-5208](https://youtrack.jetbrains.com/issue/AIR-5208))
- Linux X11: IME support in editor ([AIR-5611](https://youtrack.jetbrains.com/issue/AIR-5611))
- Linux Wayland: IME support in editor ([AIR-5610](https://youtrack.jetbrains.com/issue/AIR-5610))
- [Windows] Font rendering quality improved in editor ([AIR-4755](https://youtrack.jetbrains.com/issue/AIR-4755))
- [Windows] Native caption buttons drawn with Compose ([AIR-5600](https://youtrack.jetbrains.com/issue/AIR-5600))
- [Windows] Native-style buttons in update dialog ([AIR-5755](https://youtrack.jetbrains.com/issue/AIR-5755))

### Fixes (23)

- Tasks and changes not loading after 262.34 update — show-stopper ([AIR-5640](https://youtrack.jetbrains.com/issue/AIR-5640))
- Chat messages invisible until task is stopped ([AIR-5583](https://youtrack.jetbrains.com/issue/AIR-5583))
- Folder mentioned in a task copied into itself on Docker task run ([AIR-5670](https://youtrack.jetbrains.com/issue/AIR-5670))
- Air cannot start — null return value in RenderLoop initialization ([AIR-5645](https://youtrack.jetbrains.com/issue/AIR-5645))
- [Windows] 'window_get_screen_info' error — display device not attached to desktop ([AIR-5385](https://youtrack.jetbrains.com/issue/AIR-5385))
- [Windows] Kotlin LSP does not work — failed to CreateProcessW ([AIR-5760](https://youtrack.jetbrains.com/issue/AIR-5760))
- Invoking Review with Agent from active session deletes entire parent task ([AIR-5570](https://youtrack.jetbrains.com/issue/AIR-5570))
- Junie approval view shows no content ([AIR-4794](https://youtrack.jetbrains.com/issue/AIR-4794))
- Junie can't use mcp__Air__add_comment tool — agent review broken ([AIR-4097](https://youtrack.jetbrains.com/issue/AIR-4097))
- Uncommitted changes lost on Implement in Worktree agent ([AIR-5484](https://youtrack.jetbrains.com/issue/AIR-5484))
- Uncommitted changes lost on Implement in Docker agent ([AIR-5538](https://youtrack.jetbrains.com/issue/AIR-5538))
- Commit message input missing in Diff view ([AIR-5101](https://youtrack.jetbrains.com/issue/AIR-5101))
- Commits list not shown after Worktree plan implementation ([AIR-5240](https://youtrack.jetbrains.com/issue/AIR-5240))
- Can't open files linked in agent markdown plans ([AIR-5449](https://youtrack.jetbrains.com/issue/AIR-5449))
- Edit and Revert buttons disappear on Diff view resize ([AIR-5319](https://youtrack.jetbrains.com/issue/AIR-5319))
- Thinking level switcher missing from UI ([AIR-5606](https://youtrack.jetbrains.com/issue/AIR-5606))
- Application menu closes unexpectedly when moving mouse between options ([AIR-5639](https://youtrack.jetbrains.com/issue/AIR-5639))
- [Linux/KDE Wayland] Resize stuck ([AIR-5571](https://youtrack.jetbrains.com/issue/AIR-5571))
- High CPU usage during idle state ([AIR-5812](https://youtrack.jetbrains.com/issue/AIR-5812))
- [Windows] Copy does not work ([AIR-5558](https://youtrack.jetbrains.com/issue/AIR-5558))
- Tooltip flicker on hover ([AIR-5008](https://youtrack.jetbrains.com/issue/AIR-5008))
- Failed to parse Claude event (SerializationException on streaming response) ([AIR-6434](https://youtrack.jetbrains.com/issue/AIR-6434))
- Scrolling very slow in task view ([AIR-5233](https://youtrack.jetbrains.com/issue/AIR-5233))

---

*Produced by Air Automation. Name: Generate Release Notes / Run: https://air.stgn.jetbrains.cloud/org/05cf1a7f-6ab5-713b-abd3-29d0c8a05e2d/automations/84f198de-fcdc-48af-9342-c6e9886c9e56?run=a7090ab1-aec9-4dc2-b6ef-7accab5c5570*
