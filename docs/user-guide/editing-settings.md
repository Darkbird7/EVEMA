# Editing settings

EVEMA can change some settings directly, without copying from another character. Select a character or account in **Local Files**, then use the detail tabs on the right.

Every edit backs up the file first, and every edit waits for EVE to close if a client is running. See [Backups, and changes while EVE is running](backups-and-eve-running.md).

Overview, brackets and ship label settings live in the **account** file. If you select a character, these tabs show its [paired account](getting-started.md#3-pair-each-character-with-its-account), and your edits change that account, so every character on it gets them.

## Window layout

The **Window Layout** tab draws every window at its saved position and size, with a table of the same windows below.

- **Preview at:** shows how the layout would look at another resolution. EVE pulls windows back on screen when you move to a *smaller* resolution, and this preview copies that. Moving to a *larger* resolution doesn't rescale anything, so the layout renders small and out of place, the same as in game.
- **Move or resize a window:** drag it, or drag its edges, on the canvas. This only works with **Preview at:** set to the native resolution.
- **Show all / Hide all**, and the **Preview** column in the table, choose which windows are drawn. They don't change the file.
- **Undo** steps back one change, **Reset** drops every unsaved change, and **Save changes** writes them.
- **Export…** saves some or all of the windows to a file, and **Import…** applies such a file to the selected character. Private conversations, agent windows and windows known only by a number are left out of exports by default, because they reveal who you talked to or mean nothing to another character. Import only adds or overwrites positions: it never removes a window that's already saved.
- **Restore backup…** puts back an earlier version of this character's file.

A window outlined in red hangs off the edge of the screen at that resolution.

## Overview

The **Overview** tab lists the account's overview tabs, which bracket preset each one uses, and its columns.

- **Overview flags** (expand the section) are the overview's on/off options. Ticking or unticking one saves it straight away, with a backup.
- **Edit brackets…** changes which preset the selected tab uses, and that preset's always-shown brackets.

## Brackets

The **Brackets** tab is the bracket preset catalogue for the account.

- **Search presets** and **Unused only** narrow the list. Select a preset to see its groups and states, which tabs use it, and how it compares with another preset (**Compare with**).
- **Duplicate…**, **Rename…** and **Delete…** manage your own presets. Built-in presets can't be changed: duplicate one to make an editable copy.
- Add or remove groups and states in the detail pane, then save.
- **Assign to selected tab** makes the overview tab you picked use this preset. **Tab assignments → Edit…** does the same from the tab's side, and also edits that preset's always-shown list.
- **Copy preset to…** copies the selected preset to another account.
- EVE doesn't publish what its numbered *states* mean. Select one, type a name, and click **Save name**; EVEMA shows your name wherever that number appears. The names are kept on your computer only.

**Always show ship brackets in space** (at the bottom of the tab) shows every ship's label all the time, not only when selected. It's a client launch preference stored in `prefs.ini`, not part of the account, so it applies to every account in this settings profile and takes effect after you restart the client.

## Ship label

The **Ship Labels** tab shows a preview of the account's ship label. **Edit…** opens the editor:

- The label is a list of **segments** (for example corporation, alliance, pilot name, ship type and ship name), plus line breaks. **Add segment**, **Add line break**, **Up**, **Down** and **Remove** arrange them.
- For each segment you can set it **Enabled**, add **Pre-text** and **Post-text** (such as brackets around a ticker), and choose a **Color**, **Style** and **Font size**. Leaving a colour unchecked, or a style as a dash, uses the client's default.
- **Save** writes the label; **Cancel** drops your changes.

**Export ▾** saves the label for use elsewhere: **In game (.yaml)…** writes the whole overview, label included, as a file you can import from the client's Overview Settings, and **Step by step (.txt)…** writes instructions for typing the label into EVE's own editor by hand.
