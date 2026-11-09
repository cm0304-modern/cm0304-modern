# CM 03/04 Modern

A fan-made, unofficial update that brings **Championship Manager 03/04** (version 4.1.5) into the 2025/26 football world: real clubs, real players and staff, current stadiums and finances, and modern squad rules.

> **Unofficial.** This project is fan-made. It is not affiliated with, endorsed by, or connected to the original developers or publishers of Championship Manager. See [NOTICE.md](NOTICE.md).

**Current version: 25.1.2** - download the installer from the [Releases page](../../releases/latest).

## What you get

- **A 2025/26 world.** About 148,000 players and about 47,000 staff, built from Football Manager 26 data, with current club names, stadiums and finances.
- **28 nations with real 2025/26 divisions and cups**, tested through full seasons and season rollovers: England, Spain, Italy, France, Germany, Scotland, Holland, Portugal, Switzerland, Turkey, Czech Republic, Sweden, Wales, Northern Ireland, Argentina, Brazil, Norway, Croatia, Republic of Ireland, Slovakia, Austria, Denmark, Poland, Hungary, Greece, Finland, Ukraine and Belgium. Details: [nations](docs/nations.md).
- **Modern squad rules:** 12 named players, 5 substitutes used in league and cup matches (friendlies allow 12 substitutions).
- **2025/26 foreign-player limits** per nation (where the game can express them), updated EU flags, national-team managers, substitute rules, African Cup of Nations and year-related fixes.
- **A Contributors screen** in the game.
- **An optional update notice** (new in 25.0.2): at most once a day the game tells you when a newer version of your own version line is out (25.x players are told about 25.x versions). It can be switched off. See [the update notice](docs/update-notice.md).

Not everything is perfect. Please read the [known issues](docs/known-issues.md) before you start.

## Screenshots

![English Premier Division table](docs/images/01-premier-league-table.jpg)

![Haaland player profile](docs/images/08-haaland-profile.jpg)

![Liverpool squad](docs/images/04-liverpool-squad.jpg)

More in the [screenshots gallery](docs/screenshots.md).

## Requirements

- Windows 10 or 11.
- Championship Manager 03/04 updated to **version 4.1.5** (the official 4.1.5 patch, or a no-CD exe: any exe works, because the installer brings its own exe).
- The game folder must contain `cm0304.exe` and `data\db` with the four database files.
- The game (and the editor) must be **closed**, and the files must be writable.
- About 700 MB of free disk space.

This project does **not** include the game. You need your own copy.

## Install (3 steps)

1. Download `CM0304-Modern-25.1.2-Setup.exe` from the [latest release](../../releases/latest). (Optional: compare its SHA-256 with the one on the release page.)
2. Run it. It asks for administrator rights because the default game folder is under Program Files. Windows may show an "unknown publisher" (SmartScreen) warning, because the installer is not code-signed.
3. Pick your game folder (the folder that contains `cm0304.exe`; common locations are detected). Setup checks the folder, backs up the original files, installs, and verifies every file.

Then **start a new game**. Saves made with the original game or with versions before 25.1.0 are not compatible (saves of 25.1.0 load in 25.1.1).

**New to this update?** The installer is complete (it contains the full database and every change). You do **not** need 25.0.0 first: install it straight onto your CM 03/04 4.1.5 game.

**Upgrading from 25.1.0, or reinstalling:** just run the new installer on the same game folder. Only `cm0304.exe` and the update helper change (25.1.1 fixes the European prize money, the Slovak and Argentine league calendars and a rare Serie C Cup crash, see the [changelog](docs/changelog.md)); the database is identical, so your 25.1.0 saves keep working. The Argentina fix is for **new games**: a save made with an earlier version keeps its old Argentine second-division calendar (the Argentine leagues stay stuck in it), so start a new game to get the corrected structure.

**Upgrading from 25.0.x:** run the new installer on the same game folder and **start a new game**: saves made with 25.0.x do not load in 25.1.x.

**Which version do I need?** 25.x is the 2025/26 game you are looking at; it keeps receiving bug fixes. A 26.x line (the 2026/27 game) is planned as a separate game. See [which version do I need](docs/index.md#which-version-do-i-need-two-lines).

Silent install for advanced users:

```
CM0304-Modern-25.1.2-Setup.exe /S /D=C:\Program Files (x86)\Eidos\CM 03-04
```

Add `/noupdatecheck` to leave the update notice off (see [the update notice](docs/update-notice.md)). (`/D=` must be the last parameter. Exit code 0 means success. The log is `%TEMP%\CM0304-Modern-Setup.log`.)

## Uninstall

The installer copies the original files to `backup_pre_v25` inside your game folder. To go back, run `Uninstall CM 03-04 25.1.2.exe` from the game folder (or run the setup again with `/uninstall`). It verifies the backup, restores your files from before the update (your own exe included) byte for byte, and then removes the backup folder and the uninstaller itself. Your saves and other files are not touched. If an old backup exists from an earlier install, the installer archives it as `backup_pre_v25_old_<timestamp>` instead of blocking.

## What the installer changes

It **replaces `cm0304.exe`** with our modified executable (it carries the rule changes: substitutes, foreign-player limits, hidden nations, match speeds, year fixes; no CD is needed afterwards). Your own exe is backed up byte for byte. The installer changes **34 entries**, nothing else: `cm0304.exe`, the 4 database files and 3 player-history files in `data\db`, two UEFA data files (`club_coef.dat` and `ccs_extra.dat`, new in 25.1.0), three competition pictures, four menu/community XML files, the update helper `CM0304-UpdateCheck.exe`, the three speed-up files (`msvcr71.dll`, `MSVCR71_real.dll` and `cm_proxy.cfg`, new in 25.0.3), and 13 old competition fixture files in `data\comps` (Belgium, France, Italy) that are removed (they go into the backup). Other exe-level mods are not kept while the update is installed.

The update helper (new in 25.0.2, version 1.1.0 since 25.1.1) is added to the game folder; the uninstaller removes it and its small settings folder. The exe starts the helper at game start. The helper is an unsigned program, so antivirus or SmartScreen may warn; it can be deleted or switched off and the game works without it. See [the update notice](docs/update-notice.md).

The installer refuses, changing nothing, only when the folder is clearly not a CM 03/04 folder, the game is running or files are not writable. An unusual exe length or database header only gives a warning.

## Help, questions, bugs

- Questions: see the [FAQ](docs/faq.md).
- Found a bug? Use [Issues](../../issues/new/choose) and pick the matching form. For crashes, please attach a crash dump: [how to report a bug](docs/report-a-bug.md).

## Disclaimer

Fan-made and unofficial. Not affiliated with or endorsed by the original developers or publishers. The installer contains a modified game executable and data files, and no other game files. See [NOTICE.md](NOTICE.md).

## License

The documentation and text in this repository are licensed under [CC BY 4.0](LICENSE). The game, the installer's executable and data, and the football data are not covered; see [NOTICE.md](NOTICE.md).
