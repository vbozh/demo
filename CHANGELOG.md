# Changelog

## Sprint: July 7 – 26, 2026

### Features

- **Allow defining what JetBrains subscription should be used** ([AIR-7755847](https://youtrack.jetbrains.com/issue/AIR-7755847))
  Users can now choose which JetBrains subscription is used within Air, giving more control over licensing and billing.

- **More per-task information** ([AIR-8050403](https://youtrack.jetbrains.com/issue/AIR-8050403))
  Task details now surface the model used, credits consumed, and execution time per task for better visibility into AI usage.

- **Add support for Gemini 3.6 Flash** ([AIR-8200586](https://youtrack.jetbrains.com/issue/AIR-8200586))
  Gemini 3.6 Flash is now available as an AI model option.

- **Support Claude xhigh effort level (Fable, Opus, Sonnet 5)** ([AIR-8035645](https://youtrack.jetbrains.com/issue/AIR-8035645))
  The `xhigh` reasoning effort level is now supported for Claude Fable, Opus, and Sonnet 5 models.

---

### Fixes

- **Manage Repositories reloads the Air Web onboarding page without navigating** ([AIR-8226415](https://youtrack.jetbrains.com/issue/AIR-8226415))
  Fixed a navigation bug where opening Manage Repositories triggered an unexpected reload of the onboarding screen.

- **Custom notifications sound** ([AIR-7377331](https://youtrack.jetbrains.com/issue/AIR-7377331))
  Resolved an issue with custom notification sounds not working correctly.

- **Docker agent task hangs indefinitely when copying agent resources** ([AIR-8199322](https://youtrack.jetbrains.com/issue/AIR-8199322))
  Fixed a hang during "Copying agent resources to the agent volume" that had no timeout or error message, requiring a force-quit.

- **Content doesn't redraw on Windows** ([AIR-8141442](https://youtrack.jetbrains.com/issue/AIR-8141442))
  Resolved a rendering issue on Windows where UI content failed to redraw correctly.

- **Air using Credits over API tokens** ([AIR-8144014](https://youtrack.jetbrains.com/issue/AIR-8144014))
  Fixed incorrect billing behavior where Air consumed credits instead of the configured API tokens.

- **Show fast mode toggle for OpenAI 5.6 models** ([AIR-8150627](https://youtrack.jetbrains.com/issue/AIR-8150627))
  The fast mode toggle is now correctly displayed for OpenAI 5.6 model variants.

- **Pointer icon gets stuck in non-default state** ([AIR-8094988](https://youtrack.jetbrains.com/issue/AIR-8094988))
  Fixed a bug where the mouse cursor would become stuck in a non-default (e.g. resize or text) state.

- **Error while using Copilot via ACP: attempted to query hidden partition** ([AIR-8112371](https://youtrack.jetbrains.com/issue/AIR-8112371))
  Resolved an error thrown when using GitHub Copilot through the ACP protocol.

- **Clear command doesn't work** ([AIR-8036998](https://youtrack.jetbrains.com/issue/AIR-8036998))
  The `/clear` command now functions as expected again.

- **Filter out agents for the cloud task run** ([AIR-8036283](https://youtrack.jetbrains.com/issue/AIR-8036283))
  Agents are now properly filtered when running tasks in cloud environments.

- **Resume for worktree tasks does not work** ([AIR-8054086](https://youtrack.jetbrains.com/issue/AIR-8054086))
  Fixed an issue where attempting to resume a worktree task caused it to disappear from the task list.

- **[Windows] Opening file from Explorer shows "Air Cannot Start" error** ([AIR-7765473](https://youtrack.jetbrains.com/issue/AIR-7765473))
  Resolved a Windows-specific crash when opening a file directly from Explorer.

---

### Improvements

- **Add "Refresh Quota" action in AI Provider settings** ([AIR-7456303](https://youtrack.jetbrains.com/issue/AIR-7456303))
  A new refresh action in the AI Provider settings panel lets users manually update their quota display without restarting.

- **Better discoverability of available quota information** ([AIR-7612017](https://youtrack.jetbrains.com/issue/AIR-7612017))
  Quota details are now more prominently surfaced so users can see their remaining AI usage at a glance.

- **Configure full desktop session on CI agents** ([AIR-7679192](https://youtrack.jetbrains.com/issue/AIR-7679192))
  CI agents now run with a full desktop session, improving compatibility with GUI-dependent tasks.

- **Forbid intrinsic measurement of lazy components (UI)** ([AIR-8036283](https://youtrack.jetbrains.com/issue/AIR-8036283))
  Internal UI layout improvement preventing incorrect size measurements on lazy-loaded components.

---

*Produced by Air Automation. Name: Generate Release Notes / Run: https://air.stgn.jetbrains.cloud/org/05cf1a7f-6ab5-713b-abd3-29d0c8a05e2d/automations/700dc751-f867-4758-aa14-92fd8704e23d?run=726305ad-30df-4b85-99f5-014c1634fcc5*
