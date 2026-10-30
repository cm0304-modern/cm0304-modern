# Known issues

This is what we know is not right in 25.0.2. If you find something else, please [report it](report-a-bug.md).

## Nations

- **14 nations are not selectable:** Serbia and Montenegro, Australia, Japan, Russia, Mexico, Colombia, Indonesia, South Korea, Hong Kong, South Africa, India, China PR, Singapore and Israel. Their clubs exist as foreign clubs with current rosters, but their leagues were not updated.
- Some Welsh and Northern Irish clubs have no counterpart in the source data.

## Clubs and squads

- **Generated squads.** Some clubs have no matching squad in the source data. Those clubs get a generated squad (made-up players) so they can play. Examples we know of are a few clubs in Austria, Finland and Belgium; there may be more.
- **Missing managers.** Some clubs have no manager. Known examples include a few clubs in Belgium, Greece, Finland and Ukraine.
- **Missing clubs.** A few real clubs could not be placed in a league and are left out of their country's league structure (for example three Polish clubs).
- **Reserve and B teams** cannot be represented by the game's competition structure.
- **Youth teams are empty.**
- **Club and competition histories are still from 2003.** Trophy rooms and "previous winners" lists do not show real recent history.
- **Player accuracy.** Players come from Football Manager 26 data. We do not claim that every player's details are correct, and squad numbers are not set.

## Game engine limits

- Some divisions keep their original size because the old game cannot handle another size without breaking its cups. Belgium, for example, keeps 18 clubs in each of its top two divisions.
- Lower divisions in several nations cannot be inspected while the game runs, so their fixture dates were not checked as closely as the top divisions.
- Second and later rollovers (more than two simulated seasons) have been tested for fewer nations than the first rollover.

## Install and compatibility

- Only CM 03/04 updated to version 4.1.5 is supported. The installer replaces `cm0304.exe`, so exe-level mods and cracks you use are replaced (your own exe is backed up and restored by the uninstaller).
- The installer cannot be tested against every game variant or language version. An unusual exe length or database header only gives a warning during install.
- The commentary match view follows the same speed setting as the 2D view, so a fast setting also speeds up the commentary.
- The installer is not code-signed, so Windows SmartScreen shows an "unknown publisher" warning.
- **Update helper.** The game exe starts a small helper, `CM0304-UpdateCheck.exe`, when the game starts (an unsigned program, so antivirus or SmartScreen may warn about it). It only checks for a newer version, see [the update notice](update-notice.md). You can switch it off, or simply delete it: the game works without it.
- Saves from the original game or other versions do not work (25.0.x saves do). Start a new game.
- Only Windows 10 and 11 are considered.
