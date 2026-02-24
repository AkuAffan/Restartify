# Changelog

All notable changes to this project are documented in this file.

## [1.4.1] - 2026-02-24
- Added `/restartify help` and `/reboot help` with permission-aware usage output.
- Moved `discord-webhook` section above `warnings` in `config.yml`.
- Updated default message prefix style to use an arrow separator.

## [1.4.0] - 2026-02-23
- Added configurable countdown channels: title, actionbar, bossbar.
- Added countdown master toggle and multi-time auto-restart support.
- Added Discord webhook integration for restart start and restart complete.
- Set `pre-restart-safety.backup-world.enabled` default to `false`.
- Set `pre-restart-safety.clear-entities.enabled` default to `false`.

## [1.3.0] - 2026-02-23
- Added Pre-Restart Safety pipeline (world save, backup, entity cleanup).
- Improved restart stability with restart-in-progress and fallback handling.
- Improved legacy compatibility path with reflective API fallbacks.

## [1.2.1] - 2026-02-23
- Smart Restart now sends warning before restart on low TPS + high memory.
- Smart Restart now runs a configurable 20-second countdown by default.

## [1.2.0] - 2026-02-23
- Added Smart Restart trigger logic.
- Added `/smartrestart on|off` command.
