# Changelog

## 26.0.1

**Added**

- **Simulate.** The 'Proceed to match?' window that opens when you click Go To Match has a new button, **Simulate**, to the left of No. It plays that one match with your current squad and tactics, without the match screen, and gives control back at midnight (0:00) after the match day. The **Last Match** page of the simulated match then opens by itself, with the score, the incidents and the fixture, so you see the result at once. Yes and No work as before. If a selected player cannot play (banned or injured), the game shows its usual notice first and that window has no Simulate: replace the player and click Go To Match again.
- **Three-colour attribute values on the player profile.** The values of the attributes are coloured in three steps: white for 1 to 10, yellow for 11 to 15 and green for 16 to 20. The attribute names stay white. Before, every value was yellow, with a lighter yellow from 15.

**Changed**

- The version label is now 26.0.1.

**26.0.1 adds the Simulate button and the three-colour attribute values.** The database files and the update helper are identical to 26.0.0; only `cm0304.exe` and two screen files change: the player profile screen (`data\panels\player profile.xml`) and the 'Proceed to match?' window (`data\panels\dialog.xml`, new in this update). **Saves made with 26.0.0 load in 26.0.1.** Saves made with 25.x or earlier do not belong to the 2026/27 game: start a NEW game for those. Installer: `CM0304-Modern-26.0.1-Setup.exe`, 39,270,400 bytes, SHA-256 `AF3AE4C8508CB229FC9E22F0DD93ED7CCABA95955918EBF223D8209100F16200`.

## 26.0.0

**Added**

- **The 2026/27 season.** A new game now starts in July 2026 (Sunday 12 July 2026 when all 30 nations are ticked). Players, ratings, contracts, loans, staff, club reputations, finances, facilities and kit colours are rebuilt from the Football Manager 27 database for 30 nations: the 28 nations of 25.x plus Russia and Israel. The database holds more than 140,000 players and more than 48,000 staff.
- **Russia and Israel are playable.** Both can be ticked on the new-game screen: Russia with a 16-club Premier League and an 18-club FNL, Israel with a 14-club Premier League and a 16-club Liga Leumit. Israel sends clubs to the European competitions; Russia sends nobody. The other 12 nations that were hidden in 25.x stay hidden (see Known issues).
- **League structures of 2026/27.** The Turkish second division (TFF 1. Lig) has 20 clubs, the Welsh Cymru Premier 16, the Northern Irish Championship 16, the Russian FNL 18, the Israeli Premier League 14 and Liga Leumit 16. The promotion and relegation of the 2025/26 season are applied: the first divisions of the 30 nations hold their real 2026/27 clubs where the game has them.
- **Real 2025/26 final tables, European places and coefficients.** First-division clubs start with their real 2025/26 final positions, and the real 2025/26 cup winners are known to the game, so the 2026/27 places in the Champions League, Europa League and Conference League are worked out from the real results. The UEFA association and club coefficients carry the real points up to and including 2025/26, and the UEFA calendar is the real 2026/27 one (for example the Super Cup on 12 August 2026).
- **History up to 2025/26.** For the 30 nations the winners of the league, the national cup, the league cup and the super cup from 2003/04 to 2025/26 are in the history screens, with the runner-up and, for leagues, the third place wherever it is certain (editions that are disputed or were not held are left out). The European Championship 2004-2024 and the World Cup 2006-2026 winners are there, and the Euro 2028 and World Cup 2030 screens show their hosts (England and the Republic of Ireland; Morocco and Spain: the game shows at most two hosts). The European competition histories reach 2026.
- **Kit colours from the new data.** Hundreds of clubs that had no kit, or whose old colours did not match the club, now have their real colours (Alanyaspor are orange and green).
- **Loans.** More than 3,500 players start the game on loan at their loan clubs, as in the data.
- **Stadiums.** The grounds of 4,283 clubs were changed to the real stadium name and capacity (for example Arsenal at the Emirates Stadium, 60,704; FC Bayern München at the Allianz-Arena, 75,000; Juventus at the Allianz Stadium, 41,507; Ajax at the Johan Cruijff ArenA, 55,500). The old stadium-move entries of the original game that concern the clubs of the 30 nations (moves scheduled for 2026-2028) are switched off in the database.

**Changed**

- **26/27 everywhere.** The game window is titled 'Championship Manager 26/27', the Start Menu header and the Quit hint say 26/27, and the version label is 26.0.0. Competition names follow the new data (for example Süper Lig, Premier League).
- **Staff attributes are on the game's own 1-20 scale.** The attributes of coaches, scouts, physios and the other staff are converted from the source's larger scale to the 20-point scale the game uses.
- **Staff dates.** In the database every staff contract ends after the start of the game and nobody keeps the dummy birth year 1900: more than 1,000 staff whose source page gave no age have a plausible one. The game recalculates some staff dates itself when a new game starts, so the dates on the staff screens can still differ.
- **Midfield labels.** The squad list and the player profile print one midfield label per player (defensive midfield before attacking midfield before midfield), so a weaker 'accomplished' role could hide a natural one. About 11,000 such roles in the database were lowered one step, so that the natural role is the one that is shown; the Positions pitch still draws them as accomplished (light green). About 880 natural wing-backs who had no defender position now count as defenders.
- **The Positions pitch of the player profile (25.1.2) is included**, with the original attribute-group colours.
- **The prize-money fix and the calendar fixes of 25.1.1 are included**: European league-phase prize money is paid once per match, the Slovak divisions have the right number of matchdays, the rare Serie C Cup crash is fixed and the Argentine second division completes its season.

**26.0.0 is the 2026/27 game and needs a NEW game.** It has a new database and a new calendar: saves made with 25.x (or earlier) do not belong to it and must not be loaded in it; they stay in your game folder. The game keeps its settings under its own name ('Championship Manager 26/27'), so window and display options start from the defaults and **the game starts in full screen** (Preferences > Display Settings > untick 'Full Screen', or start `cm0304.exe` with `-windowed`). The 12 hidden nations keep rosters from the older Football Manager 26 data, about 14,000 young low-profile players have estimated attributes (the source database holds none until a game starts), and the economy (wages and prize money) is unchanged. The 2025/26 game (25.x) stays available on the Releases page. The update helper is version 1.1.0: a 26.x game is only told about newer 26.x versions. Installer: `CM0304-Modern-26.0.0-Setup.exe`, 39,268,864 bytes, SHA-256 `6D7AF568A329E58A773F9021C067EA3C6C9DE2BE64250EB2105EF6222B9A485F`.

## 25.1.2

**Added**

- Player profile: a Positions pitch shows where a player can play, as coloured dots (green natural, light green accomplished, yellow competent, orange unconvincing, grey cannot play); hover the pitch for a list. The pitch is drawn from seven small pictures in `data\graphics\pictures\positions`.

**Changed**

- The version label is now 25.1.2.

**25.1.2 adds the Positions pitch to the player profile.** The database files and the update helper are identical to 25.1.1; only `cm0304.exe`, the player profile screen (`data\panels\player profile.xml`) and the seven new pictures change. **Saves made with 25.1.1 load in 25.1.2** (no new game needed). Installer: `CM0304-Modern-25.1.2-Setup.exe`, 39,713,792 bytes, SHA-256 `F17FE1EA3414570E72BB164DBA53DD1CD86912EB6A137CC972ADBEF086F3C063`.

## 25.1.1

**Fixed**

- The prize money of the league phase of the Champions League, Europa League and Conference League was paid several times per match when the League Table tab of the live match screen was open: every refresh of that tab paid every club of the night again, and your inbox filled with the same message ('given $2,500,000' ten times for one match). It is now paid once per match, when the match is decided. The amounts are unchanged. Matches you do not watch, or watch with that tab closed, were always paid correctly.
- The Slovak divisions play exactly the number of matches they declare. The calendars of the First Division (12 clubs, 33 matches each) and the Second Division (14 clubs, 26 matches each) had 36 and 30 dates; they now have 33 and 26 matchdays. In an existing save the current season keeps its old calendar and the next season is created with the right one.
- A rare crash of the Serie C Cup knock-out stage on 10-11 September of a NEW game with Italy (about 1 in 200 new games with Italy) is fixed. A save whose Serie C Cup was already built too short cannot be repaired.
- The Argentine second division (Primera Nacional, 36 clubs) now completes its second half-season (35 matchdays instead of 21), so the Argentine leagues finish their season and move on to the next one; the Argentine second division stays at 36 clubs and the Premier Division at 30.

**Changed**

- The update notice only offers newer versions of the version line you have installed (25.x offers 25.x). A different major version (26.x) is a separate game and is never offered by it. The helper is now version 1.1.0.
- The version label is now 25.1.1.

**25.1.1 is a bug-fix update of 25.1.0.** The database files are identical to 25.1.0; only `cm0304.exe` and the update helper change. **Saves made with 25.1.0 load in 25.1.1** (no new game needed). Money that a save has already received through the prize-money bug stays in that save: it cannot be repaired. Until you update 25.1.0: do not open the League Table tab of the match screen during a live European league-phase match. **Argentina is fixed for new games only.** The calendar of a season is stored in the save: a save made with an earlier version keeps its old Argentine second-division calendar, in that save the division still cannot complete its season and the Argentine leagues stay stuck. Start a new game for the corrected structure. Installer: `CM0304-Modern-25.1.1-Setup.exe`, 39,704,064 bytes, SHA-256 `88163018132BC3F674CD504A83D8DA4F0FB6648C6AC3B89CEA9CC6F22133AB3D`.

## 25.1.0

**Added**

- Pictures for the Champions League, Europa League and Conference League in the title bar of their competition screens, and fixed header colours for the three competitions (dark blue, orange, green) instead of the colours of the last winner. The pictures are the three 60x60 PNG files in `data\graphics\pictures\competitions` (named by the competition id); you can replace them with your own.
- The qualifying rounds are listed one column per round on the competition screens, with the second chain labelled (Champions Path / League Path); the draw message arrives once per draw and 'View draw' opens that round.
- UEFA 2024+ competition formats: Champions League, Europa League and Conference League each play a 36-club league phase (Swiss-system draw with pots, 8 / 8 / 6 matchdays, the real tie-break order), then knockout play-offs, round of 16, quarter-finals, semi-finals and the final. The Super Cup is played between the Champions League and Europa League winners.
- Multi-round qualifying paths for all three competitions with the loser matrix between them (Champions League qualifying losers drop into the Europa League or Conference League qualifying, and so on), on the 2025/26 summer calendar.
- The 2026/27 UEFA access list: how many clubs each association sends to which round is worked out at every season rollover from the association coefficients (the five seasons before the closing one). Associations without a selectable league do not send clubs.
- Real UEFA association coefficients 2020/21-2024/25 and the 2024+ coefficient points rule (points per win/draw, elimination points, league-phase position bonuses, knockout bonuses); the UEFA Coefficients screen shows the new values.
- New screen **UEFA Club Coefficients** (Competitions > Europe): the top 200 clubs over the last five seasons with the total, from real club points plus the clubs of nations that are not part of your game.
- European prize money of the 2026/27 UEFA distribution (scaled by 0.75) for the Champions League, Europa League, Conference League and the Super Cup, paid through the clubs' normal finances.
- European competition history 2004-2025 (Champions League, Europa League, Conference League from 2022, Super Cup) and the new competition and round names.

**Changed**

- A new game starts from the real 2024/25 season end: league positions and the domestic cup winners decide who enters the 2025/26 Champions League, Europa League and Conference League (the previous champions and cup winners are no longer guessed from the era data).
- Squad registration for the European qualifying rounds: the first registration deadline is before the first qualifying round (27 June) and a game that starts after it asks for the squad list on the first day, so a human club in qualifying is no longer left with an unregistered squad.
- On the UEFA Club Coefficients screen your own club is shown in yellow and the club and nation columns use the same font.
- The version label is now 25.1.0.
- Clubs that play in a division of a real nation but had no nation of their own in the data now get the nation of their division (needed by the new access list).

**25.1.0 needs a NEW game.** Saves now hold club coefficient data (save stream version 148); saves made with 25.0.x, earlier versions or the original game are not compatible and are refused with the message 'Could not load the database'. Known gaps: the value pillar of the UEFA distribution is not modelled, some provisional marks in the league-phase tables appear only for clinched positions, and a few tie-break details (rule 10) are simplified. Installer: `CM0304-Modern-25.1.0-Setup.exe`, 39,702,528 bytes, SHA-256 `FBBB257A67F11CC5107A8959FAF84E608982A53B39F451BE3F30108589E32B7E`.

## 25.0.3

**Added**

- Speed-up: the game runs faster through a type-cast cache and a history-file handle cache (about 1.4x in the transfer window in our tests). Both caches live in a small replacement of the game's own runtime library: `msvcr71.dll` in the game folder is replaced, your original runtime is kept next to it as `MSVCR71_real.dll`, and the optional settings are in `cm_proxy.cfg`.
- You can switch the speed-up off at any time by putting the line `CM_PROXY_DISABLE=1` into `cm_proxy.cfg` (the game then behaves as before), or install without it with the `/noproxy` switch of a silent install. The uninstaller puts your own `msvcr71.dll` back byte for byte and removes the two other files.
- If your `msvcr71.dll` is not the original runtime but another valid one, the installer keeps your file as `MSVCR71_real.dll`; if it is not a usable runtime, the installer leaves it alone and installs everything else without the speed-up (the last page says so).

**Changed**

- The version label is now 25.0.3.

Database content is unchanged from 25.0.2, so existing 25.0.x saves keep working. The speed-up library is not code-signed: if your antivirus program reports it, add the game folder to its exclusions or install with `/noproxy`. Installer: `CM0304-Modern-25.0.3-Setup.exe`, 39,649,792 bytes, SHA-256 `BCC56B34CE982F4B8B3F430AC82BD25908AB559C609AA640C3C9AC04D9648B02`.

## 25.0.2

**Added**

- Update notice: when you start the game, a small helper checks the project's GitHub releases page at most once a day. If a newer version exists, a short dialog tells you and offers to open the download page. It sends no data about you or your game, and it never changes anything by itself.
- You can turn the update notice off in the installer ("Check for updates when the game starts"), with the `/noupdatecheck` switch of a silent install, or later by creating an empty file named `update-check.disabled` in the game folder (or by setting the environment variable `CM0304_NO_UPDATE_CHECK=1`).

**Changed**

- The version label is now 25.0.2.

Database content is unchanged from 25.0.1, so existing 25.0.x saves keep working. The uninstaller removes the update helper and its settings folder along with everything else. Installer: `CM0304-Modern-25.0.2-Setup.exe`, 39,419,904 bytes, SHA-256 `27EE32E75508B13D7DE15258600B3F0316AD2410F3ADFC6D1EED87F052E42E42`.

## 25.0.1

**Fixed**

- Friendly matches allow 12 substitutions again (25.0.0 wrongly limited them to 5). League and cup matches keep 12 named players and 5 substitutions used.
- The 2D match view now follows the speed option. Fast is about 3x and Very Fast about 4.5x the pace of Medium (approximate figures). Medium, Slow and Very slow stay as before.
- Installer: the 25.0.0 installer accepted only one specific 4.1.5 executable, so players with the official 4.1.5 exe (installed with the official 4.1.4 and 4.1.5 patches) were refused. The 25.0.1 installer works with the official exe and with no-CD exes.
- Installer: reinstalling after an uninstall works, and uninstalling cleans up.

**Changed**

- The installer replaces `cm0304.exe` with the modified executable (it carries the rule changes: substitutes, foreign-player limits, hidden nations, speeds, year fixes). Your own exe is backed up byte for byte and restored by the uninstaller. No CD is needed afterwards.
- A stale backup from an earlier install is archived as `backup_pre_v25_old_<timestamp>` instead of blocking the install.
- The installer refuses (changing nothing) only when the folder is clearly not a CM 03/04 folder, the game is running or files are not writable. An unusual exe length or database header only gives a warning.
- The game reports version 25.0.1.

Database content is unchanged from 25.0.0, so existing 25.0.0 saves keep working. Installer: `CM0304-Modern-25.0.1-Setup.exe`, 39,401,984 bytes, SHA-256 `97CC09DA977A93498B97E646EDB31E4E3BC2683BEB8C39577A520C4BDA61E7BB`.

## 25.0.0 - first public release

**World**

- Players and staff replaced with a 2025/26 set built from Football Manager 26 data (about 148,000 players and about 47,000 staff).
- Current club names, stadiums and finances for the supported nations.
- 28 nations with real 2025/26 divisions and cups, tested through full seasons and rollovers: England, Spain, Italy, France, Germany, Scotland, Holland, Portugal, Switzerland, Turkey, Czech Republic, Sweden, Wales, Northern Ireland, Argentina, Brazil, Norway, Croatia, Republic of Ireland, Slovakia, Austria, Denmark, Poland, Hungary, Greece, Finland, Ukraine and Belgium.
- 13 nations (Serbia and Montenegro, Australia, Japan, Russia, Mexico, Colombia, Indonesia, South Korea, Hong Kong, South Africa, India, China PR, Singapore) plus Israel are not selectable. Their clubs remain as foreign clubs with current rosters.

**Rules**

- Modern squad rules: 12 named players, 5 substitutes used.
- 2025/26 foreign-player limits per nation, where the game can express them.
- Updated EU flags.
- National-team managers.
- African Cup of Nations and year-related fixes.

**Interface**

- A Contributors screen.
- The game reports version 25.0.0.

**Installer**

- One setup program for a CM 03/04 4.1.5 installation. Checks every file, backs up the originals to `backup_pre_v25`, verifies the result, rolls back on failure, includes an uninstaller and a silent mode.
- SHA-256 of `CM0304-Modern-25.0.0-Setup.exe`: `e9c81c506b4e3e8b2b456e95873531c9e96cc557c367854c3967cb621ae00746`

See [known issues](known-issues.md) for what is not done yet.
