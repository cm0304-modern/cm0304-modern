# FAQ

## Do I need the original game?
Yes. This project does not include the game. You need your own CM 03/04 installation, version 4.1.5.

## I use a no-CD exe: will it work?
Yes. The installer works with any exe in a CM 03/04 4.1.5 folder, no-CD exes included. It replaces your `cm0304.exe` with our modified executable (which needs no CD) and backs up yours byte for byte. The uninstaller puts your no-CD exe back. We cannot test the installer against every game variant; if something goes wrong, please [report it](report-a-bug.md).

## I have the official 4.1.5 exe (installed with the official 4.1.4 and 4.1.5 patches)
That works in 25.0.1. The 25.0.0 installer accepted only one specific 4.1.5 executable and refused the official one; this is fixed.

## How do I upgrade from 25.0.0?
Close the game and run the 25.0.1 installer on the same game folder (the same applies to a reinstall). The database is unchanged from 25.0.0, so your 25.0.0 saves keep working.

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
Saves from 25.0.0 keep working with 25.0.1. Saves from the original game or other versions are not compatible: start a new game after a fresh install.

## Is it safe? Can I go back?
The installer backs up the 25 files it touches (your exe included) to `backup_pre_v25` in your game folder, verifies the result, and rolls back automatically if something fails. `Uninstall CM 03-04 25.0.1.exe` (or the setup with `/uninstall`) restores your originals, then removes the backup folder and itself. Reinstalling afterwards works. Saves and other files are not touched.

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
