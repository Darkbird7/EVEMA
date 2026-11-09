# What EVEMA does, and what it won't do

EVEMA is a desktop settings manager for EVE Online. It works on the settings files the EVE client saves on your own computer, and it helps you keep the community tools you use installed and up to date. It runs on Windows, macOS and Linux.

EVEMA is a fan project. It is not made, endorsed or supported by Fenris Creations (FC, formerly CCP Games).

## What it does

### Your settings files (Characters tab)

- **Finds your settings.** It looks in the usual place on each system, including Steam/Proton and Wine prefixes on Linux. You can also point it at another folder. Characters are shown by name, and accounts by a name you choose. Once you pair each character with its account, the list shows which go together.
- **Shows what's in them.** For each character and account, it shows:
  - window positions on a scaled canvas
  - a summary of the overview tabs: each one's colour, bracket preset and columns
  - the ship label
  - the probe formations
  - the drone groups, and how many drones each holds
  - the character's public profile
- **Copies settings between characters and accounts:**
  - a ready-made choice: the window layout, the overview and brackets, the interface, or audio, camera and graphics
  - the whole file, to one character or to many at once
  - or only the sections you pick: window layout, overview tab presets, bracket presets, overview options, ship label
  - or groups of settings: the whole overview, probe formations, suppressed dialogs, audio, camera and graphics, market filters, module slots, window tab groups, Neocom, chat channels, info panels, docked panels and search history
  - sections and groups can go to one file or to many at once
  - before anything is written, it shows you what will change, and **Undo** puts the files back straight afterwards
  - groups of characters and copies you repeat can be saved and run again; each run still shows every change first
- **Exports and imports** a character's or account's settings as a JSON file you can keep or share, and exports an account's overview as the `.yaml` file the game's own Overview Settings can import.
- **Makes and applies overview packs:** a small `.evpack` file of bracket presets, tab presets, overview options and the ship label, for sharing with other EVEMA players. Installing one checks it first, and applying one goes through the same review and backups as an import. A pack holds settings only, never anything that runs, and never your account's name or IDs.
- **Moves a whole setup** to another computer: **Export everything** saves every settings file of every install and profile, with EVEMA's names and pairings (and its backups, if you like), in one checksummed `.zip`. **Import everything** shows what's new and what differs before writing anything.
- **Edits settings directly:** the ship label, window positions, probe formations, and the "always show ship brackets" preference. Bracket presets can be edited too, from the Overview tab's **⋯** → **Edit presets…**; the overview itself is changed in the game, and EVEMA copies and shares it.
- **Sets up drone groups** on one account or many: an empty group for each kind of drone you pick, named from its stats at all skills V (worked out from Fenris Creations' published static data, built into EVEMA). You drag your drones in, in game. Groups that hold drones are never removed, and groups you made yourself are never touched.
- **Backs up before every change.** It makes a timestamped backup before it writes to any file, and you can restore any backup from the app, onto its own file or another of the same kind. You can also save named backups, which are kept until you delete them. Files are written in a way that can't leave a half-written file behind, even if something crashes mid-save.
- **Waits for EVE to close.** The client saves its own settings when it logs out or closes, which would overwrite a change made while it was open (and a change only shows up at the next login anyway). So while any client is running, EVEMA holds each change back, shows it in a banner, and writes it once every client has closed, on top of whatever the client saved on its way out. **Write now** and **Discard** are in the banner, and EVEMA asks before quitting with changes still waiting.

### Partnership tab

- Reads the combat log files the client writes (the `Gamelogs` folder) to list the pilots in them, to help run in-game giveaways. It only reads the logs; it never changes them.

### Tools tab

- Keeps a list of community tools: a few built in (EVE-O Preview, Pyfa, EveLens, Priceall, SMT, PELD), plus any program you add yourself.
- Finds where each one is installed, shows its version, and launches it when you click **Launch**. The tool runs as its own program, the same as if you had double-clicked it.
- **Get latest** downloads a tool's newest release from its GitHub page, but only when you click, and only after showing you exactly what it will download. It checks the file's SHA-256 checksum against the one GitHub publishes and refuses the download if the two don't match or no checksum exists.
- **Check for updates** compares the tools you have installed with their latest releases, only when you click.
- **Uninstall** removes only what EVEMA itself downloaded. It never deletes a folder you pointed it at.
- Each built-in tool carries a plain-language note on what it does to the game (for example, whether it only reads files, arranges windows, or hooks into the client), so you can judge it yourself. EVEMA lists these tools; it doesn't vouch for them.

## What it connects to

- **ESI** (Fenris Creations' official public API, `esi.evetech.net`) and Fenris Creations' image server, for character names, public profiles, portraits and logos, drone icons, and item group names. No login and no account access: only public information. Responses are cached and reused for as long as Fenris Creations allows.
- **GitHub**, to check for a newer EVEMA release at startup (you can turn this off in Settings), to download that release when you click **Install and restart**, and for the Tools tab's Get latest and Check for updates buttons when you click them.

Nothing else. EVEMA has no telemetry or analytics, and it never uploads your settings, logs or anything else.

## What it won't do

These are firm lines, not "not yet":

- **No changes to the game client.** No patching, no injected code, no loaded DLLs.
- **No reading the game's memory.**
- **No reading or altering network traffic** between the client and Fenris Creations' servers.
- **No automation or input.** No macros, no keystroke or mouse broadcasting, and nothing that plays the game for you.
- **No logging in as you.** EVEMA never asks for your EVE account or SSO login.
- **Nothing third-party runs inside EVEMA.** Managed tools run as their own programs, and only when you click Launch.
- **Nothing it downloads runs unless you click for it.** A tool starts only when you click **Launch**. A new EVEMA installs only when you click **Install and restart**, and only after the download matches the SHA-256 checksum GitHub publishes for it. EVEMA never asks for administrator rights and never installs certificates.
- **No writes without a backup.**

Requests that would cross these lines will be closed, however useful they would be.

## Good to know

- **Waiting changes need EVEMA open.** A change held back while EVE runs is written when EVE closes, so leave EVEMA running until then (it asks before you quit). With several clients open, it waits for all of them.
- **Keybinds can't be copied section by section yet.** They're copied only as part of a whole-file copy.
- **Other servers:** ESI only knows Tranquility characters. Singularity characters are looked up there anyway and marked "(via Tranquility)", since Singularity is a copy of Tranquility; Thunderdome characters are shown by ID. Serenity (the Chinese server) hasn't been tested: its files show if its client keeps them in the usual place.
- **macOS:** the app isn't notarized, so the first launch needs right-click → **Open**. On macOS, and in Wine setups other than Steam/Proton, EVEMA may not detect a running client, in which case changes are written straight away, as if EVE were closed.
- **Where EVEMA keeps its own data:** its preferences, backups, cache and logs live in its own folder, never inside EVE's. **Settings → Advanced → Open logs folder** takes you there.

## Found a problem?

[Open an issue](https://github.com/Darkbird7/EVEMA/issues/new/choose). If a change went wrong, you can restore the previous version from the file's backups in the Characters tab.
