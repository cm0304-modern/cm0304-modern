# CM 03/04 Modern

A fan-made, unofficial update that brings Championship Manager 03/04 (version 4.1.5) into the 2025/26 football world.

**Current version: 25.0.0** - [Download from Releases](https://github.com/cm0304-modern/cm0304-modern/releases/latest)

Pages: [FAQ](faq.md) | [Nations](nations.md) | [Known issues](known-issues.md) | [Changelog](changelog.md) | [Report a bug](report-a-bug.md) | [Screenshots](screenshots.md)

## Install guide

**Before you start**

- You need your own **stock, unmodified** Championship Manager 03/04, version 4.1.5, on Windows 10 or 11.
- Close the game and the editor.
- Have about 700 MB of free disk space.

**Steps**

1. Download `CM0304-Modern-25.0.0-Setup.exe` from the release page. You can check the download with PowerShell: `Get-FileHash .\CM0304-Modern-25.0.0-Setup.exe` and compare with the SHA-256 shown on the release.
2. Run the installer and accept the administrator prompt. If Windows SmartScreen says "unknown publisher", that is because the installer is not code-signed.
3. Choose the folder that contains `cm0304.exe`. Setup lists what it will change, backs up the originals to `backup_pre_v25`, installs and verifies every file.
4. Start the game and begin a **new game**. Old saves do not work with this version.

If the installer says your game is modified, already upgraded, or an unknown version, it has not changed anything. The message lists the files that differ.

**Uninstall:** run `Uninstall CM 03-04 25.0.0.exe` from your game folder. It restores the originals from the backup.

## What's new in 25.0.0

- A real 2025/26 world built from Football Manager 26 data: about 148,000 players and about 47,000 staff, with current club names, stadiums and finances.
- 28 nations with real 2025/26 divisions and cups (see [nations](nations.md)).
- Modern squad rules: 12 named players and 5 substitutes used.
- 2025/26 foreign-player limits per nation, updated EU flags, national-team managers.
- African Cup of Nations and year-related fixes.
- A "Buy Me a Coffee" button in the sidebar and a Contributors screen.

The full list is in the [changelog](changelog.md). Please also read the [known issues](known-issues.md).

## Support

Bugs and requests: [GitHub Issues](https://github.com/cm0304-modern/cm0304-modern/issues/new/choose). Tips on what to include: [report a bug](report-a-bug.md).

If you like the project: <https://buymeacoffee.com/cm0304modern>

*Fan-made and unofficial. Not affiliated with or endorsed by the original developers or publishers. No game files are included other than our installer patch and data.*
