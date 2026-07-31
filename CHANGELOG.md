# Changelog

## Sprint 262.132 — July 2026

> **59 completed items** · 6 features · 9 improvements · 44 fixes
>
> Source: [YouTrack AIR project, fix version 262.132](https://youtrack.jetbrains.com/issues/AIR?q=Fix+versions%3A+262.132+%23Resolved)

---

### Features

- **Context window and tokens display for Claude models** ([AIR-5487](https://youtrack.jetbrains.com/issue/AIR-5487)) — Real-time context usage and token count are now visible in the Claude model UI
- **Fast Mode support for Claude Opus via Anthropic API Billing** ([AIR-4630](https://youtrack.jetbrains.com/issue/AIR-4630))
- **Support `xhigh` effort level for Claude** ([AIR-6205](https://youtrack.jetbrains.com/issue/AIR-6205)) — Available for Fable, Opus, and Sonnet 5
- **Gemini 3.6 Flash support** ([AIR-6444](https://youtrack.jetbrains.com/issue/AIR-6444))
- **View proposed diff in the Editor tab** ([AIR-5476](https://youtrack.jetbrains.com/issue/AIR-5476)) — Agent-proposed changes can now be reviewed directly in the editor
- **Environment variable interpolation in `.mcp.json`** ([AIR-6583](https://youtrack.jetbrains.com/issue/AIR-6583))

---

### Improvements

- **UX for preventing machine from sleeping during active tasks** ([AIR-5191](https://youtrack.jetbrains.com/issue/AIR-5191))
- **Codex agent mode now shows generated code output** ([AIR-5287](https://youtrack.jetbrains.com/issue/AIR-5287))
- **Fast Mode no longer locks when a Codex chat session starts** ([AIR-5613](https://youtrack.jetbrains.com/issue/AIR-5613))
- **`acp.json` no longer shown as non-existing or empty on first open** ([AIR-6124](https://youtrack.jetbrains.com/issue/AIR-6124))
- **Open in Web context actions added for Cloud tasks** ([AIR-6080](https://youtrack.jetbrains.com/issue/AIR-6080))
- **Chat file mentions now show an accurate change count** ([AIR-6160](https://youtrack.jetbrains.com/issue/AIR-6160))
- **AI Quota widget in settings popup** ([AIR-5846](https://youtrack.jetbrains.com/issue/AIR-5846))
- **Fast mode toggle shown for OpenAI 5.6 models** ([AIR-6389](https://youtrack.jetbrains.com/issue/AIR-6389))
- **Updated license texts on onboarding and login screens** ([AIR-6217](https://youtrack.jetbrains.com/issue/AIR-6217))

---

### Fixes

#### AI Models & Claude

- Claude is not aware of skills in `.agents/skills` ([AIR-6141](https://youtrack.jetbrains.com/issue/AIR-6141))
- Junie "Full Access" mode not working ([AIR-5380](https://youtrack.jetbrains.com/issue/AIR-5380))
- Claude Fable incorrectly showed 200K context window instead of 1M ([AIR-6065](https://youtrack.jetbrains.com/issue/AIR-6065))
- Codex asking for permissions in Full Access mode ([AIR-6010](https://youtrack.jetbrains.com/issue/AIR-6010))
- `java.lang.IndexOutOfBoundsException` crash ([AIR-6121](https://youtrack.jetbrains.com/issue/AIR-6121))

#### Agent & Task Reliability

- Resume for worktree tasks does not work — task disappeared from list after resume attempt ([AIR-6250](https://youtrack.jetbrains.com/issue/AIR-6250))
- Cannot stop a task; stop button does nothing ([AIR-5715](https://youtrack.jetbrains.com/issue/AIR-5715))
- Docker agent task hangs indefinitely at "Copying agent resources to the agent volume" ([AIR-6440](https://youtrack.jetbrains.com/issue/AIR-6440))
- Claude compact summary & progress widget dropped from context ([AIR-6289](https://youtrack.jetbrains.com/issue/AIR-6289))
- "Auto-open task changes" does not work for Codex ([AIR-6450](https://youtrack.jetbrains.com/issue/AIR-6450))
- Air using Credits over API tokens incorrectly ([AIR-6367](https://youtrack.jetbrains.com/issue/AIR-6367))
- Custom agents incorrectly shown in Docker task run context ([AIR-6211](https://youtrack.jetbrains.com/issue/AIR-6211))
- Agents incorrectly shown in Cloud task run context ([AIR-6210](https://youtrack.jetbrains.com/issue/AIR-6210))

#### Multi-Root Workspace Isolation (15 fixes)

All 15 fixes address task-isolation regressions in multi-root workspace setups:

- Text search searched across all tasks instead of the current one ([AIR-5716](https://youtrack.jetbrains.com/issue/AIR-5716))
- MCP settings showed servers from all tasks ([AIR-5718](https://youtrack.jetbrains.com/issue/AIR-5718))
- Settings showed workspace roots from all tasks ([AIR-5719](https://youtrack.jetbrains.com/issue/AIR-5719))
- File mentions were provided by all tasks ([AIR-5721](https://youtrack.jetbrains.com/issue/AIR-5721))
- Commands, skills, and subagents were provided from all tasks ([AIR-5723](https://youtrack.jetbrains.com/issue/AIR-5723))
- Wrong file root shown in "New Task" screen ([AIR-5724](https://youtrack.jetbrains.com/issue/AIR-5724))
- Diff and Changes tools now support multi-repo scenarios ([AIR-5725](https://youtrack.jetbrains.com/issue/AIR-5725))
- Repo selector in History showed repos from all tasks ([AIR-5726](https://youtrack.jetbrains.com/issue/AIR-5726))
- Git-related actions (review changes, commit message, etc.) now use the current task's repository ([AIR-5727](https://youtrack.jetbrains.com/issue/AIR-5727))
- Git header showed all repos from all tasks and could show wrong current branch ([AIR-5728](https://youtrack.jetbrains.com/issue/AIR-5728))
- Chat mentions showed branches/commits from all tasks ([AIR-5729](https://youtrack.jetbrains.com/issue/AIR-5729))
- Agent requirements check (repo, unmerged files, AGENTS.md) now uses current task only ([AIR-5730](https://youtrack.jetbrains.com/issue/AIR-5730))
- Changes and Diff tools showed files from all tasks ([AIR-5731](https://youtrack.jetbrains.com/issue/AIR-5731))
- Local history restore picked the wrong repository in multi-root workspaces ([AIR-5741](https://youtrack.jetbrains.com/issue/AIR-5741))
- AI Docs were saved to the wrong project root when created ([AIR-5750](https://youtrack.jetbrains.com/issue/AIR-5750))

#### ACP & MCP

- Error using Copilot via ACP: attempted to query hidden partition ([AIR-6317](https://youtrack.jetbrains.com/issue/AIR-6317))
- ACP tool call showed raw tool ID instead of a human-readable name ([AIR-5890](https://youtrack.jetbrains.com/issue/AIR-5890))
- MCP call panel was not horizontally scrollable ([AIR-5849](https://youtrack.jetbrains.com/issue/AIR-5849))
- MCP Tool Call Widgets performed poorly in WASM ([AIR-6332](https://youtrack.jetbrains.com/issue/AIR-6332))
- Clear command did not work ([AIR-5599](https://youtrack.jetbrains.com/issue/AIR-5599))

#### Authentication

- Unable to log in using JetBrains account ([AIR-5465](https://youtrack.jetbrains.com/issue/AIR-5465))

#### Windows

- Opening a file from Explorer crashed with "Air Cannot Start: application_stop_event_loop already in progress" ([AIR-5478](https://youtrack.jetbrains.com/issue/AIR-5478))
- Drag and Drop not supported on Windows ([AIR-5138](https://youtrack.jetbrains.com/issue/AIR-5138))
- Custom ACP agent could not run on Windows: `%1 is not a valid Win32 application` ([AIR-5759](https://youtrack.jetbrains.com/issue/AIR-5759))
- Air could not open the chat and tasks panel on Windows ([AIR-5761](https://youtrack.jetbrains.com/issue/AIR-5761))

#### Chat & UI

- Message alignment broken in chat ([AIR-5791](https://youtrack.jetbrains.com/issue/AIR-5791))
- Table UI and scroll behavior issues in chat output ([AIR-5045](https://youtrack.jetbrains.com/issue/AIR-5045))
- Chat banners did not span the full panel width ([AIR-5530](https://youtrack.jetbrains.com/issue/AIR-5530))

#### Internals

- Re-implemented `normalizeGitStatuses` worker ([AIR-5709](https://youtrack.jetbrains.com/issue/AIR-5709))

---

*Produced by Air Automation. Name: Generate Release Notes / Run: https://air.stgn.jetbrains.cloud/org/05cf1a7f-6ab5-713b-abd3-29d0c8a05e2d/automations/a0af7518-ccd0-47fe-b6bb-0429febfee9d?run=3a9f1fa7-9bf4-4e1f-b736-d59286a7c476*
