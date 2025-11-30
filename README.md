# 99LP

<div align="center">

**Never Miss a Play**

Automatic League of Legends replay recording with post-game insights.

[🌐 Website](https://99lp.lol) • [💬 Discord](https://discord.gg/9JQzXfTVXE) • [📥 Download (Alpha)](../../releases/latest)

[![Alpha v0.2.3](https://img.shields.io/badge/version-v0.2.3-cyan)](../../releases/latest)
[![Discord](https://img.shields.io/discord/YOUR_DISCORD_ID?color=5865F2&logo=discord&logoColor=white)](https://discord.gg/9JQzXfTVXE)
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)

</div>

---

## Features

Stop forgetting to hit record. 99LP automatically captures your League games and gives you post-game insights to help you improve.

**What you get:**
- 🎥 **Auto-recording** - Detects League games and records automatically
- ✂️ **Smart clips** - Creates clips for kills, deaths, objectives, and highlights
- 📊 **Post-game insights** - Analyzes your deaths, vision, CS, and early game mistakes
- 🔒 **100% local** - No account, no cloud, everything stays on your PC
- ⚡ **No FPS impact** - Lightweight recording (~5 FPS drop)

## Download

**Alpha v0.2.3** is available for early access testers on Discord.

[📥 Download Latest Release](../../releases/latest) | [💬 Join Discord for Early Access](https://discord.gg/9JQzXfTVXE)

**Requirements:**
- Windows 10/11 (64-bit)
- ~10-20GB free disk space
- League of Legends (Windowed or Borderless mode)
- WebView2 Runtime (usually pre-installed on Windows 11)

## How it works

After each game, 99LP fetches match data from Riot's API and analyzes your performance:

**📉 Death Analysis**
- Context for each death (overextended, objective throw, gold swing)
- Role-specific early game analysis (CS loss, camps stolen, ADC abandoned)
- Links directly to the clip so you can review what happened

**👁️ Vision Score**
- Checks ward placement before objectives (Drake, Baron, Herald)
- Compares your vision score to role benchmarks
- Highlights missed vision opportunities

**🎯 Performance Metrics**
- CS/min tracking with lane-specific benchmarks
- Kill participation and map presence
- Objective control and team fighting impact

## ⚠️ Alpha Notice

This is an **alpha build** - bugs are expected!

**Known issues:**
- Windows SmartScreen warning (click "More info" → "Run anyway")
- May require admin rights for first launch
- Practice Tool games not supported
- ~1-2 minute delay after game for Riot API indexing

**Reporting bugs:**
- [Discord](https://discord.gg/9JQzXfTVXE) (fastest response)
- [GitHub Issues](../../issues)

## How it works technically

**Recording:** Uses Windows Graphics Capture API to record at ~100 FPS. Encodes with Media Foundation (H.264). Circular buffer keeps last N hours of footage and auto-deletes old files.

**Events:** Connects to League's Live Client API (port 2999) to track kills/deaths/objectives with coordinates.

**Analysis:** After game, finds the match on Riot's API by timestamp. Fetches match + timeline data. Analyzes deaths, vision score, early game mistakes. Generates insights with actionable suggestions.

**Clips:** FFmpeg extracts 30s clips around each event. Auto-clips saved with thumbnails.

## File Locations

- **Videos**: Custom folder (selected on first launch, default: `%USERPROFILE%\Videos\99LP`)
- **Database**: `%USERPROFILE%\AppData\Local\99LP\99lp.db`
- **Logs**: `%USERPROFILE%\AppData\Local\99LP\logs\`

## Roadmap

**Coming soon:**
- 🗺️ Death heatmaps visualized on minimap
- 📈 Multi-game performance dashboard
- 🎯 Win condition tracking (team comp analysis, objective priority)
- ⚔️ AI-powered outplay detection

**Long-term:**
- 🏪 Microsoft Store release (no more SmartScreen warnings)
- 🔗 Clip sharing with friends
- 🎮 Support for more games (Valorant, CS2, Dota 2)

## Privacy & Data

**100% local. No cloud. No account.**

- All recordings stay on your PC
- No telemetry or tracking
- Riot API calls only to fetch your match data
- Open source (repo available for contributors on request)

## Support

Need help or found a bug?

- 💬 [Join our Discord](https://discord.gg/9JQzXfTVXE) (fastest response)
- 🐛 [Open an issue](../../issues)
- 🌐 [Visit our website](https://99lp.lol)

---

<div align="center">

**Made with ❤️ for League players who want to improve**

© 2025 99LP • [Website](https://99lp.lol) • [Discord](https://discord.gg/9JQzXfTVXE)

</div>
