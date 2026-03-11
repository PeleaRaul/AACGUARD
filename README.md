<p align="center">
  <img src="https://aacguard.com/assets/aacguard-logo.svg" alt="AACGUARD Logo" width="240">
</p>

<h1 align="center">AACGUARD – Client‑Side Anti‑Cheat for CS:GO, CS 1.6 & CS2</h1>

<p align="center">
  Lightweight client-side anti-cheat for community servers, focused on loaders, injected modules, and cheat traces – without kernel drivers or noisy false positives.
</p>

<p align="center">
  <a href="https://aacguard.com/"><b>Website</b></a> •
  <a href="https://aacguard.com/downloads/AACGUARD-v0.0.8.exe">Download</a> •
  <a href="https://aacguard.com/trust.php">Trust Center</a> •
  <a href="https://aacguard.com/features.php">Features</a> •
  <a href="https://aacguard.com/changelog.php">Changelog</a> •
  <a href="https://aacguard.com/detected.php">Live detections</a>
</p>

> ⚠️ This repository is an informational landing page only.  
> No source code or binaries are published on GitHub.  
> To download AACGUARD, always use the official website: https://aacguard.com/

---

## What is AACGUARD?

AACGUARD is a **client-side anti-cheat scanner** for CS:GO, CS 1.6 and CS2 community servers. It focuses on detecting:

- Cheat loaders and injectors  
- Injected modules and tampering  
- Known cheat traces in configs, game folders and environment  

AACGUARD aims to help community owners catch real cheats, not legit players running Discord, overlays or common background apps. [page:1]

Current build: **AACGUARD v0.0.8 · DEV** [page:1]  

---

## Key features

- **Cheat‑first detection**  
  Targets loaders, injected modules and suspicious behaviour patterns instead of generic background software, reducing noise from harmless tools. [page:1]

- **Transparent scan history**  
  Every scan is logged with timestamps, Steam identifiers and final verdicts (CLEAN / SUSPICIOUS / CHEAT DETECTED) in your AACGUARD panel, giving admins an audit trail per player. [page:1]

- **Live stats & console**  
  The web panel shows total scans, flagged players, last detections and a live console log with the latest scan activity. [page:1]

- **Drop‑in for communities**  
  Designed to sit next to your existing CS:GO / CS 1.6 / CS2 stack – it does not force a specific host, plugin system or ecosystem. [page:1]

- **No kernel drivers (current builds)**  
  Current versions are user‑mode only; no kernel‑level drivers are installed on the player’s machine. [page:1]

- **Dedicated backend API**  
  Scans are submitted over HTTP(S) to an ASP.NET Core API on your Debian host, which writes into a MySQL/MariaDB backend. The client never touches your database directly. [page:1]

---

## How AACGUARD works (high‑level)

1. Player downloads and runs AACGUARD on Windows. [page:1]  
2. The client scans:
   - Steam account and running game processes  
   - CS:GO / CS 1.6 / CS2 configs and game folders  
   - Environment and processes for known cheat loaders and injected modules  
3. The client sends scan metadata, verdict, Steam ID and relevant non‑default config data to your AACGUARD panel via the backend API. [page:1]  
4. Your panel stores scan history and presents verdicts and evidence to server admins. [page:1]  
5. Server admins decide how to act (e.g. allow/monitor/ban) based on AACGUARD results. [page:1]

Scans only run while the user has AACGUARD open and presses **Start** or **Restart**. It does **not** run permanently in the background. [page:1]

---

## What AACGUARD collects

AACGUARD is designed as a cheat‑focused scanner, not general spyware, but it still needs deep visibility into the game environment. In broad terms it may collect: [page:1]

- Steam ID and Steam name  
- Scan metadata (timestamps, status, triggered detections, scores)  
- Game‑related data such as non‑default CS:GO / CS2 configs and some environment traces relevant to cheat detection  
- Information about loaders, injected modules and suspicious processes related to cheating  

Scan histories and verdicts are stored on the AACGUARD panel’s database so server admins can review them later. [page:1]

For full details, read the official documents:

- Privacy Policy: https://aacguard.com/privacy.php  
- Terms of Use: https://aacguard.com/terms.php  
- EULA License: https://aacguard.com/license.php  [page:1][page:0][page:2]

---

## Download & installation

AACGUARD is distributed **only** via the official website.

- Download page: https://aacguard.com/  
- Direct Windows client (current dev build):  
  https://aacguard.com/downloads/AACGUARD-v0.0.8.exe  [page:1]

Basic flow for players:

1. Download AACGUARD from the official website. [page:1]  
2. Run the installer / executable and launch the client. [page:1]  
3. Press **Start** to run a scan when requested by a server admin. [page:1]  
4. Share or link your scan status as required by the community rules. [page:1]

---

## Admin / server‑owner integration

AACGUARD is built for community servers that want an extra signal on cheating without running their own kernel‑level driver. [page:1]

As a server owner you can:

- Host the AACGUARD backend API + database on your own Debian server (as described in the changelog and docs). [page:1]  
- Use the web panel to:
  - View per‑player scan history and verdicts  
  - See live stats and console logs  
  - Track banned / detected players [page:1]  
- Integrate your existing plugins (CS:GO / CS 1.6 / CS2) to reference AACGUARD scan results when enforcing bans or whitelists. [page:1]

More information:

- Features: https://aacguard.com/features.php  
- Changelog: https://aacguard.com/changelog.php  
- Detected/Banned players list: https://aacguard.com/detected.php  [page:1]

---

## Security & trust

To help users verify AACGUARD builds, the project maintains a **Trust Center** with:

- VirusTotal reports for the client and installer  
- SHA256 hashes and timestamps for each published binary  
- Guidance on re‑uploading and verifying files independently [page:13]

Trust Center: https://aacguard.com/trust.php [page:13]

Always verify hashes and only download from the official site.

---

## Support & community

- Website: https://aacguard.com/  
- Discord: https://discord.gg/gsyVyc4xUp  
- Email: support@aacguard.com  
- Buy me a coffee: https://buymeacoffee.com/aacguard  [page:1]

---

## Legal

AACGUARD is an **unofficial** anti‑cheat for CS:GO, CS 1.6 and CS2 and has **no affiliation with Valve**. [page:1]

By downloading or using AACGUARD, you agree to the:

- EULA License: https://aacguard.com/license.php  
- Privacy Policy: https://aacguard.com/privacy.php  
- Terms of Use: https://aacguard.com/terms.php  [page:0][page:1][page:2]

© 2026 AACGUARD. All rights reserved.
