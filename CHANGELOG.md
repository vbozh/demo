# Changelog

## Sprint — July 20–August 3, 2026

> **37 issues resolved** across features, fixes, and improvements.
> Shipped in builds **262.132** (stable) and **Next** (upcoming release).

---

### Features

- **Windows IME / CJK input support** (AIR-25-7594121) — Chinese, Korean, and other CJK
  input methods now work on Windows. This was a critical gap for Windows users where IME
  composition was fully non-functional.

- **Collect Junie logs with Air logs** (AIR-25-8313522) — The "Collect Logs" action now
  bundles Junie logs (from `~/.junie/logs` on macOS/Linux and `$HOME\.junie\logs` on
  Windows) alongside Air logs, making issue debugging significantly easier.

- **Copyable links via right-click** (AIR-25-8267809) — Right-clicking on any hyperlink in
  the UI now shows a context menu option to copy the URL.

---

### Fixes

#### Agent & Task Reliability

- **Agent not responding to prompts** (AIR-25-8012066) — Fixed a regression in build
  262.43.32 where the AI agent silently stalled without any error or retry indication.

- **Tasks stuck in "waiting for user input"** (AIR-25-8271142, AIR-25-8074451) — Fixed two
  related issues where tasks displayed a "waiting for user input" state but showed no prompt
  and could not be interacted with. Affected long-running tasks with Fable 5.

- **Hard execution timeouts applied to permission prompts** (AIR-25-7764064) — Air was
  timing out user-facing "approve this action?" prompts the same way it timed out regular
  tool calls. Timeouts for interactive prompts are now indefinite.

- **Codex agent showed no progress feedback** (AIR-25-7968687) — During planning and
  execution, Codex could enter a stuck-looking "running" state with no activity indicator.
  Users now receive visual feedback while the agent works.

- **Tasks hanging after Air Desktop update** (AIR-25-7786503) — Resolved an issue where
  many tasks hung indefinitely after updating Air Desktop on macOS (build 261.681.18).

- **ACP communication issues with opencode** (AIR-25-8282013) — Fixed two bugs in ACP
  communication: `air_add_comment` calls were not being applied to the task, and Air
  sometimes rendered a blank white screen instead of task content.

- **Repeated task failures after initial success** (AIR-25-7643852) — Improved agent
  reliability for consecutive tasks; previously the first task succeeded but subsequent
  attempts failed consistently.

#### Junie / Permission Modes

- **407 Proxy Authentication Required** (AIR-25-8135229) — Fixed a critical authentication
  failure (`ExitEarly: Junie: 407 Proxy Authentication Required`) caused by proxy auth
  issues during token reset via Ingrazzio. Released in build 262.132.

- **Cloud tasks ignoring Full Access permission mode** (AIR-25-8053900) — When triggering
  a cloud task with Junie set to Full Access, the mode was silently downgraded to Ask mode.
  Root cause: Junie's `brave_mode` config was not mapped correctly in the cloud task path.
  Automations were also affected.

- **Web-triggered tasks ignoring `full-access` mode** (AIR-25-8098157) — Web-triggered
  Junie tasks now correctly honour the `full-access` permission mode by sending
  `brave_mode: true`.

- **Full Access permission indicator shown in green** (AIR-25-8197797) — The "Full Access"
  mode indicator was using green (safe-looking) color. It now uses red to signal elevated
  permissions.

#### Input Methods (IME)

- **IME composed text not committed on focus change** (AIR-25-8310931) — On macOS, moving
  focus between fields while IME composition was active left text in an inconsistent state.
  Composed text is now correctly committed or discarded on focus change.

- **Japanese characters not fully enterable in comment field** (AIR-25-7746938) — Fixed
  broken Japanese IME input in the comment field on macOS.

- **Japanese IME: intermediate text disappeared without spacebar** (AIR-25-7746948) — Fixed
  an issue where Japanese composition segments were dropped when typing without the
  spacebar before moving to the next word.

#### Chat & UI

- **No response shown in chat** (AIR-25-8132960) — After upgrading, users saw their own
  messages but no agent responses were displayed. The agent was running silently in the
  background. Fixed in build 262.132.21.

- **Chat scrolling at 1–2 FPS** (AIR-25-7748962) — Resolved severe scrolling lag in long
  chat conversations (5+ screen heights).

- **Mentions in table cells caused exceptions** (AIR-25-8315933) — Placing mentions inside
  table cells triggered layout exceptions due to a conflict between table intrinsic
  measurement and SubcomposeLayout. Fixed by prohibiting intrinsic measurement of lazy
  components.

- **Tool use not rendered in Junie** (AIR-25-7931165) — Junie's tool calls were invisible
  in the chat view, making conversations appear as disconnected messages. Tool invocations
  are now rendered inline.

- **Diff view showing "Diff is not renderable"** (AIR-25-8151145) — In cloud task
  environments, the diff viewer incorrectly reported files as non-renderable. Fixed the
  baseline diffing logic to account for cloud tasks auto-committing all changes.

- **Blur effect missing on tasks panel** (AIR-25-8362332) — The tasks panel hover overlay
  was missing its background blur effect.

- **GitHub PR link shown in task header** (AIR-25-8222725) — Task headers now display the
  GitHub PR link with current PR status in place of the previous "Create PR" button.

- **Exception when toggling UI panels** (AIR-25-7979031) — Switching from Claude agent to
  local tasks triggered a `java.util.NoSuchElementException` when building action
  presentations for Toggle Tasks Panel, Toggle Tool Panel, and related UI actions.

#### Files & Editor

- **Temp files lost on Air restart** (AIR-25-7825628) — Critical fix: temp files are now
  persisted and restored after an Air restart or update. Previously, temp files were lost
  on every restart.

- **Temp file creation ignored selected project root** (AIR-25-8309672) — In multi-project
  windows, new temp files are now assigned to the active project root instead of a default
  one.

- **Repository opened in a new window after Git clone** (AIR-25-8221252) — Cloning a repo
  from the Git main menu now opens it in the current Air window, not a new one.

- **Word not selected on right-click** (AIR-25-8267791) — Right-clicking on a word in the
  editor now selects it, matching native macOS behavior.

- **Cannot create file by path** (AIR-25-8272809) — Fixed a failure when creating files
  using an explicit file path.

#### Platform / Startup

- **Infinite "initializing JCEF" and "preparing ruff" on Linux** (AIR-25-8123867) — Fixed
  infinite startup status messages on Linux (build 262.43.32). Air no longer prompts to
  initialize a git repo when one already exists.

---

### Improvements

- **Env var interpolation in `.mcp.json`** (AIR-25-8288732) — Air now substitutes
  `${VAR}` environment variable placeholders in `.mcp.json` at load time. MCP servers
  relying on token-based auth (e.g. `"Authorization": "Bearer ${YOUTRACK_MCP_TOKEN}"`) now
  work correctly. Released in build 262.132.

- **Custom ACP agents in the cloud** (AIR-25-8210085) — Custom ACP (Agent Communication
  Protocol) agents can now run in the cloud environment. A predefined agent ID initializes
  an ACP agent from an environment variable or `acp.json` file, controllable via
  `startup-config`.

- **Updated Agent Review action UI** (AIR-25-7862620) — Redesigned UI controls for the
  Agent Review action per updated Figma mockups. Developers can now clearly see and choose
  which agent and model is used for review.

- **DataSource API and RhizomeDB integration updated** (AIR-25-7974415) — Compose
  multiplatform core's DataSource API and RhizomeDB integration updated to match the latest
  production shape after significant divergence.

- **Forbid intrinsic measurement of lazy Compose components** (AIR-25-8036283) — Architectural
  enforcement preventing `SubcomposeLayout`-based components from being measured
  intrinsically, eliminating a class of layout exceptions (including the table mentions bug).

---

*Produced by Air Automation. Name: Generate Release Notes / Run: https://air.stgn.jetbrains.cloud/org/05cf1a7f-6ab5-713b-abd3-29d0c8a05e2d/automations/700dc751-f867-4758-aa14-92fd8704e23d?run=1ac31964-d124-4bed-a2c6-4ec1e5985665*
