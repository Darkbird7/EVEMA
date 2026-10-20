# Copying settings

Everything on this page starts with a right-click on a row in the **Local Files** tab. Whatever you pick, EVEMA shows what will change before writing anything, and backs up the file it's about to change.

**Close every EVE client first.** The client saves its own settings when it logs out, which would undo your copy. If a client is open, EVEMA holds the copy back and writes it once the client closes; see [Changes while EVE is running](backups-and-eve-running.md#changes-while-eve-is-running).

## Which copy do I want?

| You want to… | Use |
| --- | --- |
| Make one character's or account's settings an exact copy of another's | [Copy all to](#copy-a-whole-file) |
| Do that for a whole group of characters at once | [Copy all to N selected files](#copy-to-many-at-once) |
| Copy only the window layout, or only the overview presets, and leave everything else alone | [Copy sections to](#copy-only-some-sections) |
| Keep a copy of your setup, move it to another computer, or share it with a friend | [Export and Import](#export-and-import-a-settings-file) |
| Share your overview in the game's own format, for anyone to import in the client | [In game (.yaml)](#export-your-overview-for-the-game) |

Copies only go between files of the same type: character to character, or account to account.

## Copy a whole file

1. Right-click the file you want to copy **from**.
2. Choose **Copy all to**, then the file to copy **to**.
3. Check the confirmation, which shows what will change, then click **Overwrite**.

The destination becomes an exact copy of the source: windows, overview, keybinds, chat, audio, graphics, everything that file holds.

## Copy to many at once

1. Click the source, then **Ctrl+click** (**Cmd+click** on macOS) each target, or **Shift+click** for a range. Targets must be the same type as the source.
2. Right-click the source.
3. Choose **Copy all to** → **Copy all to N selected files…**, check the summary, and confirm.

Each target gets its own backup.

## Copy only some sections

Section copy changes only the parts you tick and leaves the rest of the destination file alone.

1. Right-click the source and choose **Copy sections to**, then the destination.
2. The **Copy sections** window lists every change, grouped by section. Expand a section to see each change, and untick any you don't want (**Select all** / **Select none** help).
3. Click **Copy**.

What you can copy:

- **Between characters:** the **Window layout**. If both characters are [paired with an account](getting-started.md#3-pair-each-character-with-its-account), their accounts' overview sections are offered too.
- **Between accounts:** **Overview tabs' bracket presets** (which preset each tab uses), **Bracket presets**, **Overview flags** and **Ship label**.

Overview tabs and bracket presets are matched **by name**, not by position. Nothing is created on the destination: a tab that doesn't exist there is reported as not matched rather than added.

Keybinds, chat, audio and graphics can't be copied section by section yet. Use a whole-file copy for those.

## Export and import a settings file

Export saves settings to a JSON file that you can keep as a snapshot, move to another computer, or share.

- **Right-click → Export → Export all…** saves everything EVEMA can copy by section. For a character, that's its window layout plus its paired account's overview settings.
- **Right-click → Export → Export sections…** lets you pick sections and individual changes first.

To apply one, right-click the file to change and choose **Import…**. You get the same preview, per-change ticking and backup as a section copy. Importing onto a character applies the window layout to the character and the overview settings to its paired account.

## Export your overview for the game

**Right-click → Export → In game (.yaml)…** saves the account's overview (for a character, its paired account's) as the same `.yaml` file EVE's own Overview Settings → Export creates. Import it in the client from **Overview Settings**. It's the format players already use to share overview packs.

The **Ship Labels** tab has the same export under **Export ▾**, plus **Step by step (.txt)…**, which writes instructions for re-entering the label by hand in EVE's Ship Label editor.

A few overview colours EVEMA can't match to the game's palette are left out; the status bar says which, and the game uses its default colour for them.

## If a copy went wrong

Every copy backed up the destination first. Right-click the file, choose **Restore backup**, and pick the time from before the copy. See [Backups](backups-and-eve-running.md#undo-a-change-restore-a-backup).
