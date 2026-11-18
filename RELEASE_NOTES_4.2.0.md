# CM 03/04 4.2.0 (original database)

A fan-made, unofficial update that keeps Championship Manager 03/04 (4.1.5) as the **original 2003/04 game** and adds quality-of-life fixes to the game executable. Not affiliated with or endorsed by the original developers or publishers. The installer contains a modified game executable, a few screen files and pictures, a small update helper and a speed-up runtime library, and no database files: your clubs, players and competitions stay the original ones. For the 2026/27 football world use the Modern line (26.x) on the Releases page.

4.2.0 is a **complete installer**: install it straight onto a CM 03/04 4.1.5 game. Saves of the original game load.

## What is in it

- Faster 2D match engine: 'Fast' and 'Very Fast' match speeds are quicker and the 2D view pace follows the speed setting.
- Player profile: a Positions pitch shows where a player can play, and it keeps its proportions at every window size.
- Player profile: attribute values are coloured by level (1-10 white, 11-15 yellow, 16-20 green).
- Simulate: a button in the 'Proceed to match?' window plays the match with your current squad and tactics without the match screen.
- Substitutes: 12 named, 5 used in every competition (friendlies: 12 named, 12 used).
- A speed-up runtime library (switch it off with `/noproxy` or in `cm_proxy.cfg`).
- A small update-check helper that tells you about newer releases of your own 4.x line (you choose in setup whether it is on).
- The save format (147) is unchanged: CM Scout and other save tools keep working.
- The foreign-player limits and the EU flags are not included (the original rules apply).

## Changelog

### Added

- **Simulate.** The 'Proceed to match?' window that opens when you click Go To Match has a new button, **Simulate**, to the left of No. It plays that one match with your current squad and tactics, without the match screen, and gives control back at midnight (0:00) after the match day. The **Last Match** page of the simulated match then opens by itself. Yes and No work as before.
- **Proportional Positions pitch.** The pitch picture on the Positions page of the player profile now keeps its proportions at every size of the profile window, with the position dots drawn on it.
- **Faster 2D match engine.** The 'Fast' and 'Very Fast' match speeds are quicker, and the 2D view pace follows the speed setting.
- **Attribute colours.** On the player profile the attribute values are coloured by level: 1-10 white, 11-15 yellow, 16-20 green (the names stay white).
- **Substitutes.** 12 players can be named and 5 used in every competition (friendlies: 12 named, 12 used).
- **Faster game.** A small runtime library next to the game makes the game faster (the installer can skip it with `/noproxy`).

### Changed

- The version label is now 4.2.0.

### How the installer treats your files

- The installer **replaces `cm0304.exe`** with our modified executable. No CD is needed afterwards.
- Your own exe (official 4.1.5, a no-CD exe, anything else) is backed up byte for byte and restored by the uninstaller. Other exe-level mods are not kept while the update is installed.
- The installer refuses, changing nothing, when the folder is clearly not a CM 03/04 folder, the game is running, files are not writable, or the folder has the **Modern line (26.x)** (or the withdrawn 4.1.6) installed. Uninstall that first (`Uninstall CM 03-04 <version>.exe` in the game folder, or `CM0304-Modern-Setup.exe /uninstall` when that file no longer exists). Modern installers older than 26.0.2 have **no** such guard and would overwrite a 4.x folder: use the installer of the line you have installed.

### Previous versions

4.2.0 is the first release of this line.

## Install

You need a CM 03/04 installation updated to 4.1.5 (the official 4.1.5 patch, or a no-CD exe: any exe works) on Windows 10 or 11. Close the game and the editor first.

1. Download the installer below.
2. Run it and accept the administrator prompt. Windows may warn about an unknown publisher (SmartScreen): the installer is not code-signed.
3. Choose the folder containing `cm0304.exe` and let setup finish.

**From the original game (4.1.5, or a no-CD exe):** run the installer on the game folder. Your own exe is backed up byte for byte.

**From CM 03-04 Modern 26.x:** uninstall it first (`Uninstall CM 03-04 <version>.exe` in the game folder); the installer refuses a folder that still has it (or the withdrawn 4.1.6), and changes nothing. If the uninstaller file no longer exists, run `CM0304-Modern-Setup.exe /uninstall`. Modern installers older than 26.0.2 have no such guard: use the installer of the line you have installed.

**Uninstall:** the originals are backed up to `backup_pre_v4` in your game folder. Run `Uninstall CM 03-04 4.2.0.exe` in the game folder, or the setup with `/uninstall`. It restores everything, then removes the backup folder and the uninstaller itself.

## Checksum

`CM0304-4.2.0-Setup.exe` (4,377,600 bytes)

SHA-256: `8D9AF0100C7F3C9373B593394CAAF918B8D440C82B720AE58E775D0C94CFF2BB`

Check it with PowerShell: `Get-FileHash .\CM0304-4.2.0-Setup.exe`

## Known issues

- The database is the original 2003/04 one: old players, clubs and rules, by design.
- The Modern line (26.x) saves and this line's saves are not interchangeable.

## Bugs

Report problems with the issue forms (choose version 4.2.0). For crashes please attach a minidump: <https://cm0304-modern.github.io/cm0304-modern/report-a-bug>
