# Long-term Memory

This file stores persistent information across sessions.

## User Preferences

- Language: Korean (prefers polite 존댓말, clear explanations)
- Model: StepFun (step-3.5-flash:free) preferred for now (free tier)
- Notifications: Only send health summaries when issues detected.

## System Configuration

- OpenClaw installed on WSL2 (Ubuntu 24.04)
- Cron jobs configured: health check, heartbeat, hourly reminder, log rotation, memory cleanup, system update, weekly backup, security scan.
- Gateway bound to localhost only.

## Notes

- Power settings: Windows host may suspend; cron helps maintain connectivity.
- UI build: pnpm ui:build run to generate Control UI assets.
- Sudoers configured to allow passwordless apt for user 'dongm'.
- Initial system setup completed (Feb 15-16, 2026): OpenClaw installed on WSL2, all cron jobs configured, UI build attempted, sudoers set for apt, health/heartbeat tuned to issue-only notifications.
- Update channel: npm 2026.2.15 available (auto-updates scheduled at 4am).
- Initial state: 64 packages pending updates (resolved automatically by system update cron).
- Health check & heartbeat configured correctly: only report when issues detected; normal operation remains silent.
- Memory plugin: core loaded successfully, lancedb disabled (as expected for current setup).
- Cron automation verified: heartbeat, hourly reminder, health check all functioning properly.

## Decisions

- Use free models only.
- Keep system local-only (no external exposure).
- Automate recurring maintenance tasks.
