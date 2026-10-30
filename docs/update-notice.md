# The update notice

Since version 25.0.2 the game can tell you when a newer version of CM 03/04 Modern is available. This page explains exactly what it does, and how to turn it off.

## What it is

When the game starts, it also starts a small helper program, `CM0304-UpdateCheck.exe`, which sits in your game folder next to `cm0304.exe`. The helper compares the version you have with the latest version on this project's GitHub releases page. If a newer one exists, it shows a short window.

## Exactly what it does

- It runs **at most once a day**. Starting the game again the same day does nothing.
- It makes **one request** to the GitHub releases page of this project (`cm0304-modern/cm0304-modern`). That is all it talks to.
- It sends **nothing about you or your game**: no name, no save, no list of files, no settings. Like any web request, GitHub sees your internet address; the helper adds nothing else.
- It **never downloads, installs or changes anything** by itself. It only offers to open the download page in your browser, and only if you click Yes.
- If you are offline, or anything goes wrong, it stays silent and the game starts as usual.
- It keeps a small settings file (when it last checked, which version you asked not to be reminded about) in `%LOCALAPPDATA%\CM0304Modern`. The uninstaller removes it.

## What it looks like

A small window titled "CM 03/04 Modern update" appears over the game a few seconds after it starts. It says that a newer version is available and asks whether to open the download page. You can answer Yes (opens the page in your browser), No (ask again another day), or "Don't remind me about this version". The game keeps running while the window is open.

## Turning it off

Any one of these is enough:

1. **In the installer:** untick "Check for updates when the game starts".
2. **Silent install:** add `/noupdatecheck`, for example `CM0304-Modern-25.0.2-Setup.exe /S /noupdatecheck /D=...`.
3. **Later, with a file:** create an empty file named `update-check.disabled` in the game folder (next to `cm0304.exe`). Delete the file to turn the notice back on.
4. **With an environment variable:** set `CM0304_NO_UPDATE_CHECK=1` in Windows.

You can also simply delete `CM0304-UpdateCheck.exe`. The game works without it.

## Antivirus and SmartScreen

The helper is not code-signed, so antivirus software or Windows SmartScreen may warn about it. That is expected for a small unsigned program. If you prefer, switch it off as above or delete it.

## Only with the 25.x game program

The notice only works with the version 25.x `cm0304.exe` that this installer puts in your game folder. The original game program, the official 4.1.5 exe and no-CD exes do not start the helper, so they never show the notice. (After you uninstall, your own exe comes back and the helper is removed.)

Back to the [FAQ](faq.md) or the [start page](index.md).
