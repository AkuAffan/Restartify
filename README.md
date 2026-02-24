# Restartify

Restartify is a Paper plugin that automates Minecraft server restarts with configurable schedules, smart health-based triggers, and pre-restart safety steps.

## Highlights
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
1. Download the latest jar from GitHub Releases.
2. Place it in your server `plugins/` directory.
3. Start the server once to generate config files.
4. Edit:
   - `plugins/Restartify/config.yml`
   - `plugins/Restartify/messages.yml`
   - `plugins/Restartify/permissions.yml`
5. Run `/restartify reload` after changes.

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

## Build From Source
```powershell
cd plugins
.\apache-maven-3.9.6\bin\mvn.cmd -q clean package
```

Output jar:
- `plugins/target/restartify-<version>.jar`

## Release Workflow (This Repository)
Use the bundled release script to update logs and website downloads in one flow:

```powershell
cd plugins
node scripts/publish-update.mjs --changelog "Your change 1" --changelog "Your change 2"
```

What it does:
- updates `update-logs/restartify.json`
- copies jar to `website/public/downloads/`
- syncs generated website data

## Notes
- Timezone fallback: `Asia/Kuala_Lumpur` when invalid.
- Invalid auto-restart times are skipped.
- If all configured times are invalid, default fallback is `03:00`.
