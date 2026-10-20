# What EVEMA does, and what it won't do

EVEMA is a desktop settings manager for EVE Online. It works on the settings files the EVE client saves on your own computer, and it helps you keep the community tools you use installed and up to date. It runs on Windows, macOS and Linux.

EVEMA is a fan project. It is not made, endorsed or supported by Fenris Creations (FC, formerly CCP Games).

## What it does

### Your settings files (Local Files tab)

- **Finds your settings.** It looks in the usual place on each system, including Steam/Proton and Wine prefixes on Linux. You can also point it at another folder. Characters are shown by name, and accounts by a name you choose.
- **Shows what's in them.** For each character and account, it shows:
  - window positions on a scaled canvas
  - overview tabs and bracket presets
  - overview options and the ship label
  - the character's public profile
- **Copies settings between characters and accounts:**
  - the whole file, to one character or to many at once
  - or only the sections you pick: window layout, overview tab presets, bracket presets, overview options, ship label
  - before anything is written, it shows you what will change
- **Exports and imports** a character's or account's settings as a JSON file you can keep or share, and exports an account's overview as the `.yaml` file the game's own Overview Settings can import.
- **Edits settings directly:** bracket presets (create, duplicate, rename, delete, edit groups and states), which preset each overview tab uses, the ship label, overview options, window positions, and the "always show ship brackets" preference.
- **Backs up before every change.** It makes a timestamped backup before it writes to any file, and you can restore any backup from the app. Files are written in a way that can't leave a half-written file behind, even if something crashes mid-save.
- **Waits for EVE to close.** The client saves its own settings when it logs out or closes, which would overwrite a change made while it was open (and a change only shows up at the next login anyway). So while any client is running, EVEMA holds each change back, shows it in a banner, and writes it once every client has closed, on top of whatever the client saved on its way out. **Write now** and **Discard** are in the banner, and EVEMA asks before quitting with changes still waiting.

### Partnership tab

- Reads the combat log files the client writes (the `Gamelogs` folder) to list the pilots in them, to help run in-game giveaways. It only reads the logs; it never changes them.

### Tools tab

- Keeps a list of community tools: a few built in (EVE-O Preview, Pyfa, EveLens, Priceall), plus any program you add yourself.
- Finds where each one is installed, shows its version, and launches it when you click **Launch**. The tool runs as its own program, the same as if you had double-clicked it.
- **Get latest** downloads a tool's newest release from its GitHub page, but only when you click, and only after showing you exactly what it will download. It checks the file's SHA-256 checksum against the one GitHub publishes and refuses the download if the two don't match or no checksum exists.
- **Check for updates** compares the tools you have installed with their latest releases, only when you click.
- **Uninstall** removes only what EVEMA itself downloaded. It never deletes a folder you pointed it at.
- Each built-in tool carries a plain-language note on what it does to the game (for example, whether it only reads files, arranges windows, or hooks into the client), so you can judge it yourself. EVEMA lists these tools; it doesn't vouch for them.

## What it connects to

- **ESI** (Fenris Creations' official public API, `esi.evetech.net`) and Fenris Creations' image server, for character names, public profiles, portraits and logos, and item group names. No login and no account access: only public information. Responses are cached and reused for as long as Fenris Creations allows.
- **GitHub**, to check for a newer EVEMA release at startup (you can turn this off in Settings), and for the Tools tab's Get latest and Check for updates buttons when you click them.

Nothing else. EVEMA has no telemetry or analytics, and it never uploads your settings, logs or anything else.

## What it won't do

These are firm lines, not "not yet":

- **No changes to the game client.** No patching, no injected code, no loaded DLLs.
- **No reading the game's memory.**
- **No reading or altering network traffic** between the client and Fenris Creations' servers.
- **No automation or input.** No macros, no keystroke or mouse broadcasting, and nothing that plays the game for you.
- **No logging in as you.** EVEMA never asks for your EVE account or SSO login.
- **Nothing third-party runs inside EVEMA.** Managed tools run as their own programs, and only when you click Launch. EVEMA never starts something it downloaded by itself, never asks for administrator rights, and never installs certificates.
- **No writes without a backup.**

Requests that would cross these lines will be closed, however useful they would be.

## Good to know

- **Waiting changes need EVEMA open.** A change held back while EVE runs is written when EVE closes, so leave EVEMA running until then (it asks before you quit). With several clients open, it waits for all of them.
- **Not every setting can be copied section by section yet.** Keybinds, chat, audio and graphics are copied only as part of a whole-file copy.
- **Test servers:** ESI only knows Tranquility characters, so characters from Singularity or Thunderdome are shown by ID, not name.
- **macOS:** the app isn't notarized, so the first launch needs right-click → **Open**. On macOS, and in Wine setups other than Steam/Proton, EVEMA may not detect a running client, in which case changes are written straight away, as if EVE were closed.
- **Where EVEMA keeps its own data:** its preferences, backups, cache and logs live in its own folder, never inside EVE's. **Settings → Open Logs Folder** takes you there.

## Found a problem?

[Open an issue](https://github.com/Darkbird7/EVEMA/issues/new/choose). If a change went wrong, you can restore the previous version from the file's backups in the Local Files tab.
