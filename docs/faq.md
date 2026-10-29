# FAQ

## Do I need the original game?
Yes. This project does not include the game. You need your own, stock CM 03/04 installation, version 4.1.5.

## Will it work with a modded or already patched game?
No. The installer checks every file it replaces. If anything differs from stock 4.1.5 it refuses and lists the files, without changing anything. If you installed other mods, restore a clean installation first.

## Can I keep my old saves?
No. Start a new game after installing. Saves made with other versions are not compatible.

## Is it safe? Can I go back?
The installer backs up the 25 files it touches to `backup_pre_v25` in your game folder, verifies the result, and rolls back automatically if something fails. `Uninstall CM 03-04 25.0.0.exe` restores the originals. Saves and other files are not touched.

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

## Can I support the project?
Yes, if you like: <https://buymeacoffee.com/cm0304modern>. It is optional.
