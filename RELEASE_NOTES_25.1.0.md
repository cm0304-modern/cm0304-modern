# CM 03/04 Modern 25.1.0

A fan-made, unofficial update that brings Championship Manager 03/04 (4.1.5) into the 2025/26 football world. Not affiliated with or endorsed by the original developers or publishers. The installer contains a modified game executable, data files, a small update helper and (from 25.0.3) a speed-up runtime library, and no other game files.

25.1.0 is a **complete installer**: it contains the full database and every change, so you can install it straight onto a CM 03/04 4.1.5 game. You do **not** need to install 25.0.0 first.

## Changelog

### Added

- Pictures for the Champions League, Europa League and Conference League in the title bar of their competition screens, and fixed header colours for the three competitions (dark blue, orange, green) instead of the colours of the last winner. The pictures are the three 60x60 PNG files in `data\graphics\pictures\competitions` (named by the competition id); you can replace them with your own.
- The qualifying rounds are listed one column per round on the competition screens, with the second chain labelled (Champions Path / League Path); the draw message arrives once per draw and 'View draw' opens that round.
- UEFA 2024+ competition formats: Champions League, Europa League and Conference League each play a 36-club league phase (Swiss-system draw with pots, 8 / 8 / 6 matchdays, the real tie-break order), then knockout play-offs, round of 16, quarter-finals, semi-finals and the final. The Super Cup is played between the Champions League and Europa League winners.
- Multi-round qualifying paths for all three competitions with the loser matrix between them (Champions League qualifying losers drop into the Europa League or Conference League qualifying, and so on), on the 2025/26 summer calendar.
- The 2026/27 UEFA access list: how many clubs each association sends to which round is worked out at every season rollover from the association coefficients (the five seasons before the closing one). Associations without a selectable league do not send clubs.
- Real UEFA association coefficients 2020/21-2024/25 and the 2024+ coefficient points rule (points per win/draw, elimination points, league-phase position bonuses, knockout bonuses); the UEFA Coefficients screen shows the new values.
- New screen **UEFA Club Coefficients** (Competitions > Europe): the top 200 clubs over the last five seasons with the total, from real club points plus the clubs of nations that are not part of your game.
- European prize money of the 2026/27 UEFA distribution (scaled by 0.75) for the Champions League, Europa League, Conference League and the Super Cup, paid through the clubs' normal finances.
- European competition history 2004-2025 (Champions League, Europa League, Conference League from 2022, Super Cup) and the new competition and round names.

### Changed

- A new game starts from the real 2024/25 season end: league positions and the domestic cup winners decide who enters the 2025/26 Champions League, Europa League and Conference League (the previous champions and cup winners are no longer guessed from the era data).
- Squad registration for the European qualifying rounds: the first registration deadline is before the first qualifying round (27 June) and a game that starts after it asks for the squad list on the first day, so a human club in qualifying is no longer left with an unregistered squad.
- On the UEFA Club Coefficients screen your own club is shown in yellow and the club and nation columns use the same font.
- The version label is now 25.1.0.
- Clubs that play in a division of a real nation but had no nation of their own in the data now get the nation of their division (needed by the new access list).

### How the installer treats your files

- The installer **replaces `cm0304.exe`** with our modified executable. It is part of the update: it carries the rule changes (substitutes, foreign-player limits, hidden nations, match speeds, year fixes). No CD is needed afterwards.
- Your own exe (official 4.1.5, a no-CD exe, anything else) is backed up byte for byte and restored by the uninstaller. Other exe-level mods are not kept while the update is installed.
- The installer refuses, changing nothing, only when the folder is clearly not a CM 03/04 folder, the game is running, or files are not writable. An unusual exe length or database header only gives a warning.

### Previous versions

**25.0.0** was the first public release: players and staff from Football Manager 26 data (about 148,000 players and about 47,000 staff), current club names, stadiums and finances, 28 nations with real 2025/26 divisions and cups (14 other nations are hidden), modern squad rules, 2025/26 foreign-player limits, updated EU flags, national-team managers, African Cup of Nations and year fixes, a Contributors screen, and a single installer with backup, verification and uninstaller.

**25.0.1** was a complete installer that works with the official 4.1.5 exe and no-CD exes, with friendly-match substitutions and the 2D match speed fixed.

**25.0.2** added an update notice: a small helper that, when the game starts, looks (at most once a day) at the project's release page and tells you when a newer version exists.

**25.0.3** added a speed-up runtime (a type-cast cache and a history-file handle cache in a small replacement of the game's runtime library, about 1.4x in the transfer window) that can be switched off in `cm_proxy.cfg`.

## Install

You need a CM 03/04 installation updated to 4.1.5 (the official 4.1.5 patch, or a no-CD exe: any exe works) on Windows 10 or 11. The game folder must contain `cm0304.exe` and `data\db` with the four database files. Close the game and the editor first.

1. Download the installer below.
2. Run it and accept the administrator prompt. Windows may warn about an unknown publisher (SmartScreen): the installer is not code-signed.
3. Choose the folder containing `cm0304.exe` and let setup finish.

**Upgrading from 25.0.0-25.0.3, or reinstalling:** run the new installer on the same game folder. Two new data files are added (`data\db\club_coef.dat` and `data\db\ccs_extra.dat`); the uninstaller removes them again. **Start a NEW game afterwards**: your 25.0.x saves do not load in 25.1.0 (keep them and use the uninstaller if you want to go back).

**Saves:** a save made by 25.1.0 only loads in 25.1.0.

**Uninstall:** originals are backed up to `backup_pre_v25` in your game folder (an old backup from an earlier install is archived as `backup_pre_v25_old_<timestamp>` instead of blocking). Run `Uninstall CM 03-04 25.1.0.exe` in the game folder, or the setup with `/uninstall`. It restores everything, then removes the backup folder and the uninstaller itself.

## Checksum

`CM0304-Modern-25.1.0-Setup.exe` (39,702,528 bytes)

SHA-256: `FBBB257A67F11CC5107A8959FAF84E608982A53B39F451BE3F30108589E32B7E`

Check it with PowerShell: `Get-FileHash .\CM0304-Modern-25.1.0-Setup.exe`

## Known issues

- 14 nations are not selectable.
- Some clubs have generated squads and some clubs have no manager.
- Reserve/B teams cannot be represented; youth teams are empty.
- Club and competition histories are still from 2003.

Full list: <https://cm0304-modern.github.io/cm0304-modern/known-issues>

## Bugs

Report problems with the issue forms. For crashes please attach a minidump: <https://cm0304-modern.github.io/cm0304-modern/report-a-bug>
