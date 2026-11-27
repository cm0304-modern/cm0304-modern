# CM 03/04 Modern 26.0.5

A fan-made, unofficial update that brings Championship Manager 03/04 (4.1.5) into the **2026/27** football world. Not affiliated with or endorsed by the original developers or publishers. The installer contains a modified game executable, data files, a small update helper and a speed-up runtime library, and no other game files.

26.0.5 is a **complete installer**: it contains the full database and every change, so you can install it straight onto a CM 03/04 4.1.5 game. You do **not** need to install 25.x first. **It is the 2026/27 game**: saves made with 25.x or earlier versions do not load in it. The 2025/26 game (25.x) stays available on the Releases page and is not changed by this release.

## Changelog

### Fixed

- **Player career histories.** In 26.0.4 the History tab of most players showed the career of a different player: the history files shipped with 26.0.4 had been built for the player numbering of 26.0.3. They now match the players: 903,879 season rows for 120,741 players, and 6,272 more players have a history than before.

### Added

- **National team managers from the Football Manager 27 database.** 188 national teams now have a manager read from the Football Manager 27 database (179 in 26.0.4). Compared with 26.0.4 the database names a different manager for 82 teams (for example France: Zidane, Germany: Klopp, Italy: Mancini, Portugal: Jorge Jesus, Holland: Xavi, Belgium: van Bommel, Scotland: Pocognoli, Croatia: Bilic), a manager for 28 teams that had none (for example the Netherlands Antilles: Advocaat) and nobody for 16 teams: among them Mexico, Turkey and Ghana, where the game generates a manager when a new game starts, because the database has none. For nine of the managers it names, the database holds no ability data (see Known); six of those nine are among the 82 and 28 teams above, so the game generates the manager there. In a new game 84 teams keep their 26.0.4 manager, 78 get a different one and 26 get one where there was none (188 in all); Ethiopia, Chinese Taipei, Guyana and Vanuatu lose the real manager they had in 26.0.4.
- **Contributors.** The Contributors list in the community info screen now shows a second supporter.

### Changed

- The version label is now 26.0.5. Besides the people and server database (national team managers), the three player-history files and the community info screen, nothing differs from 26.0.4: the other database files, the other screens and the game programme are those of 26.0.4.

### How the installer treats your files

- The installer **replaces `cm0304.exe`** with our modified executable. It is part of the update: it carries the rule changes (substitutes, foreign-player limits, hidden nations, match speeds, the UEFA formats, year fixes, the 26/27 texts). No CD is needed afterwards.
- Your own exe (official 4.1.5, a no-CD exe, anything else) is backed up byte for byte and restored by the uninstaller. Other exe-level mods are not kept while the update is installed.
- The installer refuses, changing nothing, only when the folder is clearly not a CM 03/04 folder, the folder holds the 4.x update, the game is running, or files are not writable. An unusual exe length or database header only gives a warning.

### Previous versions

**25.0.0** was the first public release: players and staff from Football Manager 26 data (about 148,000 players and about 47,000 staff), current club names, stadiums and finances, 28 nations with real 2025/26 divisions and cups (14 other nations are hidden), modern squad rules, 2025/26 foreign-player limits, updated EU flags, national-team managers, African Cup of Nations and year fixes, a Contributors screen, and a single installer with backup, verification and uninstaller.

**25.0.1** was a complete installer that works with the official 4.1.5 exe and no-CD exes, with friendly-match substitutions and the 2D match speed fixed.

**25.0.2** added an update notice: a small helper that, when the game starts, looks (at most once a day) at the project's release page and tells you when a newer version exists.

**25.0.3** added a speed-up runtime (a type-cast cache and a history-file handle cache in a small replacement of the game's runtime library, about 1.4x in the transfer window) that can be switched off in `cm_proxy.cfg`.

**25.1.0** brought the modern UEFA formats: a 36-club league phase for the Champions League, Europa League and Conference League, multi-round qualifying paths, the 2026/27 access list from the association coefficients, a UEFA Club Coefficients screen, European prize money and competition history. It needs a new game.

**25.1.1** fixed the league-phase prize money that was paid several times per match, the Slovak division calendars, a rare Serie C Cup crash in a new game with Italy and the Argentine second division's second half-season, and made the update notice offer only versions of your own version line. Saves of 25.1.0 load.

**25.1.2** added a Positions pitch to the player profile: a small pitch with coloured dots shows where a player can play, from natural to cannot play. Saves of 25.1.1 load.

**26.0.0** was the 2026/27 game: a new database built from Football Manager 27 data for 30 nations (the 28 nations of 25.x plus Russia and Israel), the real 2025/26 results behind the 2026/27 European places, history screens up to 2025/26 and the 26/27 texts. It needed a new game: saves of 25.x do not load.

**26.0.1** added the Simulate button to the 'Proceed to match?' window and coloured attribute values (white 1-10, yellow 11-15, green 16-20) in the player profile. Saves of 26.0.0 load.

**26.0.2** was a new-game update: player career histories, tournament and club-cup histories, curated club and national-team records, Basque players, realistic contract end dates and a proportional Positions pitch. Saves of 26.0.1 load but do not get the new data.

**26.0.3** was a new-game update: reserve and youth squads, spoken languages from the career history and join dates from the career history. Saves of 26.0.2 load but do not get the new data.

**26.0.4** was a new-game update: real referees, manager formations and tactics, loans, first-team squads, a running-season column in the UEFA Club Coefficients screen, the Brazilian foreign-player rule and the first supporter in Contributors, with all squad, staff, club and stadium data read from the Football Manager 27 database. Saves of 26.0.3 load but do not get the new data. Its player-history files belonged to another player numbering; 26.0.5 replaces them.

## Install

You need a CM 03/04 installation updated to 4.1.5 (the official 4.1.5 patch, or a no-CD exe: any exe works) on Windows 10 or 11. The game folder must contain `cm0304.exe` and `data\db` with the four database files. Close the game and the editor first.

1. Download the installer below.
2. Run it and accept the administrator prompt. Windows may warn about an unknown publisher (SmartScreen): the installer is not code-signed.
3. Choose the folder containing `cm0304.exe` and let setup finish.

**Upgrading from 26.0.4, or reinstalling:** run the new installer on the same game folder. `cm0304.exe` (version label), the people and server database, the three player-history files (`pl_hist_dt.dat`, `pl_hist_id.dat` and `pl_hist_index.dat` in `data\db`) and the community info screen are replaced; your old saves are not touched. Saves made with 26.0.4 get the corrected careers in place (tested on a game-start save) but keep their old national team managers; start a NEW game to get the new national team managers and the other data changes (recommended, not required).

**Upgrading from 26.0.3 or earlier:** run the installer as before and start a NEW game: saves made with 26.0.3 or older show wrong careers with the new history files (in 26.0.4 they still showed the right ones: keep 26.0.4 until you have finished such a save).

**Upgrading from 25.x or earlier:** run the installer as before, then start a NEW game.

**Going back to 26.0.4:** run `Uninstall CM 03-04 26.0.5.exe` first, then the 26.0.4 installer. A copy back by hand must restore `cm0304.exe`, `data\db\people_db.dat`, `data\db\server_db.dat`, all three history files (`pl_hist_dt.dat`, `pl_hist_id.dat`, `pl_hist_index.dat`) and `data\screens\community info.xml`; the exe alone is not enough.

**Uninstall:** originals are backed up to `backup_pre_v25` in your game folder (an old backup from an earlier install is archived as `backup_pre_v25_old_<timestamp>` instead of blocking). Run `Uninstall CM 03-04 26.0.5.exe` in the game folder, or the setup with `/uninstall`. It restores everything, then removes the backup folder and the uninstaller itself.

## Checksum

`CM0304-Modern-26.0.5-Setup.exe` (45,210,624 bytes)

SHA-256: `63023F9CA4ADE4A6BE1FAEEFA35E4C10CC39C2223E680AB2BD4D1CAC5A82159E`

Check it with PowerShell: `Get-FileHash .\CM0304-Modern-26.0.5-Setup.exe`

## Known issues

- 12 nations are not selectable (Serbia and Montenegro, Australia, Japan, Mexico, Colombia, Indonesia, South Korea, Hong Kong, South Africa, India, China PR, Singapore). Their clubs exist as foreign clubs, with rosters from the older Football Manager 26 data.
- Lower-division clubs that have no page in the new database keep the facts of the older database. About 14,000 young, low-profile players have estimated attributes: the new database holds none for them until a game starts.
- The economy (wages, prize money) is unchanged. Some clubs have generated squads and some clubs have no manager. Reserve, B and youth teams get their players only where the club already has such a team in the game database; at other clubs these players stay in the first-team squad. Squad numbers are not set.
- Competition histories are updated for the 30 nations (see the changelog); the histories of other competitions are still the original ones from 2003.
- The European places of 2026/27 are worked out from the real 2025/26 results; a few clubs can differ from the real lists.
- Creating a new game with many nations takes several minutes (10 to 12 minutes with all 30 nations on our test machine).
- Not in this release: African competitions.
- National team managers: in a new game the preferred formation of every national team manager shows Unknown (the game links a manager's formation through his club, and a national team manager has none); 33 of the 188 have no attribute values in the database; for 9 nations the database names a manager without any ability data (Djibouti, Ethiopia, Lesotho, Seychelles, Chinese Taipei, Guyana, Andorra, Vanuatu, Guam), so the game generates the manager there. In all, 42 of the 230 national teams, among them historic ones such as the Soviet Union, get a generated manager.
- Reserve squads exist only where the club already has such a team in the game database, and the game still tops teams up with its own filler players and may re-sort them by age at the start of a game.

Full list: <https://cm0304-modern.github.io/cm0304-modern/known-issues>

## Bugs

Report problems with the issue forms. For crashes please attach a minidump: <https://cm0304-modern.github.io/cm0304-modern/report-a-bug>
