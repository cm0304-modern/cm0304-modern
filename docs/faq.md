# FAQ

## Do I need the original game?
Yes. This project does not include the game. You need your own CM 03/04 installation, version 4.1.5.

## I use a no-CD exe: will it work?
Yes. The installer works with any exe in a CM 03/04 4.1.5 folder, no-CD exes included. It replaces your `cm0304.exe` with our modified executable (which needs no CD) and backs up yours byte for byte. The uninstaller puts your no-CD exe back. We cannot test the installer against every game variant; if something goes wrong, please [report it](report-a-bug.md).

## I have the official 4.1.5 exe (installed with the official 4.1.4 and 4.1.5 patches)
That works in 25.0.1. The 25.0.0 installer accepted only one specific 4.1.5 executable and refused the official one; this is fixed.

## How do I upgrade from an earlier version?
Close the game and run the installer on the same game folder (the same applies to a reinstall). **To 26.0.0 from any 25.x version (or from the original game):** run the 26.0.0 installer and then start a **new game**: 26.0.0 is the 2026/27 game and saves made with 25.x or earlier do not load in it. **Inside the 25.x line:** from **25.1.1** to 25.1.2 `cm0304.exe`, the player profile screen and seven pictures change (from **25.1.0** also the update helper); the database is identical, so your **25.1.0 and 25.1.1 saves keep working**. From **25.0.x** to 25.1.x run the installer and then start a **new game**.

## What is 26.0.0? Is it a new game?
26.0.0 is the 2026/27 game: a new database (Football Manager 27 data for 30 nations, including Russia and Israel) and a new calendar, with the real 2025/26 season behind it. You need to **start a new game**; your old saves are not touched, they stay in the folder (`user data\games`) but must not be loaded in 26.0.0. See [what's new in 26.0.0](index.md#whats-new-in-2600).

## The game starts in full screen. How do I play in a window?
26.0.0 keeps its settings under its own name ("Championship Manager 26/27"), so the options of your 25.x or original game (window, display, manager profiles) do not carry over, and a fresh game starts in full screen. Open **Preferences > Display Settings** and untick **Full Screen**, or start `cm0304.exe` with the switch `-windowed` (for example add `-windowed` after the program name in the shortcut's Target). Your 25.x game keeps its own settings.

## Can I keep 25.x and 26.x on the same computer?
Yes: install 26.0.0 into a copy of your game folder (the installer works on any folder that contains `cm0304.exe`). The two games keep their settings separately; saves of one line do not load in the other. Do not install both into the same folder: the second installer would replace the first.

## How do I go back to 25.x?
Run `Uninstall CM 03-04 26.0.0.exe` from your game folder first (it restores your original files), then run the 25.x installer from the [Releases page](https://github.com/cm0304-modern/cm0304-modern/releases). Your 25.x saves are still in `user data\games`.

## Are Russia and Israel in the game?
Yes, in 26.0.0: Russia (Premier League 16 clubs, FNL 18) and Israel (Premier League 14, Liga Leumit 16) can be ticked on the new-game screen. Israel's clubs play in the European competitions; Russia sends nobody. See [nations](nations.md).

## Some young players have odd or estimated attributes. Why?
The Football Manager 27 database does not hold attributes for many young, low-profile players: the game creates them when a new game starts. We use the attributes of the older Football Manager 26 database where the same player exists there, and estimate the rest from the player's ability and position (about 14,000 players). Their attributes are plausible but not real data.

## Did wages and prize money change?
No. The economy (wages and prize money) is the same model as in 25.x; reworking it is a later project. The European prize money follows the UEFA distribution scaled as in 25.1.x.

## How long does a new game take to create?
With many nations ticked it takes several minutes: about 10 to 12 minutes with all 30 nations on our test machine.

## In 25.1.0 I got the same prize-money message many times for one match. Is that fixed?
Yes, in 25.1.1. In 25.1.0 the league-phase prize money of the Champions League, Europa League and Conference League was paid again every time the League Table tab of the live match screen refreshed, so one match could fill the inbox with the same "given $2,500,000" message and pay every club of the night many times over. Since 25.1.1 it is paid once per match, when the match is decided (the amounts are unchanged). Money that a save already received stays in that save; it cannot be repaired. If you stay on 25.1.0 for now, do not open the League Table tab during a live European league-phase match (matches you do not watch, or watch with that tab closed, were always paid correctly).

## The Argentine second division never finishes its first season. Is that fixed?
Yes, in 25.1.1 for **new games**. In 25.1.0 the Argentine second division (Primera Nacional, 36 clubs) had only 21 of the 35 matchdays it needs in its second half-season, so it could not complete its first season and the Argentine leagues did not move on to the next one. 25.1.1 gives it all 35 matchdays; the Argentine leagues now finish their season and roll over, the Argentine second division stays at 36 clubs and the Premier Division at 30. The calendar of a season is stored in the save, so a save made with an earlier version keeps its old Argentine second-division calendar and the Argentine leagues stay stuck in it: start a new game. (The Slovak divisions had a similar calendar problem, 36 and 30 dates for 33 and 26 matches per club, which 25.1.1 also fixes: a new game has 33 and 26 matchdays, an existing save gets the right calendar at its next season.)

## The game crashed on 10 or 11 September in a new game with Italy. Is that fixed?
25.1.1 fixes the cause for new games. In about 1 in 200 new games with Italy (25.1.0) the Serie C Cup knock-out stage was built one team short and the game crashed when it drew the first round on 10-11 September. A save whose Serie C Cup was already built too short cannot be repaired by the update.

## What are the coloured dots on a player's profile?
The **Positions** box (new in 25.1.2) shows the spots on the pitch a player can take, as seen from above with your own goal at the bottom. **Green** = natural, **light green** = accomplished (the game picks him there), **yellow** = competent, **orange** = unconvincing, **grey** = cannot play there. Hover over the pitch for a text list. It shows the game's own position ratings of that player; a goalkeeper only has the goalkeeper spot. See [What's new in 25.1.2](index.md).

## Which version do I need: 25.x or 26.x?
26.x is the 2026/27 game (26.0.0 is out); 25.x is the 2025/26 game and keeps receiving bug fixes. They are separate games: each needs a new game, and saves do not load across the two lines. The update notice only tells you about newer versions of your own line. See [which version do I need](index.md#which-version-do-i-need-two-lines).

## The game opened a window about a new version: is that safe?
Yes. Since 25.0.2 a small helper (`CM0304-UpdateCheck.exe`) starts with the game and, at most once a day, asks this project's GitHub releases page whether a newer version of **your own version line** exists (25.x players are told about 25.x versions only). If so, it shows a window and offers to open the download page. It sends nothing about you or your game, and it never downloads or installs anything by itself. Details: [the update notice](update-notice.md).

## How do I turn off the update notice?
Untick "Check for updates when the game starts" in the installer, or install silently with `/noupdatecheck`. Later you can create an empty file named `update-check.disabled` in the game folder, or set the environment variable `CM0304_NO_UPDATE_CHECK=1`. Full list: [the update notice](update-notice.md).

## Friendly matches only allowed 5 substitutions
That was a mistake in 25.0.0 and is fixed in 25.0.1: friendlies allow 12 substitutions again. League and cup matches keep 12 named players and 5 substitutions used. The fix is in the exe, so it also applies to existing games.

## The 2D match is too fast or too slow
Since 25.0.1 the speed option really controls the pace of the 2D view. Approximate figures:

| Speed setting | Pace of the 2D view |
|---|---|
| Very slow | as before |
| Slow | as before |
| Medium | as before (the reference) |
| Fast | about 3x Medium |
| Very Fast | about 4.5x Medium |

The other match views use the same setting; their pace can differ from 25.0.0.

## Mods that change the exe, and other mods
Our modified `cm0304.exe` replaces yours, so other exe mods and cracks are **not** kept while this update is installed. Database mods are replaced too. Everything is backed up, and the uninstaller restores your files from before the update.

## Can I keep my old saves?
Not in 26.0.0: it is the 2026/27 game, so saves made with 25.x or earlier versions, and saves from the original game, do not load in it. Start a new game. Your old saves stay in the folder (`user data\games`); keep them if you plan to go back to 25.x. Inside the 25.x line, saves of 25.1.0 load in 25.1.1 and 25.1.2.

## Is it safe? Can I go back?
The installer backs up the files it replaces or removes (your exe included) to `backup_pre_v25` in your game folder, verifies the result, and rolls back automatically if something fails. `Uninstall CM 03-04 26.0.0.exe` (or the setup with `/uninstall`) restores your originals, then removes the backup folder and itself. Reinstalling afterwards works. Saves and other files are not touched. To go from 26.0.0 to 25.x, run the 26.0.0 uninstaller first and then the 25.x installer from the [Releases page](https://github.com/cm0304-modern/cm0304-modern/releases) (see "How do I go back to 25.x?"). Inside the 25.x line, to go from 25.1.1 back to 25.1.0, run the 25.1.0 installer on the same game folder: it puts the 25.1.0 exe and helper back and leaves the data as it is.

## Why does Windows warn me about the installer?
The installer is not code-signed, so SmartScreen may show an "unknown publisher" warning. You can compare the file's SHA-256 with the one on the release page.

## Where is my game folder?
The folder that contains `cm0304.exe`. A common location is `C:\Program Files (x86)\Eidos\CM 03-04`. The installer checks common places and lets you browse.

## Which nations are playable?
In 26.0.0, 30 nations have real 2026/27 divisions and cups: the 28 nations of the 25.x line plus Russia and Israel. Serbia and Montenegro, Australia, Japan, Mexico, Colombia, Indonesia, South Korea, Hong Kong, South Africa, India, China PR and Singapore are not selectable. See [nations](nations.md). (In 25.x, 28 nations are playable and Russia and Israel are hidden too.)

## Why are some nations missing from the new-game screen?
They are hidden on purpose. Their clubs still exist in the world as foreign clubs with rosters from the older Football Manager 26 data, but their leagues have not been updated.

## Are the players accurate?
In 26.0.0 the players of the 30 nations come from Football Manager 27 data (the other nations from Football Manager 26 data), but we do not claim every player is accurate. Some clubs have no matching squad in the source data and use generated squads instead, and lower-division clubs without a page in the new database keep the facts of the older one. See [known issues](known-issues.md).

## Why do some clubs have no manager or an odd squad?
Some clubs have no counterpart in the source data. See [known issues](known-issues.md).

## Does it work on Linux, Mac or Steam Deck?
Only Windows 10 and 11 have been considered. The installer is a Windows program.

## How can I report a crash?
Follow [report a bug](report-a-bug.md). A small crash dump file helps a lot.


### What does the speed-up change in my game folder?
Three files: `msvcr71.dll` (replaced by the speed-up runtime; your own file is backed up first), `MSVCR71_real.dll` (your original runtime, kept under this name because the speed-up forwards to it) and `cm_proxy.cfg` (optional settings, explained inside). The uninstaller puts your own `msvcr71.dll` back byte for byte and removes the other two.

### How do I switch the speed-up off?
Open `cm_proxy.cfg` in the game folder and put the line `CM_PROXY_DISABLE=1` into it (remove the `#` in front of the example line), then restart the game: the caches are off and the game behaves as before. Or install with the `/noproxy` switch of a silent install, or run the uninstaller. By hand: delete `msvcr71.dll` and rename `MSVCR71_real.dll` to `msvcr71.dll`. Do not delete only `MSVCR71_real.dll`: the game then does not start and Windows reports that `MSVCR71_real.dll` was not found.

### My antivirus reports msvcr71.dll
The speed-up library is not code-signed. Add the game folder to your antivirus exclusions, or install with `/noproxy` (silent install), or switch the speed-up off as above.

### What if my msvcr71.dll is not the original?
If it is another valid 32-bit runtime exporting the same functions, the installer keeps your file as `MSVCR71_real.dll`. If it is not a usable runtime (or belongs to another tool), the installer leaves it alone, installs everything else without the speed-up and says so on the last page.
