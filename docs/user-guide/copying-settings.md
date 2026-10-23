# Copying settings

Everything on this page starts with a right-click on a row in the **Local Files** tab. Whatever you pick, EVEMA shows what will change before writing anything, and backs up the file it's about to change.

**Close every EVE client first.** The client saves its own settings when it logs out, which would undo your copy. If a client is open, EVEMA holds the copy back and writes it once the client closes; see [Changes while EVE is running](backups-and-eve-running.md#changes-while-eve-is-running).

## Which copy do I want?

| You want to… | Use |
| --- | --- |
| Make one character's or account's settings an exact copy of another's | [Copy all to](#copy-a-whole-file) |
| Do that for a whole group of characters at once | [Copy all to N selected files](#copy-to-many-at-once) |
| Copy only the window layout, the overview presets, the audio, camera or chat settings, and leave everything else alone | [Copy sections to](#copy-only-some-sections) |
| Do that for a whole group of characters or accounts at once | [Copy sections to N selected files](#copy-sections-to-many-at-once) |
| Keep a copy of your setup, move it to another computer, or share it with a friend | [Export and Import](#export-and-import-a-settings-file) |
| Share your overview in the game's own format, for anyone to import in the client | [In game (.yaml)](#export-your-overview-for-the-game) |
| Move everything to a new computer | [Export everything](#move-your-whole-setup-to-another-computer) |

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

### More settings you can copy

Under those sections, the window lists more groups of settings. Each is ticked to begin with only if it's on by default below and would change something:

| Group | File | On by default | What it copies |
| --- | --- | --- | --- |
| **Overview (everything)** | account | no | The whole overview, columns and colours included. Ticking it unticks the four overview sections above, and the other way round. |
| **Probe formations** | account | yes | Your saved probe formations and scanner filters. The client's own temporary formation on the destination is kept. |
| **Suppressed dialogs** | account | yes | Your "don't show this again" choices. |
| **Audio** | account | yes | Sound settings. |
| **Camera and graphics** | account | yes | Camera, space mouse and graphics effects. |
| **Market and contracts** | account | yes | Market and contract search filters. |
| **Module slots and linked weapons** | account | no | Slot order and weapon groups. Usually set up per character, so it's off. |
| **Window tab groups** | account | yes | Which tabs are grouped and selected in windows. |
| **Windows (raw)** | character | no | The whole windows section. **Window layout** is the usual way to copy layouts. |
| **Neocom** | character | yes | Your Neocom buttons. |
| **Chat channels** | character | yes | The channels the character has joined. |
| **Info panels** | character | yes | Which info panels are shown where. |
| **Docked panels** | character | yes | Docked panels such as the skill planner and the map. |
| **Search history** | both | no | Recent searches. |

A group makes the destination's settings in it **the same as the source's**. So a setting the source doesn't have is removed, and the change list shows it as **Removed**. Untick it to keep it. Private and player chat channel settings, and cached values such as market prices, are never copied.

Keybinds can't be copied section by section yet. Use a whole-file copy for those.

## Copy sections to many at once

1. Click the source, then **Ctrl+click** (**Cmd+click** on macOS) each target, or **Shift+click** for a range. Targets must be the same type as the source.
2. Right-click the source and choose **Copy sections to** → **Copy sections to N selected files…**.
3. Tick sections and groups once; they apply to every target. Each change in a list is labelled with its file, so you can untick a change on one file and keep it on the others.
4. Click **Copy**.

Each file gets its own backup and its own write. If one fails, the others still go ahead, and the status bar names the ones that failed. For characters, their paired accounts are included, each once, however many of the characters share it.

## Export and import a settings file

Export saves settings to a JSON file that you can keep as a snapshot, move to another computer, or share.

- **Right-click → Export → Export all…** saves everything EVEMA can copy by section. For a character, that's its window layout plus its paired account's overview settings.
- **Right-click → Export → Export sections…** lets you pick sections and individual changes first.

To apply one, right-click the file to change and choose **Import…**. You get the same preview, per-change ticking and backup as a section copy. Importing onto a character applies the window layout to the character and the overview settings to its paired account.

## Export your overview for the game

**Right-click → Export → In game (.yaml)…** saves the account's overview (for a character, its paired account's) as the same `.yaml` file EVE's own Overview Settings → Export creates. Import it in the client from **Overview Settings**. It's the format players already use to share overview packs.

The **Ship Labels** tab has the same export under **Export ▾**, plus **Step by step (.txt)…**, which writes instructions for re-entering the label by hand in EVE's Ship Label editor.

A few overview colours EVEMA can't match to the game's palette are left out; the status bar says which, and the game uses its default colour for them.

## Move your whole setup to another computer

**Backups ▾ → Export everything…** (above the Local Files list) saves your whole setup in one `.zip`:

- every character and account settings file, and `prefs.ini`, of every EVE install and profile on this computer
- EVEMA's account names, character names, pairings and state names
- EVEMA's backups too, if you tick **Include EVEMA's backups**

On the other computer, run each EVE client you use once, so its settings folder exists. Then choose **Backups ▾ → Import everything…** and pick the archive. EVEMA checks every file against the checksum saved with it, and refuses the whole archive if anything was damaged or changed.

The import window lists every settings file and how it compares with what's already there:

- **New** files are ticked, ready to import.
- **Different here: replace?** files are not ticked. Tick the ones you want replaced; each is backed up first.
- **Already the same** files are left alone.
- **No install of this server** files can't be imported until you've run that client on this computer.

Files go to the same server and profile they came from, even though EVE's install folder has a different name on each computer. If a computer has two installs of one server, the most recently used one gets the files.

Names and pairings are added where this computer has none. Where both computers have a different name for the same character or account, you choose once whether to keep this computer's or take the archive's.

Settings files hold your character and account IDs, chat channel IDs and other details about how you play. Only give an archive to someone you'd show your settings to.

## If a copy went wrong

Every copy backed up the destination first. Right-click the file, choose **Restore backup**, and pick the time from before the copy. See [Backups](backups-and-eve-running.md#undo-a-change-restore-a-backup).
