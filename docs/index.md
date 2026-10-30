# CM 03/04 Modern

A fan-made, unofficial update that brings Championship Manager 03/04 (version 4.1.5) into the 2025/26 football world.

**Current version: 25.0.3** - [Download from Releases](https://github.com/cm0304-modern/cm0304-modern/releases/latest)

Pages: [FAQ](faq.md) | [Nations](nations.md) | [Known issues](known-issues.md) | [Update notice](update-notice.md) | [Changelog](changelog.md) | [Report a bug](report-a-bug.md) | [Screenshots](screenshots.md)

## Install guide

**Before you start**

- You need your own Championship Manager 03/04, **version 4.1.5** (updated with the official 4.1.5 patch, or a no-CD exe: any exe works), on Windows 10 or 11. The game folder must contain `cm0304.exe` and `data\db` with the four database files.
- Close the game and the editor.
- Have about 700 MB of free disk space.

**Steps**

1. Download `CM0304-Modern-25.0.3-Setup.exe` from the release page. You can check the download with PowerShell: `Get-FileHash .\CM0304-Modern-25.0.3-Setup.exe` and compare with the SHA-256 shown on the release.
2. Run the installer and accept the administrator prompt. If Windows SmartScreen says "unknown publisher", that is because the installer is not code-signed.
3. Choose the folder that contains `cm0304.exe`. Setup lists what it will change, backs up the originals to `backup_pre_v25`, installs and verifies every file.
4. Start the game and begin a **new game**. Saves from the original game or other versions do not work with this version.

**The installer replaces `cm0304.exe`** with our modified executable (it carries the rule changes). Your own exe is backed up byte for byte. No CD is needed afterwards.

**Upgrading from 25.0.0 or 25.0.1, or reinstalling:** just run the new installer on the same game folder. Your 25.0.x saves keep working (the database is unchanged).

If the installer refuses, it has not changed anything. It refuses only when the folder is clearly not a CM 03/04 folder, the game is running or files are not writable.

**Uninstall:** run `Uninstall CM 03-04 25.0.3.exe` from your game folder. It restores your original files (your own exe included) from the backup and then removes the backup folder and itself.

## What's new in 25.0.3

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
