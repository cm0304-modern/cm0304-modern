# CM 03/04 Modern 25.0.1

A fan-made, unofficial update that brings Championship Manager 03/04 (4.1.5) into the 2025/26 football world. Not affiliated with or endorsed by the original developers or publishers. The installer contains a modified game executable and data files, and no other game files.

25.0.1 is a **complete installer**: it contains the full database and every change, so you can install it straight onto a CM 03/04 4.1.5 game. You do **not** need to install 25.0.0 first.

## Changelog

### Fixed

- Friendly matches allow 12 substitutions again. 25.0.0 wrongly limited them to 5. League and cup matches keep the modern rule (12 named players, 5 substitutions used).
- The 2D match view now follows the speed option. Fast is about 3x and Very Fast about 4.5x the pace of Medium (approximate figures). Medium, Slow and Very slow are unchanged.
- Installer: the 25.0.0 installer accepted only one specific 4.1.5 executable, so players with the official 4.1.5 exe (the one you get by installing the game and the official 4.1.4 and 4.1.5 patches) were refused. This is fixed: the installer now works with the official 4.1.5 exe and with no-CD exes.
- Installer: reinstalling after an uninstall works, and uninstalling cleans up after itself.

### Changed

- The version label is now 25.0.1.

### How the installer treats your files

- The installer **replaces `cm0304.exe`** with our modified executable. It is part of the update: it carries the rule changes (substitutes, foreign-player limits, hidden nations, match speeds, year fixes). No CD is needed afterwards.
- Your own exe (official 4.1.5, a no-CD exe, anything else) is backed up byte for byte and restored by the uninstaller. Other exe-level mods are not kept while the update is installed.
- The installer refuses, changing nothing, only when the folder is clearly not a CM 03/04 folder, the game is running, or files are not writable. An unusual exe length or database header only gives a warning.

### Previous versions

**25.0.0** was the first public release: players and staff from Football Manager 26 data (about 148,000 players and about 47,000 staff), current club names, stadiums and finances, 28 nations with real 2025/26 divisions and cups (14 other nations are hidden), modern squad rules, 2025/26 foreign-player limits, updated EU flags, national-team managers, African Cup of Nations and year fixes, a Contributors screen, and a single installer with backup, verification and uninstaller.

## Install

You need a CM 03/04 installation updated to 4.1.5 (the official 4.1.5 patch, or a no-CD exe: any exe works) on Windows 10 or 11. The game folder must contain `cm0304.exe` and `data\db` with the four database files. Close the game and the editor first.

1. Download the installer below.
2. Run it and accept the administrator prompt. Windows may warn about an unknown publisher (SmartScreen): the installer is not code-signed.
3. Choose the folder containing `cm0304.exe` and let setup finish.

**Upgrading from 25.0.0, or reinstalling:** just run the new installer on the same game folder. The database is unchanged from 25.0.0, so your 25.0.0 saves keep working.

**Saves:** for a fresh install on a game that never had 25.0.0, start a new game; saves from the original game or other versions are not compatible.

**Uninstall:** originals are backed up to `backup_pre_v25` in your game folder (an old backup from an earlier install is archived as `backup_pre_v25_old_<timestamp>` instead of blocking). Run `Uninstall CM 03-04 25.0.1.exe` in the game folder, or the setup with `/uninstall`. It restores everything, then removes the backup folder and the uninstaller itself.

## Checksum

`CM0304-Modern-25.0.1-Setup.exe` (39,401,984 bytes)

SHA-256: `97CC09DA977A93498B97E646EDB31E4E3BC2683BEB8C39577A520C4BDA61E7BB`

Check it with PowerShell: `Get-FileHash .\CM0304-Modern-25.0.1-Setup.exe`

## Known issues

- 14 nations are not selectable.
- Some clubs have generated squads and some clubs have no manager.
- Reserve/B teams cannot be represented; youth teams are empty.
- Club and competition histories are still from 2003.

Full list: <https://cm0304-modern.github.io/cm0304-modern/known-issues>

## Bugs

Report problems with the issue forms. For crashes please attach a minidump: <https://cm0304-modern.github.io/cm0304-modern/report-a-bug>
