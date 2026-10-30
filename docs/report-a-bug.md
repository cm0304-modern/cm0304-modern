# Report a bug

Please open an issue here: <https://github.com/cm0304-modern/cm0304-modern/issues/new/choose>. Pick the form that fits (crash, data error, gameplay bug, request).

## What to include

- The version (shown at the lower left of the game; this release is 25.0.1).
- Which nations you ticked when you created the game.
- The in-game date when it happened.
- What happened and what you expected.
- Steps to repeat it, if you know them.
- For data errors: the club or player name, and what you think is correct.
- For crashes: a crash dump (see below). Screenshots of any error dialog also help.

## Crash dumps

When the game crashes, Windows can save a small "minidump" file that shows where it crashed. This is the most useful thing you can send. Windows Error Reporting (WER) does it if "LocalDumps" is switched on for `cm0304.exe`.

### Switch it on

1. Download `tools\enable-crash-dumps.reg` from this repository.
2. Right-click it, choose **Merge**, and accept the administrator prompt. Administrator rights are needed because it writes to `HKEY_LOCAL_MACHINE`.
3. Play until the crash happens again.
4. Open `%LOCALAPPDATA%\CM0304Modern\dumps` (paste it into the Explorer address bar). If the folder does not exist, create it and try to reproduce the crash again. You should find a file like `cm0304.exe.1234.dmp`.
5. Zip the `.dmp` file and attach the zip to your issue. If it is too large for GitHub, tell us in the issue and we will find another way.

The settings are: `DumpType` = 1 (minidump), `DumpFolder` = `%LOCALAPPDATA%\CM0304Modern\dumps`, `DumpCount` = 3 (Windows keeps the last three dumps).

### Switch it off

Use `tools\disable-crash-dumps.reg` in the same way. It removes the `cm0304.exe` entry again.

A minidump can contain parts of the game's memory, file paths and your Windows user name. Only share it if you are comfortable with that.

## Other useful files

- The installer log: `%TEMP%\CM0304-Modern-Setup.log` (for install problems).
- For install problems: the exact message the installer showed, and whether your game folder is CM 03/04 updated to 4.1.5 (official patch or no-CD exe, and where it came from).
- A screenshot of the error.
