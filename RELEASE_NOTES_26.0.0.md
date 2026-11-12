# CM 03/04 Modern 26.0.0

A fan-made, unofficial update that brings Championship Manager 03/04 (4.1.5) into the **2026/27** football world. Not affiliated with or endorsed by the original developers or publishers. The installer contains a modified game executable, data files, a small update helper and a speed-up runtime library, and no other game files.

26.0.0 is a **complete installer**: it contains the full database and every change, so you can install it straight onto a CM 03/04 4.1.5 game. You do **not** need to install 25.x first. **It is the 2026/27 game and needs a NEW game**: saves made with 25.x or earlier versions do not load in it. The 2025/26 game (25.x) stays available on the Releases page and is not changed by this release.

## Changelog

### Added

- **The 2026/27 season.** A new game now starts in July 2026 (Sunday 12 July 2026 when all 30 nations are ticked). Players, ratings, contracts, loans, staff, club reputations, finances, facilities and kit colours are rebuilt from the Football Manager 27 database for 30 nations: the 28 nations of 25.x plus Russia and Israel. The database holds more than 140,000 players and more than 48,000 staff.
- **Russia and Israel are playable.** Both can be ticked on the new-game screen: Russia with a 16-club Premier League and an 18-club FNL, Israel with a 14-club Premier League and a 16-club Liga Leumit. Israel sends clubs to the European competitions; Russia sends nobody. The other 12 nations that were hidden in 25.x stay hidden (see Known issues).
- **League structures of 2026/27.** The Turkish second division (TFF 1. Lig) has 20 clubs, the Welsh Cymru Premier 16, the Northern Irish Championship 16, the Russian FNL 18, the Israeli Premier League 14 and Liga Leumit 16. The promotion and relegation of the 2025/26 season are applied: the first divisions of the 30 nations hold their real 2026/27 clubs where the game has them.
- **Real 2025/26 final tables, European places and coefficients.** First-division clubs start with their real 2025/26 final positions, and the real 2025/26 cup winners are known to the game, so the 2026/27 places in the Champions League, Europa League and Conference League are worked out from the real results. The UEFA association and club coefficients carry the real points up to and including 2025/26, and the UEFA calendar is the real 2026/27 one (for example the Super Cup on 12 August 2026).
- **History up to 2025/26.** For the 30 nations the winners of the league, the national cup, the league cup and the super cup from 2003/04 to 2025/26 are in the history screens, with the runner-up and, for leagues, the third place wherever it is certain (editions that are disputed or were not held are left out). The European Championship 2004-2024 and the World Cup 2006-2026 winners are there, and the Euro 2028 and World Cup 2030 screens show their hosts (England and the Republic of Ireland; Morocco and Spain: the game shows at most two hosts). The European competition histories reach 2026.
- **Kit colours from the new data.** Hundreds of clubs that had no kit, or whose old colours did not match the club, now have their real colours (Alanyaspor are orange and green).
- **Loans.** More than 3,500 players start the game on loan at their loan clubs, as in the data.
- **Stadiums.** The grounds of 4,283 clubs were changed to the real stadium name and capacity (for example Arsenal at the Emirates Stadium, 60,704; FC Bayern München at the Allianz-Arena, 75,000; Juventus at the Allianz Stadium, 41,507; Ajax at the Johan Cruijff ArenA, 55,500). The old stadium-move entries of the original game that concern the clubs of the 30 nations (moves scheduled for 2026-2028) are switched off in the database.

### Changed

- **26/27 everywhere.** The game window is titled 'Championship Manager 26/27', the Start Menu header and the Quit hint say 26/27, and the version label is 26.0.0. Competition names follow the new data (for example Süper Lig, Premier League).
- **Staff attributes are on the game's own 1-20 scale.** The attributes of coaches, scouts, physios and the other staff are converted from the source's larger scale to the 20-point scale the game uses.
- **Staff dates.** In the database every staff contract ends after the start of the game and nobody keeps the dummy birth year 1900: more than 1,000 staff whose source page gave no age have a plausible one. The game recalculates some staff dates itself when a new game starts, so the dates on the staff screens can still differ.
- **Midfield labels.** The squad list and the player profile print one midfield label per player (defensive midfield before attacking midfield before midfield), so a weaker 'accomplished' role could hide a natural one. About 11,000 such roles in the database were lowered one step, so that the natural role is the one that is shown; the Positions pitch still draws them as accomplished (light green). About 880 natural wing-backs who had no defender position now count as defenders.
- **The Positions pitch of the player profile (25.1.2) is included**, with the original attribute-group colours.
- **The prize-money fix and the calendar fixes of 25.1.1 are included**: European league-phase prize money is paid once per match, the Slovak divisions have the right number of matchdays, the rare Serie C Cup crash is fixed and the Argentine second division completes its season.

### How the installer treats your files

- The installer **replaces `cm0304.exe`** with our modified executable. It is part of the update: it carries the rule changes (substitutes, foreign-player limits, hidden nations, match speeds, the UEFA formats, year fixes, the 26/27 texts). No CD is needed afterwards.
- Your own exe (official 4.1.5, a no-CD exe, anything else) is backed up byte for byte and restored by the uninstaller. Other exe-level mods are not kept while the update is installed.
- The installer refuses, changing nothing, only when the folder is clearly not a CM 03/04 folder, the game is running, or files are not writable. An unusual exe length or database header only gives a warning.

### Previous versions

**25.0.0** was the first public release: players and staff from Football Manager 26 data (about 148,000 players and about 47,000 staff), current club names, stadiums and finances, 28 nations with real 2025/26 divisions and cups (14 other nations are hidden), modern squad rules, 2025/26 foreign-player limits, updated EU flags, national-team managers, African Cup of Nations and year fixes, a Contributors screen, and a single installer with backup, verification and uninstaller.

**25.0.1** was a complete installer that works with the official 4.1.5 exe and no-CD exes, with friendly-match substitutions and the 2D match speed fixed.

**25.0.2** added an update notice: a small helper that, when the game starts, looks (at most once a day) at the project's release page and tells you when a newer version exists.

**25.0.3** added a speed-up runtime (a type-cast cache and a history-file handle cache in a small replacement of the game's runtime library, about 1.4x in the transfer window) that can be switched off in `cm_proxy.cfg`.

**25.1.0** brought the modern UEFA formats: a 36-club league phase for the Champions League, Europa League and Conference League, multi-round qualifying paths, the 2026/27 access list from the association coefficients, a UEFA Club Coefficients screen, European prize money and competition history. It needs a new game.

**25.1.1** fixed the league-phase prize money that was paid several times per match, the Slovak division calendars, a rare Serie C Cup crash in a new game with Italy and the Argentine second division's second half-season, and made the update notice offer only versions of your own version line. Saves of 25.1.0 load.

**25.1.2** added a Positions pitch to the player profile: a small pitch with coloured dots shows where a player can play, from natural to cannot play. Saves of 25.1.1 load.

## Install

You need a CM 03/04 installation updated to 4.1.5 (the official 4.1.5 patch, or a no-CD exe: any exe works) on Windows 10 or 11. The game folder must contain `cm0304.exe` and `data\db` with the four database files. Close the game and the editor first.

1. Download the installer below.
2. Run it and accept the administrator prompt. Windows may warn about an unknown publisher (SmartScreen): the installer is not code-signed.
3. Choose the folder containing `cm0304.exe` and let setup finish.

**Installing 26.0.0:** run the installer on your CM 03/04 4.1.5 game folder, also when 25.x is installed there. The installer backs up your own files first, replaces `cm0304.exe`, the database and the menu / profile screens, adds the new data and picture files and verifies every file. Then **start a NEW game**.

**Saves:** saves made with 25.x, with earlier versions or with the original game do not load in 26.0.0. Nothing is deleted: they stay in `user data\games`.

**Settings:** options of your 25.x game (window, screen, manager profiles) do not carry over; the game starts in full screen. To play in a window untick 'Full Screen' under Preferences > Display Settings, or start `cm0304.exe` with the switch `-windowed`. The 25.x game keeps its own options.

**Keeping 25.x as well:** install 26.0.0 into a copy of your game folder (the installer works on any folder that contains `cm0304.exe`), or go back to 25.x with the uninstaller.

**Going back to 25.x:** run `Uninstall CM 03-04 26.0.0.exe` from the game folder first (it restores your original files), then the 25.x installer from the Releases page. Your 25.x saves are still in `user data\games`.

**Update notice:** the helper (`CM0304-UpdateCheck.exe`, version 1.1.0) only offers newer versions of your own version line: a 26.x game is told about 26.x versions only.

**Uninstall:** originals are backed up to `backup_pre_v25` in your game folder (an old backup from an earlier install is archived as `backup_pre_v25_old_<timestamp>` instead of blocking). Run `Uninstall CM 03-04 26.0.0.exe` in the game folder, or the setup with `/uninstall`. It restores everything, then removes the backup folder and the uninstaller itself.

## Checksum

`CM0304-Modern-26.0.0-Setup.exe` (39,268,864 bytes)

SHA-256: `6D7AF568A329E58A773F9021C067EA3C6C9DE2BE64250EB2105EF6222B9A485F`

Check it with PowerShell: `Get-FileHash .\CM0304-Modern-26.0.0-Setup.exe`

## Known issues

- 12 nations are not selectable (Serbia and Montenegro, Australia, Japan, Mexico, Colombia, Indonesia, South Korea, Hong Kong, South Africa, India, China PR, Singapore). Their clubs exist as foreign clubs, with rosters from the older Football Manager 26 data.
- Lower-division clubs that have no page in the new database keep the facts of the older database. About 14,000 young, low-profile players have estimated attributes: the new database holds none for them until a game starts.
- The economy (wages, prize money) is unchanged. Some clubs have generated squads and some clubs have no manager. Reserve/B teams cannot be represented; youth teams are empty; squad numbers are not set.
- Competition histories are updated for the 30 nations (see the changelog); the histories of other competitions are still the original ones from 2003.
- The European places of 2026/27 are worked out from the real 2025/26 results; a few clubs can differ from the real lists.
- Creating a new game with many nations takes several minutes (10 to 12 minutes with all 30 nations on our test machine).

Full list: <https://cm0304-modern.github.io/cm0304-modern/known-issues>

## Bugs

Report problems with the issue forms. For crashes please attach a minidump: <https://cm0304-modern.github.io/cm0304-modern/report-a-bug>
