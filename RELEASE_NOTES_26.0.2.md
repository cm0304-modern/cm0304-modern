NEW GAME REQUIRED: 26.0.2 stores new data in every save (player career histories, tournament and club-cup histories, curated club and national-team records, a new contract-end spread); saves made with 26.0.1 still load but do not get it

# CM 03/04 Modern 26.0.2

A fan-made, unofficial update that brings Championship Manager 03/04 (4.1.5) into the **2026/27** football world. Not affiliated with or endorsed by the original developers or publishers. The installer contains a modified game executable, data files, a small update helper and a speed-up runtime library, and no other game files.

26.0.2 is a **complete installer**: it contains the full database and every change, so you can install it straight onto a CM 03/04 4.1.5 game. You do **not** need to install 25.x first. **It is the 2026/27 game and needs a NEW game**: saves made with 25.x or earlier versions do not load in it. The 2025/26 game (25.x) stays available on the Releases page and is not changed by this release.

## Changelog

### Added

- **Tournament histories.** The history screens now list the winners of the national-team tournaments and of the continental and Inter-Continental club cups, including the 2025 editions (Paris Saint-Germain and Flamengo in the Inter-Continental Cup). The 2025 Africa Cup of Nations is shown with Morocco as winner, as decided by the CAF Appeal Board on 17 March 2026; the ruling of the Court of Arbitration for Sport is still pending, and a later update may follow it.
- **Player career histories.** The History tab of the players shows their real career: 864,727 season rows for 114,469 players. Clubs that are not loaded in your world show as Unknown Club.
- **Club and national-team records.** All 148 curated club records now apply, including RB Leipzig (most league appearances and/or goals, as of November 2026), and 175 nations have their most-capped player (as of July 2026); other clubs start without a stored record.
- **Basque players.** Players with Basque roots (born in the Basque Country or Navarre, or in the current Athletic squads) can again be signed by the clubs with a Basque-only policy, such as Athletic Club.
- **Proportional Positions pitch.** The pitch of the player profile is drawn in the proportions of the real pitch. 55 pre-rendered sizes (`pitch_r46.png` to `pitch_r100.png`) are installed next to the pitch pictures, and the game takes the one that fits the window.

### Changed

- Contract end dates of the players are spread over a realistic range of years instead of ending in the same few seasons. The game accepts contract end years up to 2048.
- The update helper is version 1.2.0: it tells you only about newer releases of your own line (26.x), and it knows the separate 4.x line.
- The version label is now 26.0.2.

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

## Install

You need a CM 03/04 installation updated to 4.1.5 (the official 4.1.5 patch, or a no-CD exe: any exe works) on Windows 10 or 11. The game folder must contain `cm0304.exe` and `data\db` with the four database files. Close the game and the editor first.

1. Download the installer below.
2. Run it and accept the administrator prompt. Windows may warn about an unknown publisher (SmartScreen): the installer is not code-signed.
3. Choose the folder containing `cm0304.exe` and let setup finish.

**Upgrading from 26.0.1, or reinstalling:** run the new installer on the same game folder, then **start a NEW game** for the new data. The database files, `cm0304.exe`, the update helper and the 55 new pitch pictures are replaced or added; your old saves are not touched.

**Upgrading from 25.x or earlier:** run the installer as before, then start a NEW game.

**Saves:** a save made with 26.0.1 loads in 26.0.2 but has none of the new data.

**Going back to 26.0.1:** run `Uninstall CM 03-04 26.0.2.exe` first, then the 26.0.1 installer. The 26.0.1 installer does not know the 55 new pictures: run alone over 26.0.2 it leaves them, which does no harm without the new `cm0304.exe`.

**Uninstall:** originals are backed up to `backup_pre_v25` in your game folder (an old backup from an earlier install is archived as `backup_pre_v25_old_<timestamp>` instead of blocking). Run `Uninstall CM 03-04 26.0.2.exe` in the game folder, or the setup with `/uninstall`. It restores everything, then removes the backup folder and the uninstaller itself.

## Checksum

`CM0304-Modern-26.0.2-Setup.exe` (45,122,048 bytes)

SHA-256: `4624F52B0D4A7F29062354480DC5C7F4D46E8F92E6F4EACA7CAD104CB26BBD7E`

Check it with PowerShell: `Get-FileHash .\CM0304-Modern-26.0.2-Setup.exe`

## Known issues

- 12 nations are not selectable (Serbia and Montenegro, Australia, Japan, Mexico, Colombia, Indonesia, South Korea, Hong Kong, South Africa, India, China PR, Singapore). Their clubs exist as foreign clubs, with rosters from the older Football Manager 26 data.
- Lower-division clubs that have no page in the new database keep the facts of the older database. About 14,000 young, low-profile players have estimated attributes: the new database holds none for them until a game starts.
- The economy (wages, prize money) is unchanged. Some clubs have generated squads and some clubs have no manager. Reserve/B teams cannot be represented; youth teams are empty; squad numbers are not set.
- Competition histories are updated for the 30 nations (see the changelog); the histories of other competitions are still the original ones from 2003.
- The European places of 2026/27 are worked out from the real 2025/26 results; a few clubs can differ from the real lists.
- Creating a new game with many nations takes several minutes (10 to 12 minutes with all 30 nations on our test machine).
- Not in this release: African competitions.

Full list: <https://cm0304-modern.github.io/cm0304-modern/known-issues>

## Bugs

Report problems with the issue forms. For crashes please attach a minidump: <https://cm0304-modern.github.io/cm0304-modern/report-a-bug>
