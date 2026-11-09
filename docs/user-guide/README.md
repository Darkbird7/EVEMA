# EVEMA user guide

Step-by-step help for using EVEMA. If you haven't installed it yet, start with the [download instructions](../../README.md#download--install).

## Pages

1. **[Getting started](getting-started.md)**: first launch, finding your settings, naming accounts and pairing each character with its account.
2. **[Copying settings](copying-settings.md)**: copy the window layout, the overview, the interface or the whole file to one character or many, save groups and copies you repeat, and export or import settings as a file.
3. **[Editing settings](editing-settings.md)**: the overview summary, window positions, the ship label, probe formations and drone groups.
4. **[Backups, and changes while EVE is running](backups-and-eve-running.md)**: how EVEMA keeps your files safe, how to undo a change, and why it waits for EVE to close.
5. **[Tools](tools.md)**: keep EVE-O Preview, Pyfa and other community tools installed, launched and up to date.
6. **[Partnership](partnership.md)**: list the pilots from your combat logs and run a skin giveaway draw.
7. **[Troubleshooting](troubleshooting.md)**: common problems and where to find the logs.

For what EVEMA will and won't do, and everything it connects to, see [what EVEMA does](../what-evema-does.md).

## Two words used everywhere

EVE keeps your settings in two kinds of file, and EVEMA shows both in the **Characters** tab:

| Type in EVEMA | File | What's in it |
| --- | --- | --- |
| **Character** | `core_char_<character ID>.dat` | Window positions and sizes, and other per-character settings. |
| **Account** | `core_user_<account ID>.dat` | Overview tabs and columns, bracket presets, overview options, the ship label, probe formations, drone groups, and graphics, audio and camera settings. Shared by every character on that account. |

So moving your windows around changes a *character* file, and changing your overview changes an *account* file. EVE can't tell EVEMA which characters belong to which account, which is why [pairing](getting-started.md#3-pair-each-character-with-its-account) exists.
