# CM 03/04 Modern 26.0.1

A fan-made, unofficial update that brings Championship Manager 03/04 (4.1.5) into the **2026/27** football world. Not affiliated with or endorsed by the original developers or publishers. The installer contains a modified game executable, data files, a small update helper and a speed-up runtime library, and no other game files.

26.0.1 is a **complete installer**: it contains the full database and every change, so you can install it straight onto a CM 03/04 4.1.5 game. You do **not** need to install 26.0.0 or 25.x first. **It is the 2026/27 game**: saves made with 26.0.0 load in 26.0.1; saves made with 25.x or earlier versions do not (start a new game if you come from 25.x). The 2025/26 game (25.x) stays available on the Releases page and is not changed by this release.

## Changelog

### Added

- **Simulate.** The 'Proceed to match?' window that opens when you click Go To Match has a new button, **Simulate**, to the left of No. It plays that one match with your current squad and tactics, without the match screen, and gives control back at midnight (0:00) after the match day. The **Last Match** page of the simulated match then opens by itself, with the score, the incidents and the fixture, so you see the result at once. Yes and No work as before. If a selected player cannot play (banned or injured), the game shows its usual notice first and that window has no Simulate: replace the player and click Go To Match again.
- **Three-colour attribute values on the player profile.** The values of the attributes are coloured in three steps: white for 1 to 10, yellow for 11 to 15 and green for 16 to 20. The attribute names stay white. Before, every value was yellow, with a lighter yellow from 15.

### Changed

- The version label is now 26.0.1.

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

**26.0.0** was the 2026/27 game: a new database built from Football Manager 27 data for 30 nations (the 28 nations of 25.x plus Russia and Israel), the real 2025/26 results behind the 2026/27 European places, history screens up to 2025/26 and the 26/27 texts. It needed a new game: saves of 25.x do not load.

## Install

You need a CM 03/04 installation updated to 4.1.5 (the official 4.1.5 patch, or a no-CD exe: any exe works) on Windows 10 or 11. The game folder must contain `cm0304.exe` and `data\db` with the four database files. Close the game and the editor first.

1. Download the installer below.
2. Run it and accept the administrator prompt. Windows may warn about an unknown publisher (SmartScreen): the installer is not code-signed.
3. Choose the folder containing `cm0304.exe` and let setup finish.

**Upgrading from 26.0.0, or reinstalling:** run the new installer on the same game folder. `cm0304.exe` and the two screen files are replaced; the database files and everything else are left as they are, and your saves keep working. Your own copy of the 'Proceed to match?' window is added to the backup first.

**Upgrading from 25.x or earlier:** run the installer as before, then **start a NEW game**: saves of 25.x and earlier do not load in the 2026/27 game.

**Saves:** a save made with 26.0.0 loads in 26.0.1.

**Uninstall:** the uninstaller puts the original player profile screen and the original 'Proceed to match?' window back, together with the rest of your original files.

**Going back to 26.0.0:** run `Uninstall CM 03-04 26.0.1.exe` first, then the 26.0.0 installer. The 26.0.0 installer does not know the new `data\panels\dialog.xml`: run alone over 26.0.1 it puts its own `cm0304.exe` and player profile screen back and leaves that file, which does no harm without the new `cm0304.exe`.

**Uninstall:** originals are backed up to `backup_pre_v25` in your game folder (an old backup from an earlier install is archived as `backup_pre_v25_old_<timestamp>` instead of blocking). Run `Uninstall CM 03-04 26.0.1.exe` in the game folder, or the setup with `/uninstall`. It restores everything, then removes the backup folder and the uninstaller itself.

## Checksum

`CM0304-Modern-26.0.1-Setup.exe` (39,270,400 bytes)

SHA-256: `9FFE91F9838A17B059FF04A58100EBE4C2E1C59D01D9DB1E4701C1FF102616AC`

Check it with PowerShell: `Get-FileHash .\CM0304-Modern-26.0.1-Setup.exe`

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
