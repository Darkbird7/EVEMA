# Getting started

This page takes you from a fresh install to your first copied setting. It takes about five minutes.

## 1. First launch

The first time EVEMA starts, it shows a short **Welcome to EVEMA** window:

- **Theme:** Dark or Light.
- **EVE locations:** the **Settings folder** and **Combat log folder**. EVEMA finds these itself in the usual places, including Steam/Proton and Wine prefixes on Linux and macOS. Only change them if your EVE install is somewhere unusual.
- **Components:** which tabs to show (Characters, Partnership, Tools). You can switch them on or off later.

Click **Get started**, or **Skip (use defaults)**. Everything here can be changed later in **Settings**: the gear at the right end of the tabs.

> **Tip:** if EVEMA found more than one EVE install (common with several Wine prefixes), **Settings** lists them all under **EVE locations**; click **Use this** next to the right one.

## 2. Find your characters and accounts

Open the **Characters** tab. The list on the left shows every settings file EVEMA found, grouped the way you play: each **account** (with its violet mark), its characters beneath it, and any characters not yet paired with an account under **Not paired** at the end.

- **Characters** are shown by name and portrait, looked up from EVE's public API, which only knows Tranquility. Singularity is a copy of Tranquility, so its characters are looked up there too and marked **(via Tranquility)**: a character made on Singularity since the last copy may not match. Thunderdome characters are shown by ID, with their initials instead of a portrait. The time on the right is how long ago the file was last saved.
- **Accounts** have no public name, so they're listed by ID. Give each one a name you'll recognise: select it and choose **⋯** → **Rename Account…** (or right-click it). The name is only stored in EVEMA.

Click any row to see its details on the right. The search box above the list finds a file by name, file name, ID or server. When your files come from more than one server, buttons above the list show one server at a time. The **↻** button looks again after EVE has saved new files.

**Prefer a table?** The table button next to the search box switches to a table with Name, Type, Account, Server and Last modified columns, which you can sort and filter. EVEMA remembers which you chose.

## 3. Pair each character with its account

A character's overview, ship label and probe formations live in its *account's* file (see [the two file types](README.md#two-words-used-everywhere)). To see them when you select the character, pair the two.

**All at once (the quickest way):** while any character is unpaired or any account has no name, a bar above the list says so. Click **Set up now** (or choose **⋯** → **Pair and name…** above the list). One window lists every account with a box for its name, and every character with a choice of account:

- Type a name for each account.
- Pick each character's account. The client saves a character's file and its account's file together when the character logs out, so where an account was saved at the same moment as an unpaired character, EVEMA suggests it: click **Saved together with …: use it**, or **Use all suggestions**.
- Click **Save**. Only the choices you changed are saved, and only in EVEMA; your EVE files aren't touched.

**Not now** hides the bar until more characters or accounts need setting up.

**One character at a time:**

1. Select the character.
2. Click the amber **Not paired · Pair…** chip next to its name, above the detail tabs.
3. Under **Paired account:**, pick the account that character belongs to.

Once paired, the chip reads **Account:** and the account's name; click it to change the pairing.

EVEMA remembers the pairing. **Clear** removes it.

The list shows the pairing straight away: the character moves from **Not paired** to under its account. You can also pair by dragging a character onto its account in the list, or unpair it by dragging it onto **Not paired**. Selecting an account lists its characters in the header above the tabs.

In the table, the **Account** column shows each character's account, or **Not paired**, and each account's number of characters. Selecting a row there tints its account **violet** and the other characters on that account **amber**.

> **Not sure which account a character is on?** Log in with only that character, log out, close the client, then click **Refresh** in EVEMA. The character file and the account file with the newest **Last Modified** times belong together.

## 4. Look around

In the table, click a column heading to sort by it, drag a column's edge to resize it, and **double-click the edge** to fit the column to its contents. EVEMA remembers the widths you set, and where you leave the divider between the list and the details, like the window size.

When you pick a character, the details open on whichever tab you last used for one.

**Settings** (the gear at the right end of the tabs) is one page of settings, each saved as you change it; there's no Apply button. Turn whole tabs on or off under **Tabs**. If you never use some of a character's tabs, click them off under **Tabs → Character details** (an account keeps at least one of Overview, Ship Labels and Probe Formations). The rarely needed settings (window size, logs and the resets) are folded under **Advanced**. **Advanced → Reset settings** puts every setting back to its default; click **Undo** in the status bar straight afterwards to change your mind.

With a character selected, the detail tabs show:

- **Profile:** public information from EVE's API (corporation, alliance, history) and what EVEMA can see on this computer.
- **Window Layout:** every window's position drawn to scale. **Preview at:** shows how the layout would look at another screen resolution.
- **Ship Labels:** the paired account's ship label, and the "always show ship brackets in space" preference.
- **Probe Formations:** the paired account's saved probe formations, with **Edit…** to change them.

Nothing is changed by looking. EVEMA only writes when you click something that says so, and it always makes a [backup](backups-and-eve-running.md) first.

## 5. Copy your first setting

A common first job: give a new character the same window layout as your main.

1. **Close every EVE client.** (If one is open, EVEMA will hold the change until it closes; see [why](backups-and-eve-running.md#changes-while-eve-is-running).)
2. In **Characters**, select your main character and click **Copy to…**.
3. Tick the new character, click **Next**, choose **Window layout**, and click **Review changes**.
4. In the **Copy sections** window, check the window layout changes, and click **Copy**.
5. Log the new character in. Its windows are where your main's are.

Next: [Copying settings](copying-settings.md) covers the other things you can copy, copying to many characters at once, and sharing settings as a file.
