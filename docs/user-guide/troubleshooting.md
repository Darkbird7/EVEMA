# Troubleshooting

## My change didn't show up in game

Almost always, an EVE client was running. The client saves its own settings when it logs out, over the top of yours.

- If EVEMA saw the client, your change waited in the banner and was written after the client closed. Check the **Activity** panel (bottom left) to see whether it was written.
- If EVEMA didn't see the client (possible on macOS and in Wine setups other than Steam/Proton), the change was written straight away, then overwritten. Close every client and make the change again.
- A character's window layout is read when that character logs in. Log out to character selection and back in, or restart the client.

See [Changes while EVE is running](backups-and-eve-running.md#changes-while-eve-is-running).

## The Overview, Ship Labels or Probe Formations tab is empty for a character

Those settings live in the account file, so the character needs a [paired account](getting-started.md#3-pair-each-character-with-its-account). Click the **Not paired · Pair…** chip next to the character's name and pick its account.

## EVEMA found no settings files, or the wrong ones

Go to **Settings → EVE locations**. If EVEMA found more than one install, pick the right one with **Use this**. Otherwise click **Change…** next to **Settings folder**, then **Browse…**, and choose EVE's settings folder (the one holding a folder for each EVE install). **Use detected** goes back to the automatic choice. The change applies the next time EVEMA starts.

The usual locations are:

- **Windows:** `%LOCALAPPDATA%\CCP\EVE\`
- **macOS:** `~/Library/Application Support/CCP/EVE/`
- **Linux, Steam/Proton or Wine:** the Windows path, inside the Wine prefix (under `drive_c/users/<name>/`)

## A character shows a number instead of a name

Names come from EVE's public API, which only knows Tranquility characters. Singularity characters are looked up there too and marked **(via Tranquility)**; if one shows the wrong name, it was probably made on Singularity after the last copy from Tranquility. Thunderdome characters are shown by ID. Either way, select it and choose **⋯** → **Rename Character…** (or right-click it) to give it a name in EVEMA; your name always wins.

## I want to undo a change

Straight after the change, click **Undo** at the right of the status bar. For an older change, select the file in **Characters**, choose **⋯** → **Restore backup** (or right-click the file), and pick a time from before the change. See [Backups](backups-and-eve-running.md#undo-a-change-restore-a-backup).

## macOS says EVEMA "can't be opened"

The app isn't notarized yet. Right-click `EVEMA.app`, choose **Open**, then confirm. Or allow it under **System Settings → Privacy & Security → Open Anyway**. You only need to do this once.

## Windows SmartScreen warns about EVEMA

The app isn't code-signed yet. Choose **More info → Run anyway**. You can check your download against the release's `SHA256SUMS` file first.

## A Linux AppImage tool won't start

**Launch** marks an AppImage executable before starting it, but it can only do that for a file you own. If the message says to mark it executable, do it yourself (`chmod +x Tool.AppImage`, or tick "Allow executing as program" in your file manager), then click **Launch** again.

## Updating EVEMA

When a newer EVEMA is out, a banner above the tabs says so (turn the check off in **Settings → General**).

- **Install and restart** (Windows and Linux) downloads the new version, checks it against the SHA-256 checksum GitHub publishes for it, puts it in place of the running one, and restarts EVEMA. If the download doesn't match, or GitHub published no checksum, nothing is installed and the banner says why. EVEMA's old files are removed the next time it starts.
- While changes are waiting for EVE to close, EVEMA won't restart for an update: write or discard them in **Characters** first.
- **View release** opens the release page, to download the new version yourself. On macOS that's the only option: macOS runs an app it hasn't seen notarized from a read-only copy, so EVEMA can't replace itself there. The same goes for the Linux AppImage, which runs from a read-only image (download the new AppImage instead), and for any folder EVEMA can't write to.

## Where EVEMA keeps its own data

EVEMA's preferences, backups, cache and logs live in their own `EVEMA` folder, never inside EVE's. On Windows that's `%LOCALAPPDATA%\EVEMA`, and on Linux `~/.local/share/EVEMA`.

**Settings → Advanced → Open logs folder** opens its `logs` folder on any system; the rest of EVEMA's data is in the folder above it. A new log is started each day and logs older than 14 days are deleted.

**Settings → Advanced → Reset EVEMA…** erases EVEMA's preferences and takes you back to first-time setup. Your EVE settings files and backups are not touched.

## Reporting a bug

[Open an issue](https://github.com/Darkbird7/EVEMA/issues/new/choose) using the bug report form. Two things help a lot:

- **Activity → Copy** copies every message EVEMA showed this session.
- The lines from today's `evema-*.log` around the time of the problem (**Settings → Advanced → Open logs folder**).

Logs can contain character names, IDs and folder paths; remove anything you'd rather not post. **Please don't attach your `core_char_*.dat` or `core_user_*.dat` files** to a public issue.
