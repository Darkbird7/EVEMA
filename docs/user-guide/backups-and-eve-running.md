# Backups, and changes while EVE is running

## Every change is backed up

Before EVEMA writes to any EVE settings file, it saves a timestamped copy of the file as it was. That covers copies, imports, edits, restores, all of it. Files are also written in a way that can't leave a half-written file behind if something crashes mid-save.

Backups are kept in EVEMA's own data folder, never inside EVE's (see [where EVEMA keeps its data](troubleshooting.md#where-evema-keeps-its-own-data)). By default EVEMA keeps the newest **5** backups of each file and deletes older ones. Change that in **Settings → Backups → Keep per file**.

## Undo a change: restore a backup

1. Close every EVE client.
2. In **Local Files**, right-click the file and choose **Restore backup**.
3. Pick the date and time from before the change, and confirm.

Restoring is itself a change, so the current version is backed up first. If you pick the wrong backup, you can restore the one you just replaced.

For a character's window layout, the **Window Layout** tab also has a **Restore backup…** button.

## Changes while EVE is running

The EVE client saves its own copy of your settings when you log out or close it. A change written while the client is open would be overwritten a moment later, and the client wouldn't show it until next login anyway.

So while any client is running, EVEMA **holds changes back** instead of writing them:

- A banner at the top of **Local Files** says a client is running and lists every change that's waiting.
- EVEMA's previews already show your waiting changes, so you can keep working (and make further changes on top).
- Once every client has been closed for a few seconds, EVEMA writes the waiting changes, on top of whatever the client saved on its way out. Each still gets its backup.

In the banner:

- **Write now** writes the waiting changes immediately. EVE may then overwrite them when it logs out, so EVEMA warns you first.
- **Discard** drops the waiting changes. Nothing was written, so nothing needs undoing.

**Leave EVEMA open until EVE closes.** Waiting changes only exist while EVEMA is running. If you try to quit with changes waiting, EVEMA asks first. With several clients open, it waits for all of them.

### When EVEMA can't see the client

EVEMA spots a running client by its process name. That's confirmed on Windows and on Linux with Steam/Proton. On macOS, and in Wine setups other than Steam/Proton, EVEMA may not see the client; then changes are written straight away, as if EVE were closed. In that case, close every client yourself before making changes.
