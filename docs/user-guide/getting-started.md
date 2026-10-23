# Getting started

This page takes you from a fresh install to your first copied setting. It takes about five minutes.

## 1. First launch

The first time EVEMA starts, it shows a short **Welcome to EVEMA** window:

- **Theme:** Dark or Light.
- **EVE locations:** the **Settings folder** and **Combat log folder**. EVEMA finds these itself in the usual places, including Steam/Proton and Wine prefixes on Linux and macOS. Only change them if your EVE install is somewhere unusual.
- **Components:** which tabs to show (Local Files, Partnership, Tools). You can switch them on or off later.

Click **Get started**, or **Skip (use defaults)**. Everything here can be changed later in the **Settings** tab.

> **Tip:** if EVEMA found more than one EVE install (common with several Wine prefixes), the Settings tab lists them all under **EVE locations**; click **Use this** next to the right one.

## 2. Find your characters and accounts

Open the **Local Files** tab. The left side lists every settings file EVEMA found, under **Discovered settings files**:

- **Characters** are shown by name, looked up from EVE's public API, which only knows Tranquility. Singularity is a copy of Tranquility, so its characters are looked up there too and marked **(via Tranquility)**: a character made on Singularity since the last copy may not match. Thunderdome characters are shown by ID. The **Server** column, and its filter, say which server each file belongs to.
- **Accounts** have no public name, so they're listed by ID. Give each one a name you'll recognise: right-click it and choose **Rename Account…**. The name is only stored in EVEMA.

Click any row to see its details on the right. Use the funnel icons in the **Name**, **Type** and **Server** column headers to filter the list, and **Refresh** after EVE has saved new files.

## 3. Pair each character with its account

A character's overview, ship label and probe formations live in its *account's* file (see [the two file types](README.md#two-words-used-everywhere)). To see them when you select the character, pair the two:

1. Select the character.
2. Click the **⇄** button next to its name, above the detail tabs.
3. Under **Paired account:**, pick the account that character belongs to.

EVEMA remembers the pairing. **Clear** removes it.

You can see the pairings in the list:

- The **Account** column shows each character's account, or **Not paired**, and each account's number of characters. Click the column heading to sort, which puts each account's characters together.
- Select a character, and its account's row is tinted **violet** and the other characters on that account **amber**, so every file that goes with it, and which kind it is, shows at a glance. Select an account, and all of its characters are tinted amber, and the header above the tabs lists them. Select several rows at once (say, to copy settings to them) and the tints stay while they all belong to one account; pick rows from different accounts and the tints step aside.

> **Not sure which account a character is on?** Log in with only that character, log out, close the client, then click **Refresh** in EVEMA. The character file and the account file with the newest **Last Modified** times belong together.

## 4. Look around

In the list, click a column heading to sort by it, drag a column's edge to resize it, and **double-click the edge** to fit the column to its contents. EVEMA remembers the widths you set, and where you leave the divider between the list and the details, like the window size.

With a character selected, the detail tabs show:

- **Profile:** public information from EVE's API (corporation, alliance, history) and what EVEMA can see on this computer.
- **Window Layout:** every window's position drawn to scale. **Preview at:** shows how the layout would look at another screen resolution.
- **Ship Labels:** the paired account's ship label, and the "always show ship brackets in space" preference.
- **Probe Formations:** the paired account's saved probe formations, with **Edit…** to change them.

Nothing is changed by looking. EVEMA only writes when you click something that says so, and it always makes a [backup](backups-and-eve-running.md) first.

## 5. Copy your first setting

A common first job: give a new character the same window layout as your main.

1. **Close every EVE client.** (If one is open, EVEMA will hold the change until it closes; see [why](backups-and-eve-running.md#changes-while-eve-is-running).)
2. In **Local Files**, right-click your main character.
3. Choose **Copy sections to**, then the new character.
4. In the **Copy sections** window, tick the window layout changes you want, and click **Copy**.
5. Log the new character in. Its windows are where your main's are.

Next: [Copying settings](copying-settings.md) covers whole-file copies, copying to many characters at once, and sharing settings as a file.
