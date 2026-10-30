# FAQ

## Do I need the original game?
Yes. This project does not include the game. You need your own CM 03/04 installation, version 4.1.5.

## I use a no-CD exe: will it work?
Yes. The installer works with any exe in a CM 03/04 4.1.5 folder, no-CD exes included. It replaces your `cm0304.exe` with our modified executable (which needs no CD) and backs up yours byte for byte. The uninstaller puts your no-CD exe back. We cannot test the installer against every game variant; if something goes wrong, please [report it](report-a-bug.md).

## I have the official 4.1.5 exe (installed with the official 4.1.4 and 4.1.5 patches)
That works in 25.0.1. The 25.0.0 installer accepted only one specific 4.1.5 executable and refused the official one; this is fixed.

## How do I upgrade from 25.0.0 or 25.0.1?
Close the game and run the 25.0.2 installer on the same game folder (the same applies to a reinstall). The database is unchanged, so your 25.0.x saves keep working.

## The game opened a window about a new version: is that safe?
Yes. Since 25.0.2 a small helper (`CM0304-UpdateCheck.exe`) starts with the game and, at most once a day, asks this project's GitHub releases page whether a newer version exists. If so, it shows a window and offers to open the download page. It sends nothing about you or your game, and it never downloads or installs anything by itself. Details: [the update notice](update-notice.md).

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
Saves from 25.0.0 and 25.0.1 keep working with 25.0.2. Saves from the original game or other versions are not compatible: start a new game after a fresh install.

## Is it safe? Can I go back?
The installer backs up the files it replaces or removes (26 entries, your exe included) (your exe included) to `backup_pre_v25` in your game folder, verifies the result, and rolls back automatically if something fails. `Uninstall CM 03-04 25.0.3.exe` (or the setup with `/uninstall`) restores your originals, then removes the backup folder and itself. Reinstalling afterwards works. Saves and other files are not touched.

## Why does Windows warn me about the installer?
The installer is not code-signed, so SmartScreen may show an "unknown publisher" warning. You can compare the file's SHA-256 with the one on the release page.

## Where is my game folder?
The folder that contains `cm0304.exe`. A common location is `C:\Program Files (x86)\Eidos\CM 03-04`. The installer checks common places and lets you browse.

## Which nations are playable?
28 nations have real 2025/26 divisions and cups. Serbia and Montenegro, Australia, Japan, Russia, Mexico, Colombia, Indonesia, South Korea, Hong Kong, South Africa, India, China PR and Israel are not selectable. See [nations](nations.md).

## Why are some nations missing from the new-game screen?
They are hidden on purpose. Their clubs still exist in the world as foreign clubs with current squads, but their leagues have not been updated.

## Are the players accurate?
The players come from Football Manager 26 data, but we do not claim every player is accurate. Some clubs have no matching squad in the source data and use generated squads instead. See [known issues](known-issues.md).

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
