# CM 03/04 Modern

A fan-made, unofficial update that brings Championship Manager 03/04 (version 4.1.5) into the 2025/26 football world.

**Current version: 25.1.1** - [Download from Releases](https://github.com/cm0304-modern/cm0304-modern/releases/latest)

Pages: [FAQ](faq.md) | [Nations](nations.md) | [Known issues](known-issues.md) | [Update notice](update-notice.md) | [Changelog](changelog.md) | [Report a bug](report-a-bug.md) | [Screenshots](screenshots.md)

## Install guide

**Before you start**

- You need your own Championship Manager 03/04, **version 4.1.5** (updated with the official 4.1.5 patch, or a no-CD exe: any exe works), on Windows 10 or 11. The game folder must contain `cm0304.exe` and `data\db` with the four database files.
- Close the game and the editor.
- Have about 700 MB of free disk space.

**Steps**

1. Download `CM0304-Modern-25.1.1-Setup.exe` from the release page. You can check the download with PowerShell: `Get-FileHash .\CM0304-Modern-25.1.1-Setup.exe` and compare with the SHA-256 shown on the release.
2. Run the installer and accept the administrator prompt. If Windows SmartScreen says "unknown publisher", that is because the installer is not code-signed.
3. Choose the folder that contains `cm0304.exe`. Setup lists what it will change, backs up the originals to `backup_pre_v25`, installs and verifies every file.
4. Start the game and begin a **new game**. Saves from the original game or from versions before 25.1.0 do not work with this version (saves of 25.1.0 do).

**The installer replaces `cm0304.exe`** with our modified executable (it carries the rule changes). Your own exe is backed up byte for byte. No CD is needed afterwards.

**Upgrading from 25.1.0, or reinstalling:** run the new installer on the same game folder. Only `cm0304.exe` and the update helper `CM0304-UpdateCheck.exe` are replaced; the database files are identical, so your **25.1.0 saves keep working** and no new game is needed (only the Argentine fix needs a new game, see "What's new in 25.1.1"). If you switched the update notice off (`update-check.disabled`), it stays off.

**Upgrading from 25.0.0-25.0.3:** run the new installer on the same game folder (two new data files are added: `data\db\club_coef.dat` and `data\db\ccs_extra.dat`). **Start a NEW game afterwards: saves made with 25.0.x do not load in 25.1.x** (keep them and use the uninstaller if you want to go back).

If the installer refuses, it has not changed anything. It refuses only when the folder is clearly not a CM 03/04 folder, the game is running or files are not writable.

**Uninstall:** run `Uninstall CM 03-04 25.1.1.exe` from your game folder. It restores your original files (your own exe included) from the backup and then removes the backup folder and itself.

## Which version do I need? (two lines)

CM 03/04 Modern has two version lines, because the 2025/26 game and the planned 2026/27 game are different games:

- **25.x - the 2025/26 game** (this page): 2025/26 squads, clubs and competitions. It keeps receiving bug fixes (25.1.1 and later). Download it from the [latest release](https://github.com/cm0304-modern/cm0304-modern/releases/latest).
- **26.x - the 2026/27 game** (planned, not released yet): the next season's squads, clubs and competitions. It is a separate game: it needs a **new game**, and saves of one line do not load in the other. When it comes out it will be listed on the [Releases page](https://github.com/cm0304-modern/cm0304-modern/releases) under its own `v26` tag; the "latest release" link above stays on the 25.x line.

The update notice only tells you about newer versions of **your own line**: 25.x players hear about 25.x versions, 26.x players about 26.x versions. To keep a 25.x game playable next to 26.x, install 26.x into a copy of your game folder (the installer works on any folder that contains `cm0304.exe`).

## What's new in 25.1.1

**A bug-fix update of 25.1.0.** Your 25.1.0 saves keep working; no new game is needed (only the Argentine fix needs one, see below).

- **European prize money is paid once per match.** In 25.1.0 the league-phase prize money of the Champions League, Europa League and Conference League was paid several times per match when the League Table tab of the live match screen was open (every refresh of the tab paid every club of the night again, so the inbox filled with the same message). It is now paid once per match, when the match is decided; the amounts are unchanged. Matches you do not watch, or watch with that tab closed, were always paid correctly.
- **The Slovak divisions play exactly the matches they declare.** The calendars of the First Division (12 clubs, 33 matches each) and the Second Division (14 clubs, 26 matches each) had 36 and 30 dates; they now have 33 and 26 matchdays. In an existing save the current season keeps its old calendar and the next season is created with the right one.
- **A rare crash of the Serie C Cup is fixed.** In about 1 in 200 new games with Italy the knock-out stage of the Serie C Cup was built one team short and the game crashed on 10-11 September when it drew the first round. A save whose Serie C Cup was already built too short cannot be repaired.
- **The Argentine second division now completes its season.** The Primera Nacional (36 clubs) had only 21 of the 35 matchdays in its second half-season, so the division could never finish and the Argentine leagues did not move on to the next season. It now has all 35 matchdays and the Argentine leagues finish their season and move to the next one; the Argentine second division stays at 36 clubs and the Premier Division at 30.
- **The update notice stays on your version line.** It only offers newer versions of the line you have installed (25.x offers 25.x), so a separate 26.x game is never offered to a 25.x player. See [the update notice](update-notice.md).

**Argentina is fixed for new games only.** The calendar of a season is stored in the save: a save made with an earlier version keeps its old Argentine second-division calendar, in that save the division still cannot complete its season and the Argentine leagues stay stuck. Start a new game for the corrected structure.

Not repaired: money that a 25.1.0 save already received through the prize-money bug stays in that save. Until you update, do not open the League Table tab of the match screen during a live European league-phase match.

## What's new in 25.1.0

**The three European competitions now follow the modern UEFA formats.** Start a NEW game: saves from 25.0.x do not load in 25.1.0.

- **Champions League, Europa League and Conference League** each play a 36-club league phase (Swiss-system draw with pots; 8, 8 and 6 matchdays) with the real tie-break order. The best 8 go straight to the round of 16, places 9 to 24 play a knockout play-off round, then quarter-finals, semi-finals and the final. No away-goals rule. The Super Cup is played between the Champions League and Europa League winners.
- **Qualifying paths.** Each competition has a main path and a champions path, and clubs that lose in qualifying drop into the next competition's qualifying or league phase, like in the real game. The rounds are listed one column per round on the competition screens, with the path named (Champions Path / League Path / Main Path); the draw message arrives once per draw and "View draw" opens that round.
- **Who gets in is calculated from the real world.** A new game starts from the real 2024/25 season end (league positions and domestic cup winners decide the 2025/26 places). At every season rollover the number of clubs each association sends to each round is worked out from the association coefficients (the five seasons before the closing one), with the European Performance Spots and the title-holder rules. Associations without a selectable league do not send clubs.
- **UEFA coefficients.** Real association coefficients 2020/21 to 2024/25 and the 2024+ points rule; the UEFA Coefficients screen shows the new values. A new screen, **UEFA Club Coefficients** (Competitions > Europe), lists the top 200 clubs over the last five seasons with the total.
- **European prize money** follows the 2026/27 UEFA distribution (scaled by 0.75): participation fees, win and draw bonuses, league-phase ranking, knockout rounds and the Super Cup, paid through your club's normal finances.
- **History and looks.** European competition histories from 2004 to 2025 (the Conference League from 2022), the new competition and round names, a picture for each competition in the title bar of its screen, and fixed header colours (dark blue, orange, green) instead of the last winner's colours.
- **Squad registration** for the European qualifying rounds works from the first round: the first deadline is before the first qualifying round, and a game that starts after it asks for your squad list on the first day.

Known gaps: the value pillar of the UEFA distribution is not modelled, some provisional marks in the league-phase tables appear only for clinched positions, and a few tie-break details are simplified. See [known issues](known-issues.md).
## What came with 25.0.3

- **The game runs faster.** A type-cast cache and a history-file handle cache sit in a small replacement of the game's own runtime library. In our tests this made the transfer window about 1.4 times faster. The game data is unchanged, so your 25.0.x saves keep working.
- The installer now also puts three small files in your game folder: `msvcr71.dll` (the speed-up, your own file is backed up first), `MSVCR71_real.dll` (your original runtime, kept because the speed-up forwards to it) and `cm_proxy.cfg` (optional settings). The uninstaller puts your own file back. See the [FAQ](faq.md) for how to switch the speed-up off.

## What came with 25.0.2

- **A friendly "new version" notice.** When you start the game, a small helper looks at this project's releases page, at most once a day. If a newer version is out, a short window tells you and asks whether you want to open the download page. Nothing is downloaded or changed for you, and nothing about you or your game is sent.
- **You are in control.** The installer has a box "Check for updates when the game starts". Untick it and the notice never appears. You can also switch it off later. Details: [the update notice](update-notice.md).
- The game data is the same as in 25.0.1, so your 25.0.x saves keep working.
- Note: the installer now also puts a small program, `CM0304-UpdateCheck.exe`, in your game folder. It is not code-signed, so antivirus or Windows may mention it. It is safe to delete (see [known issues](known-issues.md)).

## What came with 25.0.1

- Friendly matches allow 12 substitutions again (25.0.0 limited them to 5 by mistake).
- The 2D match speed option now really controls the pace.
- The installer now works with the official 4.1.5 exe (25.0.0 refused it) and with no-CD exes; reinstalling and uninstalling work cleanly. You can install it straight over 25.0.0.

## What came with 25.0.0

- A real 2025/26 world built from Football Manager 26 data: about 148,000 players and about 47,000 staff, with current club names, stadiums and finances.
- 28 nations with real 2025/26 divisions and cups (see [nations](nations.md)).
- Modern squad rules: 12 named players and 5 substitutes used.
- 2025/26 foreign-player limits per nation, updated EU flags, national-team managers.
- African Cup of Nations and year-related fixes.
- A Contributors screen.

The full list is in the [changelog](changelog.md). Please also read the [known issues](known-issues.md).

## Support

Bugs and requests: [GitHub Issues](https://github.com/cm0304-modern/cm0304-modern/issues/new/choose). Tips on what to include: [report a bug](report-a-bug.md).

*Fan-made and unofficial. Not affiliated with or endorsed by the original developers or publishers. The installer contains a modified game executable and data files, and no other game files.*
