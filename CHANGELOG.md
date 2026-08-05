# Changelog

## Sprint 262.132 — July–August 2026

**60 completed items** (3 features, 12 improvements, 45 fixes)

### Features (3)

- Context window and tokens display for Claude models ([AIR-5487](https://youtrack.jetbrains.com/issue/AIR-5487))
- Fast Mode support for Claude Opus via Anthropic API Billing ([AIR-4630](https://youtrack.jetbrains.com/issue/AIR-4630))
- Support Claude xhigh effort level (Fable, Opus, Sonnet 5) ([AIR-6205](https://youtrack.jetbrains.com/issue/AIR-6205))

### Improvements (12)

- Support env var interpolation in `.mcp.json` ([AIR-6583](https://youtrack.jetbrains.com/issue/AIR-6583))
- Add support for Gemini 3.6 Flash ([AIR-6444](https://youtrack.jetbrains.com/issue/AIR-6444))
- Add ability to see proposed diff in the Editor tab ([AIR-5476](https://youtrack.jetbrains.com/issue/AIR-5476))
- AI Quota widget in settings popup ([AIR-5846](https://youtrack.jetbrains.com/issue/AIR-5846))
- UX for preventing machine from sleeping during active tasks ([AIR-5191](https://youtrack.jetbrains.com/issue/AIR-5191))
- Codex agent mode now shows generated code output ([AIR-5287](https://youtrack.jetbrains.com/issue/AIR-5287))
- Fast Mode no longer locks when a Codex chat session starts ([AIR-5613](https://youtrack.jetbrains.com/issue/AIR-5613))
- `acp.json` shown as non-existing and empty file on first open ([AIR-6124](https://youtrack.jetbrains.com/issue/AIR-6124))
- Open in Web context actions added for Cloud tasks ([AIR-6080](https://youtrack.jetbrains.com/issue/AIR-6080))
- MCP Tool Call Widgets performance improved in WASM ([AIR-6332](https://youtrack.jetbrains.com/issue/AIR-6332))
- Update license texts on onboarding/login screens ([AIR-6217](https://youtrack.jetbrains.com/issue/AIR-6217))
- Chat file mentions show stale change count when file has no pending changes ([AIR-6160](https://youtrack.jetbrains.com/issue/AIR-6160))

### Fixes (45)

#### Authentication & Licensing

- Unable to log in using JetBrains account ([AIR-5465](https://youtrack.jetbrains.com/issue/AIR-5465))
- Air using Credits over API tokens ([AIR-6367](https://youtrack.jetbrains.com/issue/AIR-6367))

#### Junie

- Junie "Full Access" mode not working ([AIR-5380](https://youtrack.jetbrains.com/issue/AIR-5380))
- Junie: 407 Proxy Authentication Required — Failed to authenticate ([AIR-6349](https://youtrack.jetbrains.com/issue/AIR-6349))
- Junie does not answer — Failed to reset ingrazzio access with code error in log ([AIR-6207](https://youtrack.jetbrains.com/issue/AIR-6207))
- Junie cloud task started with Full Access switched to Ask mode ([AIR-6249](https://youtrack.jetbrains.com/issue/AIR-6249))

#### Codex & Agents

- Codex was asking for permissions in full access mode ([AIR-6010](https://youtrack.jetbrains.com/issue/AIR-6010))
- "Auto-open task changes" doesn't work for Codex ([AIR-6450](https://youtrack.jetbrains.com/issue/AIR-6450))
- Filter out custom agents for the docker task run ([AIR-6211](https://youtrack.jetbrains.com/issue/AIR-6211))
- Filter out agents for the cloud task run ([AIR-6210](https://youtrack.jetbrains.com/issue/AIR-6210))
- Docker agent task hangs indefinitely at "Copying agent resources to the agent volume" — no timeout, no error ([AIR-6440](https://youtrack.jetbrains.com/issue/AIR-6440))
- Claude is not aware of skills in `.agents/skills` ([AIR-6141](https://youtrack.jetbrains.com/issue/AIR-6141))

#### Claude & AI Models

- Claude Fable incorrectly showed 200K context window instead of 1M ([AIR-6065](https://youtrack.jetbrains.com/issue/AIR-6065))
- Claude compact summary & progress widget dropped (synthetic User events) ([AIR-6289](https://youtrack.jetbrains.com/issue/AIR-6289))
- Show fast mode toggle for OpenAI 5.6 models ([AIR-6389](https://youtrack.jetbrains.com/issue/AIR-6389))

#### MCP

- Error while using Copilot via ACP: attempted to query hidden partition ([AIR-6317](https://youtrack.jetbrains.com/issue/AIR-6317))
- ACP tool call shows tool ID instead of tool name ([AIR-5890](https://youtrack.jetbrains.com/issue/AIR-5890))
- MCP call panel is not horizontally scrollable ([AIR-5849](https://youtrack.jetbrains.com/issue/AIR-5849))
- MCP settings showed servers from all tasks ([AIR-5718](https://youtrack.jetbrains.com/issue/AIR-5718))

#### Tasks & Worktrees

- Resume for worktree tasks does not work — task disappears from list after resume attempt ([AIR-6250](https://youtrack.jetbrains.com/issue/AIR-6250))
- Can't stop a task — agent does nothing and stop button does not work ([AIR-5715](https://youtrack.jetbrains.com/issue/AIR-5715))

#### Multi-Root Workspace Isolation (15 fixes)

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
- AI Docs were saved to the wrong project root when created ([AIR-5750](https://youtrack.jetbrains.com/issue/AIR-5750))
- Local history restore picked the wrong repository in multi-root workspaces ([AIR-5741](https://youtrack.jetbrains.com/issue/AIR-5741))
- Settings showed all workspace roots for all tasks ([AIR-5719](https://youtrack.jetbrains.com/issue/AIR-5719))
- Fixed git status normalization worker ([AIR-5709](https://youtrack.jetbrains.com/issue/AIR-5709))

#### Windows

- Opening file from Explorer shows "Air Cannot Start: application_stop_event_loop already in progress" ([AIR-5478](https://youtrack.jetbrains.com/issue/AIR-5478))
- Drag and Drop not supported on Windows ([AIR-5138](https://youtrack.jetbrains.com/issue/AIR-5138))
- Can't run custom ACP agent — `%1 is not a valid Win32 application` ([AIR-5759](https://youtrack.jetbrains.com/issue/AIR-5759))
- Air can't open chat and tasks panel on Windows ([AIR-5761](https://youtrack.jetbrains.com/issue/AIR-5761))

#### UI & Chat

- Alignment of messages is broken in chat ([AIR-5791](https://youtrack.jetbrains.com/issue/AIR-5791))
- Table UI and scroll behavior in chat output ([AIR-5045](https://youtrack.jetbrains.com/issue/AIR-5045))
- Chat banners' width does not support the full width ([AIR-5530](https://youtrack.jetbrains.com/issue/AIR-5530))
- Clear command doesn't work ([AIR-5599](https://youtrack.jetbrains.com/issue/AIR-5599))
- Crash (IndexOutOfBoundsException) when typing in "Add To Task Context" menu ([AIR-6121](https://youtrack.jetbrains.com/issue/AIR-6121))

---

*Produced by Air Automation. Name: Generate Release Notes / Run: https://air.stgn.jetbrains.cloud/org/05cf1a7f-6ab5-713b-abd3-29d0c8a05e2d/automations/700dc751-f867-4758-aa14-92fd8704e23d?run=236ff0eb-952a-4662-91ac-8d0e2567df00*
