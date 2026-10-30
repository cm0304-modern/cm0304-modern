# CM 03/04 Modern

A fan-made, unofficial update that brings **Championship Manager 03/04** (version 4.1.5) into the 2025/26 football world: real clubs, real players and staff, current stadiums and finances, and modern squad rules.

> **Unofficial.** This project is fan-made. It is not affiliated with, endorsed by, or connected to the original developers or publishers of Championship Manager. See [NOTICE.md](NOTICE.md).

**Current version: 25.0.1** - download the installer from the [Releases page](../../releases/latest).

## What you get

- **A 2025/26 world.** About 148,000 players and about 47,000 staff, built from Football Manager 26 data, with current club names, stadiums and finances.
- **28 nations with real 2025/26 divisions and cups**, tested through full seasons and season rollovers: England, Spain, Italy, France, Germany, Scotland, Holland, Portugal, Switzerland, Turkey, Czech Republic, Sweden, Wales, Northern Ireland, Argentina, Brazil, Norway, Croatia, Republic of Ireland, Slovakia, Austria, Denmark, Poland, Hungary, Greece, Finland, Ukraine and Belgium. Details: [nations](docs/nations.md).
- **Modern squad rules:** 12 named players, 5 substitutes used in league and cup matches (friendlies allow 12 substitutions).
- **2025/26 foreign-player limits** per nation (where the game can express them), updated EU flags, national-team managers, substitute rules, African Cup of Nations and year-related fixes.
- **A Contributors screen** in the game.

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

1. Download `CM0304-Modern-25.0.1-Setup.exe` from the [latest release](../../releases/latest). (Optional: compare its SHA-256 with the one on the release page.)
2. Run it. It asks for administrator rights because the default game folder is under Program Files. Windows may show an "unknown publisher" (SmartScreen) warning, because the installer is not code-signed.
3. Pick your game folder (the folder that contains `cm0304.exe`; common locations are detected). Setup checks the folder, backs up the original files, installs, and verifies every file.

Then **start a new game**. Saves made with the original game or other versions are not compatible.

**New to this update?** The installer is complete (it contains the full database and every change). You do **not** need 25.0.0 first: install it straight onto your CM 03/04 4.1.5 game.

**Upgrading from 25.0.0, or reinstalling:** just run the new installer on the same game folder. The database is unchanged from 25.0.0, so your 25.0.0 saves keep working.

Silent install for advanced users:

```
CM0304-Modern-25.0.1-Setup.exe /S /D=C:\Program Files (x86)\Eidos\CM 03-04
```

(`/D=` must be the last parameter. Exit code 0 means success. The log is `%TEMP%\CM0304-Modern-Setup.log`.)

## Uninstall

The installer copies the original files to `backup_pre_v25` inside your game folder. To go back, run `Uninstall CM 03-04 25.0.1.exe` from the game folder (or run the setup again with `/uninstall`). It verifies the backup, restores your files from before the update (your own exe included) byte for byte, and then removes the backup folder and the uninstaller itself. Your saves and other files are not touched. If an old backup exists from an earlier install, the installer archives it as `backup_pre_v25_old_<timestamp>` instead of blocking.

## What the installer changes

It **replaces `cm0304.exe`** with our modified executable (it carries the rule changes: substitutes, foreign-player limits, hidden nations, match speeds, year fixes; no CD is needed afterwards). Your own exe is backed up byte for byte. 25 entries, nothing else: `cm0304.exe`, the 4 database files and 3 player-history files in `data\db`, four menu/community XML files, and 13 old competition fixture files in `data\comps` (Belgium, France, Italy) that are removed (they go into the backup). Other exe-level mods are not kept while the update is installed.

The installer refuses, changing nothing, only when the folder is clearly not a CM 03/04 folder, the game is running or files are not writable. An unusual exe length or database header only gives a warning.

## Help, questions, bugs

- Questions: see the [FAQ](docs/faq.md).
- Found a bug? Use [Issues](../../issues/new/choose) and pick the matching form. For crashes, please attach a crash dump: [how to report a bug](docs/report-a-bug.md).

## Disclaimer

Fan-made and unofficial. Not affiliated with or endorsed by the original developers or publishers. The installer contains a modified game executable and data files, and no other game files. See [NOTICE.md](NOTICE.md).

## License

The documentation and text in this repository are licensed under [CC BY 4.0](LICENSE). The game, the installer's executable and data, and the football data are not covered; see [NOTICE.md](NOTICE.md).
