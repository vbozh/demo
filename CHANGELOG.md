# Changelog

## Sprint 262.132 (July 2026)

**60 completed items** — 6 features, 10 improvements, 44 fixes.
Sourced from YouTrack AIR project, fix version 262.132, as of 2026-07-24.

### Features

- Context window and tokens display for Claude models ([AIR-5487](https://youtrack.jetbrains.com/issue/AIR-5487))
- Fast Mode support for Claude Opus via Anthropic API Billing ([AIR-4630](https://youtrack.jetbrains.com/issue/AIR-4630))
- Support Claude xhigh effort level (Fable, Opus, Sonnet 5) ([AIR-6205](https://youtrack.jetbrains.com/issue/AIR-6205))
- Add ability to see proposed diff in the Editor tab ([AIR-5476](https://youtrack.jetbrains.com/issue/AIR-5476))
- AI Quota widget in settings popup ([AIR-5846](https://youtrack.jetbrains.com/issue/AIR-5846))
- Support for Gemini 3.6 Flash ([AIR-6444](https://youtrack.jetbrains.com/issue/AIR-6444))

### Improvements

- UX for preventing machine from sleeping during active tasks ([AIR-5191](https://youtrack.jetbrains.com/issue/AIR-5191))
- Codex agent mode now shows generated code output ([AIR-5287](https://youtrack.jetbrains.com/issue/AIR-5287))
- Fast Mode no longer locks when a Codex chat session starts ([AIR-5613](https://youtrack.jetbrains.com/issue/AIR-5613))
- `acp.json` shown as non-existing and empty file on first open ([AIR-6124](https://youtrack.jetbrains.com/issue/AIR-6124))
- Open in Web context actions added for Cloud tasks ([AIR-6080](https://youtrack.jetbrains.com/issue/AIR-6080))
- Chat file mentions no longer show stale change count ([AIR-6160](https://youtrack.jetbrains.com/issue/AIR-6160))
- Fast mode toggle shown for OpenAI 5.6 models ([AIR-6389](https://youtrack.jetbrains.com/issue/AIR-6389))
- Agents filtered out for cloud task runs ([AIR-6210](https://youtrack.jetbrains.com/issue/AIR-6210))
- Custom agents filtered out for Docker task runs ([AIR-6211](https://youtrack.jetbrains.com/issue/AIR-6211))
- Updated license texts on onboarding and login screens ([AIR-6217](https://youtrack.jetbrains.com/issue/AIR-6217))

### Fixes

- Unable to log in using JetBrains account ([AIR-5465](https://youtrack.jetbrains.com/issue/AIR-5465))
- Air can't open chat and tasks panel on Windows ([AIR-5761](https://youtrack.jetbrains.com/issue/AIR-5761))
- [Windows] Drag and drop not supported ([AIR-5138](https://youtrack.jetbrains.com/issue/AIR-5138))
- [Windows] Can't run custom acp agent — `%1 is not a valid Win32 application` ([AIR-5759](https://youtrack.jetbrains.com/issue/AIR-5759))
- [Windows] Opening file from Explorer shows "Air Cannot Start: application_stop_event_loop already in progress" ([AIR-5478](https://youtrack.jetbrains.com/issue/AIR-5478))
- Alignment of messages is broken in chat ([AIR-5791](https://youtrack.jetbrains.com/issue/AIR-5791))
- Table UI and scroll behavior in chat output ([AIR-5045](https://youtrack.jetbrains.com/issue/AIR-5045))
- Chat banners did not span the full panel width ([AIR-5530](https://youtrack.jetbrains.com/issue/AIR-5530))
- MCP call panel not horizontally scrollable ([AIR-5849](https://youtrack.jetbrains.com/issue/AIR-5849))
- ACP tool call shows tool ID instead of tool name ([AIR-5890](https://youtrack.jetbrains.com/issue/AIR-5890))
- Junie "Full Access" mode not working ([AIR-5380](https://youtrack.jetbrains.com/issue/AIR-5380))
- Junie ignores permission level ([AIR-5722](https://youtrack.jetbrains.com/issue/AIR-5722))
- Junie cloud task started with Full Access switched to Ask mode ([AIR-6249](https://youtrack.jetbrains.com/issue/AIR-6249))
- Can't stop a task — agent does nothing and stop button does not work ([AIR-5715](https://youtrack.jetbrains.com/issue/AIR-5715))
- Resume for worktree tasks does not work — task disappears from list after resume attempt ([AIR-6250](https://youtrack.jetbrains.com/issue/AIR-6250))
- Docker agent task hangs indefinitely at "Copying agent resources" — no timeout, no error, app must be force-quit ([AIR-6440](https://youtrack.jetbrains.com/issue/AIR-6440))
- Claude Fable incorrectly showed 200K context window instead of 1M ([AIR-6065](https://youtrack.jetbrains.com/issue/AIR-6065))
- Claude compact summary and progress widget dropped on synthetic User events ([AIR-6289](https://youtrack.jetbrains.com/issue/AIR-6289))
- Codex was asking for permissions in full access mode ([AIR-6010](https://youtrack.jetbrains.com/issue/AIR-6010))
- Claude is not aware of skills in `.agents/skills` ([AIR-6141](https://youtrack.jetbrains.com/issue/AIR-6141))
- OpenCode via acp.json does not answer ([AIR-6226](https://youtrack.jetbrains.com/issue/AIR-6226))
- Error while using Copilot via acp — attempted to query hidden partition ([AIR-6317](https://youtrack.jetbrains.com/issue/AIR-6317))
- "Auto-open task changes" doesn't work for Codex ([AIR-6450](https://youtrack.jetbrains.com/issue/AIR-6450))
- Crash (IndexOutOfBoundsException) when typing in "Add To Task Context" menu ([AIR-6121](https://youtrack.jetbrains.com/issue/AIR-6121))
- Clear command doesn't work ([AIR-5599](https://youtrack.jetbrains.com/issue/AIR-5599))
- Air using Credits over API tokens ([AIR-6367](https://youtrack.jetbrains.com/issue/AIR-6367))
- MCP Tool Call Widgets perform poorly in WASM ([AIR-6332](https://youtrack.jetbrains.com/issue/AIR-6332))
- Fixed git status normalization worker ([AIR-5709](https://youtrack.jetbrains.com/issue/AIR-5709))
- Multi-root workspace task-isolation fixes — text search, file mentions, commands/skills/subagents, Diff/Changes tools, repo selector, git actions/header, chat mentions, agent requirements check, MCP settings, workspace roots, AI Docs, local history restore, git awareness, New Task screen file root ([AIR-5716](https://youtrack.jetbrains.com/issue/AIR-5716) · [AIR-5718](https://youtrack.jetbrains.com/issue/AIR-5718) · [AIR-5719](https://youtrack.jetbrains.com/issue/AIR-5719) · [AIR-5721](https://youtrack.jetbrains.com/issue/AIR-5721) · [AIR-5723](https://youtrack.jetbrains.com/issue/AIR-5723) · [AIR-5724](https://youtrack.jetbrains.com/issue/AIR-5724) · [AIR-5725](https://youtrack.jetbrains.com/issue/AIR-5725) · [AIR-5726](https://youtrack.jetbrains.com/issue/AIR-5726) · [AIR-5727](https://youtrack.jetbrains.com/issue/AIR-5727) · [AIR-5728](https://youtrack.jetbrains.com/issue/AIR-5728) · [AIR-5729](https://youtrack.jetbrains.com/issue/AIR-5729) · [AIR-5730](https://youtrack.jetbrains.com/issue/AIR-5730) · [AIR-5731](https://youtrack.jetbrains.com/issue/AIR-5731) · [AIR-5741](https://youtrack.jetbrains.com/issue/AIR-5741) · [AIR-5750](https://youtrack.jetbrains.com/issue/AIR-5750) · [AIR-5502](https://youtrack.jetbrains.com/issue/AIR-5502))

---

## Sprint 262.43 (June 2026)

**43 completed items** — 4 features, 6 improvements, 33 fixes.
Sourced from YouTrack AIR project, fix version 262.43.

### Features

- Open in IDE (IJ-family) for local project & changes ([AIR-3687](https://youtrack.jetbrains.com/issue/AIR-3687))
- Windows support ([AIR-4132](https://youtrack.jetbrains.com/issue/AIR-4132))
- Linux Wayland: implement IME in editor ([AIR-5610](https://youtrack.jetbrains.com/issue/AIR-5610))
- Linux X11: implement IME in editor ([AIR-5611](https://youtrack.jetbrains.com/issue/AIR-5611))

### Improvements

- [Windows] Native-style buttons in update dialog ([AIR-5755](https://youtrack.jetbrains.com/issue/AIR-5755))
- [Windows] Native caption buttons drawn with Compose ([AIR-5600](https://youtrack.jetbrains.com/issue/AIR-5600))
- [Windows] Font rendering quality in editor ([AIR-4755](https://youtrack.jetbrains.com/issue/AIR-4755))
- [Windows] Air icon alignment on main toolbar ([AIR-5608](https://youtrack.jetbrains.com/issue/AIR-5608))
- Update Slash menu ([AIR-5208](https://youtrack.jetbrains.com/issue/AIR-5208))
- Terminal commands shown as code snippets in archived tasks ([AIR-3335](https://youtrack.jetbrains.com/issue/AIR-3335))

### Fixes

- Tasks and changes not loading after 262.34 update — show-stopper ([AIR-5640](https://youtrack.jetbrains.com/issue/AIR-5640))
- Chat messages invisible until task is stopped — critical ([AIR-5583](https://youtrack.jetbrains.com/issue/AIR-5583))
- Folder mentioned in a task is copied into itself on Docker task run — critical ([AIR-5670](https://youtrack.jetbrains.com/issue/AIR-5670))
- Air cannot start after Toolbox update ([AIR-5645](https://youtrack.jetbrains.com/issue/AIR-5645))
- CPU hog in idle ([AIR-5812](https://youtrack.jetbrains.com/issue/AIR-5812))
- Scrolling is very slow ([AIR-5233](https://youtrack.jetbrains.com/issue/AIR-5233))
- Kotlin LSP does not work on Windows ([AIR-5760](https://youtrack.jetbrains.com/issue/AIR-5760))
- [Windows] Copy does not work ([AIR-5558](https://youtrack.jetbrains.com/issue/AIR-5558))
- [Windows] Terminal stops working when window is minimized ([AIR-5316](https://youtrack.jetbrains.com/issue/AIR-5316))
- [Windows] Can't run custom acp agent — `%1 is not a valid Win32 application` ([AIR-5759](https://youtrack.jetbrains.com/issue/AIR-5759))
- [Windows] Agent's final response is sometimes missing from the chat ([AIR-5738](https://youtrack.jetbrains.com/issue/AIR-5738))
- `window_get_screen_info` error when display device is not attached to desktop ([AIR-5385](https://youtrack.jetbrains.com/issue/AIR-5385))
- Arch KDE Wayland: resize stuck after drag ([AIR-5571](https://youtrack.jetbrains.com/issue/AIR-5571))
- Invoking Review with Agent from active session deletes entire parent task ([AIR-5570](https://youtrack.jetbrains.com/issue/AIR-5570))
- Agent launch blocked with "No Git Repository Found" when workspace has no commits ([AIR-5565](https://youtrack.jetbrains.com/issue/AIR-5565))
- Agent not starting when workspace was initially in "Safe Mode" ([AIR-5525](https://youtrack.jetbrains.com/issue/AIR-5525))
- Uncommitted changes lost on Implement in Worktree agent ([AIR-5484](https://youtrack.jetbrains.com/issue/AIR-5484))
- Uncommitted changes lost on Implement in Docker agent ([AIR-5538](https://youtrack.jetbrains.com/issue/AIR-5538))
- Resume Docker task does not work correctly due to race condition ([AIR-4270](https://youtrack.jetbrains.com/issue/AIR-4270))
- Gemini asks permission for AskUserQuestion tool ([AIR-4606](https://youtrack.jetbrains.com/issue/AIR-4606))
- Failed to parse Claude System "commands_changed" ([AIR-5857](https://youtrack.jetbrains.com/issue/AIR-5857))
- Unable to log in using JetBrains account ([AIR-5465](https://youtrack.jetbrains.com/issue/AIR-5465))
- Junie approval view shows no content ([AIR-4794](https://youtrack.jetbrains.com/issue/AIR-4794))
- Junie cannot use `mcp__Air__add_comment` tool in agent review ([AIR-4097](https://youtrack.jetbrains.com/issue/AIR-4097))
- Can't open files linked in agent markdown plans ([AIR-5449](https://youtrack.jetbrains.com/issue/AIR-5449))
- Alignment of messages is broken in chat ([AIR-5791](https://youtrack.jetbrains.com/issue/AIR-5791))
- Table rendering and scroll in chat output ([AIR-5045](https://youtrack.jetbrains.com/issue/AIR-5045))
- Thinking level switcher missing from UI ([AIR-5606](https://youtrack.jetbrains.com/issue/AIR-5606))
- Commits list not shown after Worktree plan implementation ([AIR-5240](https://youtrack.jetbrains.com/issue/AIR-5240))
- Commit message input missing in Diff view ([AIR-5101](https://youtrack.jetbrains.com/issue/AIR-5101))
- Edit and Revert buttons disappear on Diff view resize ([AIR-5319](https://youtrack.jetbrains.com/issue/AIR-5319))
- Application menu closes unexpectedly when moving mouse between options ([AIR-5639](https://youtrack.jetbrains.com/issue/AIR-5639))
- Tooltip flicker on hover ([AIR-5008](https://youtrack.jetbrains.com/issue/AIR-5008))
