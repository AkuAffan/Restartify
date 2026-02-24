# Restartify

Restartify is a Paper plugin that automates Minecraft server restarts with smart monitoring, configurable countdown UI, and pre-restart safety actions.
Powered by Affanlabs Studios.

[![Website](https://img.shields.io/badge/Website-Restartify-0ea5e9?style=for-the-badge&logo=google-chrome&logoColor=white)](https://restartify.affanlabs.cloud)
[![Discord](https://img.shields.io/badge/Discord-Affanlabs-5865F2?style=for-the-badge&logo=discord&logoColor=white)](https://discord.affanlabs.cloud)
[![Portfolio](https://img.shields.io/badge/Portfolio-Affanlabs-111827?style=for-the-badge&logo=firefox-browser&logoColor=white)](https://portfolio.affanlabs.cloud)
[![GitHub Releases](https://img.shields.io/badge/Releases-GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com)

## Why Restartify
- Auto restart with multi-time schedule support (`auto-restart.times`).
- Smart Restart trigger when TPS is low and memory usage is high.
- Pre-Restart Safety pipeline:
  - auto world save
  - optional world backup
  - optional entity cleanup
- Countdown channels:
  - chat
  - title
  - actionbar
  - bossbar
- Optional Discord webhook notifications for restart start and restart complete.
- In-game help command: `/restartify help` (and `/reboot help`).

## Compatibility
- Software: Paper
- Minecraft versions: `1.8.9 - 1.21.11`
- Java: 8+

## Installation
1. Download the latest jar from GitHub Releases or our website ([restartify.affanlabs.cloud](https://restartify.affanlabs.cloud)).
2. Place the jar in your server `plugins/` directory.
3. Start the server once to generate plugin config files.
4. (Optional) Customize:
   - `plugins/Restartify/config.yml`
   - `plugins/Restartify/messages.yml`
   - `plugins/Restartify/permissions.yml`
5. Run `/restartify reload` after configuration changes.

## Commands
- `/restartify help`
- `/restartify reload`
- `/reboot help`
- `/reboot status`
- `/reboot now`
- `/reboot schedule <duration>` (example: `10m`, `1h30m`, `45s`)
- `/reboot cancel`
- `/autorestart on|off`
- `/smartrestart on|off`

## Permissions
- `restartify.admin`
- `restartify.now`
- `restartify.schedule`
- `restartify.cancel`
- `restartify.status`
- `restartify.reload`
- `restartify.autorestart`
- `restartify.smartrestart`

## Important Links
- Website: https://restartify.affanlabs.cloud
- Discord: https://discord.affanlabs.cloud
- Portfolio: https://portfolio.affanlabs.cloud

## Credits
- Created and maintained by Affanlabs Studios.

## Copyright
- Copyright (c) 2026 Affanlabs Studios. All rights reserved.

## Notes
- Timezone fallback: `UTC` when invalid.
- Invalid auto-restart times are skipped.
- If all configured times are invalid, default fallback is `03:00`.
