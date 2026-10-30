# Changelog

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
