# CM 03/04 Modern 25.0.3

A fan-made, unofficial update that brings Championship Manager 03/04 (4.1.5) into the 2025/26 football world. Not affiliated with or endorsed by the original developers or publishers. The installer contains a modified game executable, data files, a small update helper and (from 25.0.3) a speed-up runtime library, and no other game files.

25.0.3 is a **complete installer**: it contains the full database and every change, so you can install it straight onto a CM 03/04 4.1.5 game. You do **not** need to install 25.0.0 first.

## Changelog

### Added

- Speed-up: the game runs faster through a type-cast cache and a history-file handle cache (about 1.4x in the transfer window in our tests). Both caches live in a small replacement of the game's own runtime library: `msvcr71.dll` in the game folder is replaced, your original runtime is kept next to it as `MSVCR71_real.dll`, and the optional settings are in `cm_proxy.cfg`.
- You can switch the speed-up off at any time by putting the line `CM_PROXY_DISABLE=1` into `cm_proxy.cfg` (the game then behaves as before), or install without it with the `/noproxy` switch of a silent install. The uninstaller puts your own `msvcr71.dll` back byte for byte and removes the two other files.
- If your `msvcr71.dll` is not the original runtime but another valid one, the installer keeps your file as `MSVCR71_real.dll`; if it is not a usable runtime, the installer leaves it alone and installs everything else without the speed-up (the last page says so).

### Changed

- The version label is now 25.0.3.

### How the installer treats your files

- The installer **replaces `cm0304.exe`** with our modified executable. It is part of the update: it carries the rule changes (substitutes, foreign-player limits, hidden nations, match speeds, year fixes). No CD is needed afterwards.
- Your own exe (official 4.1.5, a no-CD exe, anything else) is backed up byte for byte and restored by the uninstaller. Other exe-level mods are not kept while the update is installed.
- The installer refuses, changing nothing, only when the folder is clearly not a CM 03/04 folder, the game is running, or files are not writable. An unusual exe length or database header only gives a warning.

### Previous versions

**25.0.0** was the first public release: players and staff from Football Manager 26 data (about 148,000 players and about 47,000 staff), current club names, stadiums and finances, 28 nations with real 2025/26 divisions and cups (14 other nations are hidden), modern squad rules, 2025/26 foreign-player limits, updated EU flags, national-team managers, African Cup of Nations and year fixes, a Contributors screen, and a single installer with backup, verification and uninstaller.

**25.0.1** was a complete installer that works with the official 4.1.5 exe and no-CD exes, with friendly-match substitutions and the 2D match speed fixed.

**25.0.2** added an update notice: a small helper that, when the game starts, looks (at most once a day) at the project's release page and tells you when a newer version exists.

## Install

You need a CM 03/04 installation updated to 4.1.5 (the official 4.1.5 patch, or a no-CD exe: any exe works) on Windows 10 or 11. The game folder must contain `cm0304.exe` and `data\db` with the four database files. Close the game and the editor first.

1. Download the installer below.
2. Run it and accept the administrator prompt. Windows may warn about an unknown publisher (SmartScreen): the installer is not code-signed.
3. Choose the folder containing `cm0304.exe` and let setup finish.

**Upgrading from 25.0.0, 25.0.1 or 25.0.2, or reinstalling:** just run the new installer on the same game folder. The database is unchanged, so your 25.0.x saves keep working. The installer adds your `msvcr71.dll` to the existing backup before it replaces it.

**Switching the speed-up off by hand:** put `CM_PROXY_DISABLE=1` into `cm_proxy.cfg` (reversible), or delete `msvcr71.dll` and rename `MSVCR71_real.dll` to `msvcr71.dll`. Never delete only `MSVCR71_real.dll`: the game then does not start and Windows reports that `MSVCR71_real.dll` was not found.

**Saves:** for a fresh install on a game that never had 25.0.0, start a new game; saves from the original game or other versions are not compatible.

**Uninstall:** originals are backed up to `backup_pre_v25` in your game folder (an old backup from an earlier install is archived as `backup_pre_v25_old_<timestamp>` instead of blocking). Run `Uninstall CM 03-04 25.0.3.exe` in the game folder, or the setup with `/uninstall`. It restores everything, then removes the backup folder and the uninstaller itself.

## Checksum

`CM0304-Modern-25.0.3-Setup.exe` (39,649,792 bytes)

SHA-256: `BCC56B34CE982F4B8B3F430AC82BD25908AB559C609AA640C3C9AC04D9648B02`

Check it with PowerShell: `Get-FileHash .\CM0304-Modern-25.0.3-Setup.exe`

## Known issues

- 14 nations are not selectable.
- Some clubs have generated squads and some clubs have no manager.
- Reserve/B teams cannot be represented; youth teams are empty.
- Club and competition histories are still from 2003.

Full list: <https://cm0304-modern.github.io/cm0304-modern/known-issues>

## Bugs

Report problems with the issue forms. For crashes please attach a minidump: <https://cm0304-modern.github.io/cm0304-modern/report-a-bug>
