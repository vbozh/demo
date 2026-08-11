# Changelog

## Sprint 262.132 — July 2026

**42 completed items** · 3 features · 6 improvements · 33 fixes

---

### Features

- Context window and tokens display for Claude models ([AIR-5487](https://youtrack.jetbrains.com/issue/AIR-5487))
- Fast Mode support for Claude Opus via Anthropic API Billing ([AIR-4630](https://youtrack.jetbrains.com/issue/AIR-4630))
- Support Claude xhigh effort level (Fable, Opus, Sonnet 5) ([AIR-6205](https://youtrack.jetbrains.com/issue/AIR-6205))

### Improvements

- UX for preventing machine from sleeping during active tasks ([AIR-5191](https://youtrack.jetbrains.com/issue/AIR-5191))
- Codex agent mode now shows generated code output ([AIR-5287](https://youtrack.jetbrains.com/issue/AIR-5287))
- Fast Mode no longer locks when a Codex chat session starts ([AIR-5613](https://youtrack.jetbrains.com/issue/AIR-5613))
- `acp.json` shown as non-existing and empty file on first open ([AIR-6124](https://youtrack.jetbrains.com/issue/AIR-6124))
- Open in Web context actions added for Cloud tasks ([AIR-6080](https://youtrack.jetbrains.com/issue/AIR-6080))
- Chat file mentions show stale change count when file has no pending changes ([AIR-6160](https://youtrack.jetbrains.com/issue/AIR-6160))

### Fixes

**Crash & Stability**
- Crash (IndexOutOfBoundsException) when typing in "Add To Task Context" menu ([AIR-6121](https://youtrack.jetbrains.com/issue/AIR-6121))
- [Windows] Opening file from Explorer shows "Air Cannot Start: application_stop_event_loop already in progress" ([AIR-5478](https://youtrack.jetbrains.com/issue/AIR-5478))

**Authentication**
- Unable to log in using JetBrains account ([AIR-5465](https://youtrack.jetbrains.com/issue/AIR-5465))

**Tasks & Agents**
- Resume for worktree tasks does not work — task disappears from list after resume attempt ([AIR-6250](https://youtrack.jetbrains.com/issue/AIR-6250))
- Can't stop a task — agent does nothing and stop button does not work ([AIR-5715](https://youtrack.jetbrains.com/issue/AIR-5715))
- Junie "Full Access" mode not working ([AIR-5380](https://youtrack.jetbrains.com/issue/AIR-5380))
- OpenCode via acp.json does not answer ([AIR-6226](https://youtrack.jetbrains.com/issue/AIR-6226))

**AI Models & Skills**
- Claude Fable incorrectly showed 200K context window instead of 1M ([AIR-6065](https://youtrack.jetbrains.com/issue/AIR-6065))
- Claude is not aware of skills in `.agents/skills` ([AIR-6141](https://youtrack.jetbrains.com/issue/AIR-6141))
- Codex was asking for permissions in full access mode ([AIR-6010](https://youtrack.jetbrains.com/issue/AIR-6010))

**Multi-Root Workspace** (task-isolation fixes)
- Text search scoped incorrectly across workspace roots ([AIR-5716](https://youtrack.jetbrains.com/issue/AIR-5716))
- File mentions not isolated to the active root ([AIR-5718](https://youtrack.jetbrains.com/issue/AIR-5718))
- Commands/skills/subagents leaking across roots ([AIR-5719](https://youtrack.jetbrains.com/issue/AIR-5719))
- Diff/Changes tools operating on wrong root ([AIR-5721](https://youtrack.jetbrains.com/issue/AIR-5721))
- Repo selector not respecting active root ([AIR-5723](https://youtrack.jetbrains.com/issue/AIR-5723))
- Git actions/header showing wrong root ([AIR-5724](https://youtrack.jetbrains.com/issue/AIR-5724))
- Chat mentions not scoped to active root ([AIR-5725](https://youtrack.jetbrains.com/issue/AIR-5725))
- Agent requirements check using wrong root ([AIR-5726](https://youtrack.jetbrains.com/issue/AIR-5726))
- MCP settings not isolated per root ([AIR-5727](https://youtrack.jetbrains.com/issue/AIR-5727))
- Workspace roots list incorrect ([AIR-5728](https://youtrack.jetbrains.com/issue/AIR-5728))
- AI Docs not scoped to active root ([AIR-5729](https://youtrack.jetbrains.com/issue/AIR-5729))
- Local history restore using wrong root ([AIR-5730](https://youtrack.jetbrains.com/issue/AIR-5730))
- New Task screen file root not set correctly ([AIR-5731](https://youtrack.jetbrains.com/issue/AIR-5731))
- Additional multi-root workspace isolation fix ([AIR-5741](https://youtrack.jetbrains.com/issue/AIR-5741))
- Additional multi-root workspace isolation fix ([AIR-5750](https://youtrack.jetbrains.com/issue/AIR-5750))

**Windows**
- Air can't open chat and tasks panel on Windows ([AIR-5761](https://youtrack.jetbrains.com/issue/AIR-5761))
- [Windows] Drag and Drop not supported ([AIR-5138](https://youtrack.jetbrains.com/issue/AIR-5138))
- [Windows] Can't run custom acp agent — `%1 is not a valid Win32 application` ([AIR-5759](https://youtrack.jetbrains.com/issue/AIR-5759))

**UI & Chat**
- Alignment of messages is broken in chat ([AIR-5791](https://youtrack.jetbrains.com/issue/AIR-5791))
- Table UI and scroll behavior in chat output ([AIR-5045](https://youtrack.jetbrains.com/issue/AIR-5045))
- MCP call panel not horizontally scrollable ([AIR-5849](https://youtrack.jetbrains.com/issue/AIR-5849))
- Chat banners did not span the full panel width ([AIR-5530](https://youtrack.jetbrains.com/issue/AIR-5530))
- Git status normalization worker running incorrectly ([AIR-5709](https://youtrack.jetbrains.com/issue/AIR-5709))

---

## Sprint 262.43 — June 2026

**43 completed items** · 4 features · 6 improvements · 33 fixes

---

### Features

- Open in IDE (IntelliJ-family) for local project & changes ([AIR-3687](https://youtrack.jetbrains.com/issue/AIR-3687))
- Windows support ([AIR-4132](https://youtrack.jetbrains.com/issue/AIR-4132))
- Linux Wayland: IME support in editor ([AIR-5610](https://youtrack.jetbrains.com/issue/AIR-5610))
- Linux X11: IME support in editor ([AIR-5611](https://youtrack.jetbrains.com/issue/AIR-5611))

### Improvements

- [Windows] Native-style buttons in update dialog ([AIR-5755](https://youtrack.jetbrains.com/issue/AIR-5755))
- [Windows] Native caption buttons drawn with Compose ([AIR-5600](https://youtrack.jetbrains.com/issue/AIR-5600))
- [Windows] Font rendering quality in editor ([AIR-4755](https://youtrack.jetbrains.com/issue/AIR-4755))
- [Windows] Air icon alignment on main toolbar ([AIR-5608](https://youtrack.jetbrains.com/issue/AIR-5608))
- Update Slash menu ([AIR-5208](https://youtrack.jetbrains.com/issue/AIR-5208))
- Terminal commands shown as code snippets in archived tasks ([AIR-3335](https://youtrack.jetbrains.com/issue/AIR-3335))

### Fixes

**Critical / Show-stopper**
- Tasks and changes not loading after 262.34 update ([AIR-5640](https://youtrack.jetbrains.com/issue/AIR-5640))
- Chat messages invisible until task is stopped ([AIR-5583](https://youtrack.jetbrains.com/issue/AIR-5583))
- Search / indexing regression ([AIR-5670](https://youtrack.jetbrains.com/issue/AIR-5670))

**Startup**
- Air fails to start / cannot start after Toolbox update ([AIR-5645](https://youtrack.jetbrains.com/issue/AIR-5645))

**Performance**
- Slow performance regression ([AIR-5812](https://youtrack.jetbrains.com/issue/AIR-5812))
- Another performance issue ([AIR-5233](https://youtrack.jetbrains.com/issue/AIR-5233))

**Windows**
- Windows-specific display issue ([AIR-5760](https://youtrack.jetbrains.com/issue/AIR-5760))
- [Windows] Copy does not work ([AIR-5558](https://youtrack.jetbrains.com/issue/AIR-5558))
- [Windows] UI rendering issue ([AIR-5316](https://youtrack.jetbrains.com/issue/AIR-5316))
- [Windows] Can't run custom acp agent — `%1 is not a valid Win32 application` ([AIR-5759](https://youtrack.jetbrains.com/issue/AIR-5759))
- [Windows] Taskbar/window issue ([AIR-5738](https://youtrack.jetbrains.com/issue/AIR-5738))
- [Windows] UI styling issue ([AIR-5385](https://youtrack.jetbrains.com/issue/AIR-5385))

**Linux**
- Linux-specific rendering issue ([AIR-5571](https://youtrack.jetbrains.com/issue/AIR-5571))

**Agents & Tasks**
- Agent stopping unexpectedly ([AIR-5570](https://youtrack.jetbrains.com/issue/AIR-5570))
- Agent permission issue ([AIR-5565](https://youtrack.jetbrains.com/issue/AIR-5565))
- Agent context issue ([AIR-5525](https://youtrack.jetbrains.com/issue/AIR-5525))
- Uncommitted changes lost on Implement in Worktree agent ([AIR-5484](https://youtrack.jetbrains.com/issue/AIR-5484))
- Uncommitted changes lost on Implement in Docker agent ([AIR-5538](https://youtrack.jetbrains.com/issue/AIR-5538))
- Agent behavior issue ([AIR-4270](https://youtrack.jetbrains.com/issue/AIR-4270))
- Agent UI issue ([AIR-5857](https://youtrack.jetbrains.com/issue/AIR-5857))
- Gemini asks permission for AskUserQuestion tool ([AIR-4606](https://youtrack.jetbrains.com/issue/AIR-4606))

**UI & Chat**
- Alignment of messages is broken in chat ([AIR-5791](https://youtrack.jetbrains.com/issue/AIR-5791))
- Table rendering and scroll in Chat output ([AIR-5045](https://youtrack.jetbrains.com/issue/AIR-5045))
- Junie approval view shows no content ([AIR-4794](https://youtrack.jetbrains.com/issue/AIR-4794))
- Thinking level switcher missing from UI ([AIR-5606](https://youtrack.jetbrains.com/issue/AIR-5606))
- Chat display regression ([AIR-5639](https://youtrack.jetbrains.com/issue/AIR-5639))
- Tooltip flicker on hover ([AIR-5008](https://youtrack.jetbrains.com/issue/AIR-5008))

**Editor**
- Can't open files linked in agent markdown plans ([AIR-5449](https://youtrack.jetbrains.com/issue/AIR-5449))
- Editor scroll/display issue ([AIR-4097](https://youtrack.jetbrains.com/issue/AIR-4097))
- Commits list not shown after Worktree plan implementation ([AIR-5240](https://youtrack.jetbrains.com/issue/AIR-5240))
- Commit message input missing in Diff view ([AIR-5101](https://youtrack.jetbrains.com/issue/AIR-5101))
- Edit and Revert buttons disappear on Diff view resize ([AIR-5319](https://youtrack.jetbrains.com/issue/AIR-5319))

**Authentication**
- Unable to log in using JetBrains account ([AIR-5465](https://youtrack.jetbrains.com/issue/AIR-5465))

---

*Produced by Air Automation. Name: Generate Release Notes / Run: https://air.stgn.jetbrains.cloud/org/05cf1a7f-6ab5-713b-abd3-29d0c8a05e2d/automations/700dc751-f867-4758-aa14-92fd8704e23d?run=0b3c5f7c-65b9-4412-8d0e-6244e02a6cbc*
