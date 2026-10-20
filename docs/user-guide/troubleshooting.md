# Troubleshooting

## My change didn't show up in game

Almost always, an EVE client was running. The client saves its own settings when it logs out, over the top of yours.

- If EVEMA saw the client, your change waited in the banner and was written after the client closed. Check the **Activity** panel (bottom left) to see whether it was written.
- If EVEMA didn't see the client (possible on macOS and in Wine setups other than Steam/Proton), the change was written straight away, then overwritten. Close every client and make the change again.
- A character's window layout is read when that character logs in. Log out to character selection and back in, or restart the client.

See [Changes while EVE is running](backups-and-eve-running.md#changes-while-eve-is-running).

## The Overview, Brackets or Ship Labels tab is empty for a character

Those settings live in the account file, so the character needs a [paired account](getting-started.md#3-pair-each-character-with-its-account). Click **⇄** next to the character's name and pick its account.

## EVEMA found no settings files, or the wrong ones

Go to **Settings → EVE locations**. If EVEMA found more than one install, pick the right one with **Use this**. Otherwise click **Browse…** next to **Settings folder** and choose EVE's settings folder (the one holding a folder for each EVE install). **Auto-Detect** goes back to the automatic choice. The change applies the next time EVEMA starts.

The usual locations are:

- **Windows:** `%LOCALAPPDATA%\CCP\EVE\`
- **macOS:** `~/Library/Application Support/CCP/EVE/`
- **Linux, Steam/Proton or Wine:** the Windows path, inside the Wine prefix (under `drive_c/users/<name>/`)

## A character shows a number instead of a name

Names come from EVE's public API, which only knows Tranquility characters. Characters on Singularity or Thunderdome are shown by ID. Right-click and **Rename Character…** to give it a name in EVEMA.

## I want to undo a change

Right-click the file in **Local Files**, choose **Restore backup**, and pick a time from before the change. See [Backups](backups-and-eve-running.md#undo-a-change-restore-a-backup).

## macOS says EVEMA "can't be opened"

The app isn't notarized yet. Right-click `EVEMA.app`, choose **Open**, then confirm. Or allow it under **System Settings → Privacy & Security → Open Anyway**. You only need to do this once.

## Windows SmartScreen warns about EVEMA

The app isn't code-signed yet. Choose **More info → Run anyway**. You can check your download against the release's `SHA256SUMS` file first.

## A Linux AppImage tool won't start

Mark it executable (`chmod +x Tool.AppImage`, or tick "Allow executing as program" in your file manager), then click **Launch** again.

## Where EVEMA keeps its own data

EVEMA's preferences, backups, cache and logs live in their own `EVEMA` folder, never inside EVE's. On Windows that's `%LOCALAPPDATA%\EVEMA`, and on Linux `~/.local/share/EVEMA`.

**Settings → Open Logs Folder** opens its `logs` folder on any system; the rest of EVEMA's data is in the folder above it. A new log is started each day and logs older than 14 days are deleted.

**Settings → Reset EVEMA…** erases EVEMA's preferences and takes you back to first-time setup. Your EVE settings files and backups are not touched.

## Reporting a bug

[Open an issue](https://github.com/Darkbird7/EVEMA/issues/new/choose) using the bug report form. Two things help a lot:

- **Activity → Copy** copies every message EVEMA showed this session.
- The lines from today's `evema-*.log` around the time of the problem (**Settings → Open Logs Folder**).

Logs can contain character names, IDs and folder paths; remove anything you'd rather not post. **Please don't attach your `core_char_*.dat` or `core_user_*.dat` files** to a public issue.
