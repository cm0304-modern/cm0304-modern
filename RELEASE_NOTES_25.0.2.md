# CM 03/04 Modern 25.0.2

A fan-made, unofficial update that brings Championship Manager 03/04 (4.1.5) into the 2025/26 football world. Not affiliated with or endorsed by the original developers or publishers. The installer contains a modified game executable and data files, and no other game files.

25.0.2 is a **complete installer**: it contains the full database and every change, so you can install it straight onto a CM 03/04 4.1.5 game. You do **not** need to install 25.0.0 first.

## Changelog

### Added

- Update notice: when you start the game, a small helper checks the project's GitHub releases page at most once a day. If a newer version exists, a short dialog tells you and offers to open the download page. It sends no data about you or your game, and it never changes anything by itself.
- You can turn the update notice off in the installer ("Check for updates when the game starts"), with the `/noupdatecheck` switch of a silent install, or later by creating an empty file named `update-check.disabled` in the game folder (or by setting the environment variable `CM0304_NO_UPDATE_CHECK=1`).

### Changed

- The version label is now 25.0.2.

### How the installer treats your files

- The installer **replaces `cm0304.exe`** with our modified executable. It is part of the update: it carries the rule changes (substitutes, foreign-player limits, hidden nations, match speeds, year fixes). No CD is needed afterwards.
- Your own exe (official 4.1.5, a no-CD exe, anything else) is backed up byte for byte and restored by the uninstaller. Other exe-level mods are not kept while the update is installed.
- The installer refuses, changing nothing, only when the folder is clearly not a CM 03/04 folder, the game is running, or files are not writable. An unusual exe length or database header only gives a warning.

### Previous versions

**25.0.0** was the first public release: players and staff from Football Manager 26 data (about 148,000 players and about 47,000 staff), current club names, stadiums and finances, 28 nations with real 2025/26 divisions and cups (14 other nations are hidden), modern squad rules, 2025/26 foreign-player limits, updated EU flags, national-team managers, African Cup of Nations and year fixes, a Contributors screen, and a single installer with backup, verification and uninstaller.

**25.0.1** was a complete installer that works with the official 4.1.5 exe and no-CD exes, with friendly-match substitutions and the 2D match speed fixed.

## Install

You need a CM 03/04 installation updated to 4.1.5 (the official 4.1.5 patch, or a no-CD exe: any exe works) on Windows 10 or 11. The game folder must contain `cm0304.exe` and `data\db` with the four database files. Close the game and the editor first.

1. Download the installer below.
2. Run it and accept the administrator prompt. Windows may warn about an unknown publisher (SmartScreen): the installer is not code-signed.
3. Choose the folder containing `cm0304.exe` and let setup finish.

**Upgrading from 25.0.0 or 25.0.1, or reinstalling:** just run the new installer on the same game folder. The database is unchanged, so your 25.0.x saves keep working.

**Saves:** for a fresh install on a game that never had 25.0.0, start a new game; saves from the original game or other versions are not compatible.

**Uninstall:** originals are backed up to `backup_pre_v25` in your game folder (an old backup from an earlier install is archived as `backup_pre_v25_old_<timestamp>` instead of blocking). Run `Uninstall CM 03-04 25.0.2.exe` in the game folder, or the setup with `/uninstall`. It restores everything, then removes the backup folder and the uninstaller itself.

## Checksum

`CM0304-Modern-25.0.2-Setup.exe` (39,419,904 bytes)

SHA-256: `27EE32E75508B13D7DE15258600B3F0316AD2410F3ADFC6D1EED87F052E42E42`

Check it with PowerShell: `Get-FileHash .\CM0304-Modern-25.0.2-Setup.exe`

## Known issues

- 14 nations are not selectable.
- Some clubs have generated squads and some clubs have no manager.
- Reserve/B teams cannot be represented; youth teams are empty.
- Club and competition histories are still from 2003.

Full list: <https://cm0304-modern.github.io/cm0304-modern/known-issues>

## Bugs

Report problems with the issue forms. For crashes please attach a minidump: <https://cm0304-modern.github.io/cm0304-modern/report-a-bug>
