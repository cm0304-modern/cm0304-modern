# CM 03/04 Modern 25.1.1

A fan-made, unofficial update that brings Championship Manager 03/04 (4.1.5) into the 2025/26 football world. Not affiliated with or endorsed by the original developers or publishers. The installer contains a modified game executable, data files, a small update helper and (from 25.0.3) a speed-up runtime library, and no other game files.

25.1.1 is a **complete installer**: it contains the full database and every change, so you can install it straight onto a CM 03/04 4.1.5 game. You do **not** need to install 25.0.0 first.

## Changelog

### Fixed

- The prize money of the league phase of the Champions League, Europa League and Conference League was paid several times per match when the League Table tab of the live match screen was open: every refresh of that tab paid every club of the night again, and your inbox filled with the same message ('given $2,500,000' ten times for one match). It is now paid once per match, when the match is decided. The amounts are unchanged. Matches you do not watch, or watch with that tab closed, were always paid correctly.
- The Slovak divisions play exactly the number of matches they declare. The calendars of the First Division (12 clubs, 33 matches each) and the Second Division (14 clubs, 26 matches each) had 36 and 30 dates; they now have 33 and 26 matchdays. In an existing save the current season keeps its old calendar and the next season is created with the right one.
- A rare crash of the Serie C Cup knock-out stage on 10-11 September of a NEW game with Italy (about 1 in 200 new games with Italy) is fixed. A save whose Serie C Cup was already built too short cannot be repaired.
- The Argentine second division (Primera Nacional, 36 clubs) now completes its second half-season (35 matchdays instead of 21), so the Argentine leagues finish their season and move on to the next one; the Argentine second division stays at 36 clubs and the Premier Division at 30.

### Changed

- The update notice only offers newer versions of the version line you have installed (25.x offers 25.x). A different major version (26.x) is a separate game and is never offered by it. The helper is now version 1.1.0.
- The version label is now 25.1.1.

### How the installer treats your files

- The installer **replaces `cm0304.exe`** with our modified executable. It is part of the update: it carries the rule changes (substitutes, foreign-player limits, hidden nations, match speeds, year fixes). No CD is needed afterwards.
- Your own exe (official 4.1.5, a no-CD exe, anything else) is backed up byte for byte and restored by the uninstaller. Other exe-level mods are not kept while the update is installed.
- The installer refuses, changing nothing, only when the folder is clearly not a CM 03/04 folder, the game is running, or files are not writable. An unusual exe length or database header only gives a warning.

### Previous versions

**25.0.0** was the first public release: players and staff from Football Manager 26 data (about 148,000 players and about 47,000 staff), current club names, stadiums and finances, 28 nations with real 2025/26 divisions and cups (14 other nations are hidden), modern squad rules, 2025/26 foreign-player limits, updated EU flags, national-team managers, African Cup of Nations and year fixes, a Contributors screen, and a single installer with backup, verification and uninstaller.

**25.0.1** was a complete installer that works with the official 4.1.5 exe and no-CD exes, with friendly-match substitutions and the 2D match speed fixed.

**25.0.2** added an update notice: a small helper that, when the game starts, looks (at most once a day) at the project's release page and tells you when a newer version exists.

**25.0.3** added a speed-up runtime (a type-cast cache and a history-file handle cache in a small replacement of the game's runtime library, about 1.4x in the transfer window) that can be switched off in `cm_proxy.cfg`.

**25.1.0** brought the modern UEFA formats: a 36-club league phase for the Champions League, Europa League and Conference League, multi-round qualifying paths, the 2026/27 access list from the association coefficients, a UEFA Club Coefficients screen, European prize money and competition history. It needs a new game.

## Install

You need a CM 03/04 installation updated to 4.1.5 (the official 4.1.5 patch, or a no-CD exe: any exe works) on Windows 10 or 11. The game folder must contain `cm0304.exe` and `data\db` with the four database files. Close the game and the editor first.

1. Download the installer below.
2. Run it and accept the administrator prompt. Windows may warn about an unknown publisher (SmartScreen): the installer is not code-signed.
3. Choose the folder containing `cm0304.exe` and let setup finish.

**Upgrading from 25.1.0, or reinstalling:** run the new installer on the same game folder. Only `cm0304.exe` and `CM0304-UpdateCheck.exe` are replaced; the database files and everything else are left as they are, and your saves keep working. If you switched the update notice off (the file `update-check.disabled`), it stays off.

**Upgrading from 25.0.x or earlier:** run the installer as before, then **start a NEW game**: saves of 25.0.x and earlier do not load.

**Saves:** a save made with 25.1.0 loads in 25.1.1. The Slovak calendar fix reaches an existing save at its next season; a save whose Serie C Cup was already built too short cannot be repaired.

**About the bug in 25.1.0:** money that a save has already received through it stays in that save and cannot be repaired. Until you update, do not open the League Table tab of the match screen during a live European league-phase match.

**Argentina is fixed for new games only.** A save made with an earlier version keeps its old Argentine second-division calendar (the calendar of a season is stored in the save): in such a save that division still cannot complete its season and the Argentine leagues stay stuck. Start a new game for the corrected structure.

**Uninstall:** originals are backed up to `backup_pre_v25` in your game folder (an old backup from an earlier install is archived as `backup_pre_v25_old_<timestamp>` instead of blocking). Run `Uninstall CM 03-04 25.1.1.exe` in the game folder, or the setup with `/uninstall`. It restores everything, then removes the backup folder and the uninstaller itself.

## Checksum

`CM0304-Modern-25.1.1-Setup.exe` (39,704,064 bytes)

SHA-256: `88163018132BC3F674CD504A83D8DA4F0FB6648C6AC3B89CEA9CC6F22133AB3D`

Check it with PowerShell: `Get-FileHash .\CM0304-Modern-25.1.1-Setup.exe`

## Known issues

- 14 nations are not selectable.
- Some clubs have generated squads and some clubs have no manager.
- Reserve/B teams cannot be represented; youth teams are empty.
- Club and competition histories are still from 2003.

Full list: <https://cm0304-modern.github.io/cm0304-modern/known-issues>

## Bugs

Report problems with the issue forms. For crashes please attach a minidump: <https://cm0304-modern.github.io/cm0304-modern/report-a-bug>
