# Changelog

## Sprint 262.132 — Released 2026-07-31

### Features

New capabilities added this sprint.

- **Claude xhigh effort level support** (AIR-6205) — The `xhigh` reasoning effort level is now available for Claude Fable, Opus, and Sonnet 5 models.
- **Context window and token display for Claude** (AIR-5487) — The Claude panel now shows the current context window size and token consumption.
- **Fast Mode for Claude Opus** (AIR-4630) — Fast Mode is now supported for Claude Opus under Anthropic API billing.
- **Gemini 3.6 Flash model support** (AIR-6444) — Gemini 3.6 Flash is now available as a model option.
- **Env var interpolation in `.mcp.json`** (AIR-6583) — Air now substitutes `${VAR}` placeholders in `.mcp.json` from the environment, so MCP servers that authenticate via token placeholders work correctly without hardcoding secrets.
- **Open in Web context actions for Cloud tasks** (AIR-6080) — Cloud task entries now include "Open in Web" context actions to jump directly to the task in the browser.
- **AI Quota widget in settings popup** (AIR-5846) — A new quota indicator in the settings popup shows remaining AI quota at a glance.
- **Proposed diff view in Editor tab** (AIR-5476) — Users can now view agent-proposed diffs directly in the Editor tab before applying them.
- **Prevent machine from sleeping during tasks** (AIR-5191) — Air now keeps the machine awake while a task is running to prevent interrupted agent sessions.

---

### Improvements

Enhancements and usability refinements to existing functionality.

- **Multi-root workspace isolation** (AIR-5502 and related) — A comprehensive set of fixes ensures that all task-scoped surfaces (file mentions, Git headers, MCP settings, text search, chat history, commands, skills, subagents, agent requirement checks) are isolated to the current task's workspace root rather than leaking data across all open tasks. Affects AIR-5716, AIR-5718, AIR-5719, AIR-5721, AIR-5722, AIR-5723, AIR-5724, AIR-5725, AIR-5726, AIR-5727, AIR-5728, AIR-5729, AIR-5730, AIR-5731, AIR-5741, AIR-5750.
- **Codex shows generated code in agent mode** (AIR-5287) — Code produced by Codex in agent mode is now rendered in the chat output.
- **File change visibility from chat mentions** (AIR-6160) — Opening a file from a chat mention that references changes now opens the file at the correct changed state.
- **`acp.json` first-open experience** (AIR-6124) — `acp.json` is no longer shown as missing or empty on its first open.
- **Updated license texts** (AIR-6217) — License text on the onboarding and login screens has been updated.
- **Fast mode lock fixed after Codex chat starts** (AIR-5613) — The Fast mode toggle is no longer locked when a Codex chat session is active.

---

### Bug Fixes

#### Critical & Show-stopper

- **Worktree task resume** (AIR-6250, Show-stopper) — Resuming a worktree task no longer causes it to disappear from the task list.
- **Docker agent task hang** (AIR-6440, Critical) — Docker agent tasks no longer hang indefinitely at "Copying agent resources to the agent volume"; a timeout now terminates and reports the failure.
- **MCP Tool Call Widget performance in WASM** (AIR-6332, Critical) — Significant performance regression in MCP Tool Call Widgets under WASM has been resolved.
- **Windows: "Air Cannot Start" crash on file open** (AIR-5478, Critical) — Opening a file from Windows Explorer no longer triggers an application shutdown loop crash.
- **Windows: Chat and tasks panel inaccessible** (AIR-5761, Critical) — Air can now reliably open the chat and tasks panel on Windows.
- **Junie "Full Access" mode not working** (AIR-5380, Critical) — Junie's Full Access permission mode now functions correctly.
- **OpenCode via `acp.json` not responding** (AIR-6226, Critical) — OpenCode configured via `acp.json` now responds to queries.

#### Agent & Model Integration

- **Air using AI credits instead of configured API token** (AIR-6367) — Air now correctly routes requests through the user-configured Anthropic API token rather than JetBrains AI credits.
- **Fast mode toggle missing for OpenAI 5.6 models** (AIR-6389) — The Fast mode toggle is now shown for OpenAI 5.6 models.
- **Claude Fable incorrect context window size** (AIR-6065) — Claude Fable now reports its actual 1M context window instead of 200K.
- **Claude compact summary progress widget dropped** (AIR-6289) — The compact summary and progress widget is no longer dropped when synthetic User events are present.
- **Claude unaware of skills in `.agents/skills`** (AIR-6141) — Claude now correctly loads and uses skills defined in the `.agents/skills` directory.
- **Auto-open task changes not working for Codex** (AIR-6450) — The "Auto-open task changes" setting now applies to Codex tasks.
- **Codex asking for permissions in Full Access mode** (AIR-6010) — Codex no longer requests redundant permissions when Full Access mode is active.
- **Junie ignores permission level** (AIR-5722) — Junie now respects the configured permission level.
- **Custom agents shown for Docker/cloud task runs** (AIR-6211, AIR-6210) — Custom agents are now correctly filtered out from Docker and cloud task run model selectors.
- **ACP tool calls showing raw tool IDs** (AIR-5890) — ACP tool call widgets now display readable tool names instead of raw tool IDs.
- **Copilot via ACP hidden partition error** (AIR-6317) — Resolved an error ("attempted to query hidden partition") that occurred when using Copilot through ACP.

#### Windows

- **Drag and drop not supported on Windows** (AIR-5138) — Drag and drop file interactions now work on Windows.
- **Custom ACP agent not running on Windows** (AIR-5759) — Fixed `%1 is not a valid Win32 application` error when running a custom ACP agent on Windows.

#### Task Management

- **Task stop button unresponsive** (AIR-5715) — The stop button for running tasks now reliably terminates the agent.

#### UI & Chat

- **Table UI and scroll behavior in Chat** (AIR-5045) — Table rendering and scrolling in chat output has been corrected.
- **Message alignment broken in chat** (AIR-5791) — Chat message alignment is now consistent.
- **Chat banners not expanding to full width** (AIR-5530) — Chat banners now use the full available width.
- **MCP call panel not horizontally scrollable** (AIR-5849) — The MCP call panel can now be scrolled horizontally for wide content.

#### Other

- **Login with JetBrains credentials** (AIR-5465) — Fixed an issue preventing login via JetBrains account.
- **Terminal clear command not working** (AIR-5599) — The `clear` command in the integrated terminal now works correctly.
- **IndexOutOfBoundsException in Add To Task Context menu** (AIR-6121) — Fixed a crash triggered by typing in the Add To Task Context menu.
- **`normalizeGitStatuses` worker re-implemented** (AIR-5709) — Underlying Git status normalization worker has been rewritten for correctness and reliability.

---

*Produced by Air Automation. Name: Generate Release Notes / Run: [c15dfc7d](https://air.stgn.jetbrains.cloud/org/05cf1a7f-6ab5-713b-abd3-29d0c8a05e2d/automations/700dc751-f867-4758-aa14-92fd8704e23d?run=c15dfc7d-851c-4338-bc6a-91fd64b2345c)*
