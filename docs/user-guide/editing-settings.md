# Editing settings

EVEMA can change some settings directly, without copying from another character. Select a character or account in **Local Files**, then use the detail tabs on the right.

Every edit backs up the file first, and every edit waits for EVE to close if a client is running. See [Backups, and changes while EVE is running](backups-and-eve-running.md).

The ship label and probe formations live in the **account** file. If you select a character, the **Ship Labels** tab shows its [paired account](getting-started.md#3-pair-each-character-with-its-account), and your edits change that account, so every character on it gets them.

Overview tabs and bracket presets can't be viewed or edited in EVEMA for now; that part of EVEMA is being reworked. You can still copy them between accounts with [Copy sections to](copying-settings.md#copy-only-some-sections), and export the whole overview for the game from the **Ship Labels** tab's **Export ▾**.

## Window layout

The **Window Layout** tab draws every window at its saved position and size, with a table of the same windows below.

- **Preview at:** shows how the layout would look at another resolution. EVE pulls windows back on screen when you move to a *smaller* resolution, and this preview copies that. Moving to a *larger* resolution doesn't rescale anything, so the layout renders small and out of place, the same as in game.
- **Move or resize a window:** drag it, or drag its edges, on the canvas. This only works with **Preview at:** set to the native resolution.
- **Show all / Hide all**, and the **Preview** column in the table, choose which windows are drawn. They don't change the file.
- **Undo** steps back one change, **Reset** drops every unsaved change, and **Save changes** writes them.
- **Export…** saves some or all of the windows to a file, and **Import…** applies such a file to the selected character. Private conversations, agent windows and windows known only by a number are left out of exports by default, because they reveal who you talked to or mean nothing to another character. Import only adds or overwrites positions: it never removes a window that's already saved.
- **Restore backup…** puts back an earlier version of this character's file.

A window outlined in red hangs off the edge of the screen at that resolution.

## Ship label

**Always show ship brackets in space** (at the top of the **Ship Labels** tab) shows every ship's label all the time, not only when selected. It's a client launch preference stored in `prefs.ini`, not part of the account, so it applies to every account in this settings profile and takes effect after you restart the client.

Below it, the tab shows a preview of the account's ship label. **Edit…** opens the editor:

- The label is a list of **segments** (for example corporation, alliance, pilot name, ship type and ship name), plus line breaks. **Add segment**, **Add line break**, **Up**, **Down** and **Remove** arrange them.
- For each segment you can set it **Enabled**, add **Pre-text** and **Post-text** (such as brackets around a ticker), and choose a **Color**, **Style** and **Font size**. Leaving a colour unchecked, or a style as a dash, uses the client's default.
- **Save** writes the label; **Cancel** drops your changes.

**Export ▾** saves the label for use elsewhere: **In game (.yaml)…** writes the whole overview, label included, as a file you can import from the client's Overview Settings, and **Step by step (.txt)…** writes instructions for typing the label into EVE's own editor by hand.

## Probe formations

Your saved probe formations live in the **account** file. Select an account, or a character paired with one, and open the **Probe Formations** tab. It lists the formations; select one to see it around your ship, with each probe's range and how far off-centre it is.

![Probe Formations tab](../images/local-files-probe-formations.png)

To change them, click **Edit…** (or right-click the account and choose **Probe formations…**). The editor opens in its own window:

![Probe formation editor](../images/probe-formations.png)

- **Formations** (left): **Add**, **Duplicate**, **Move up**, **Move down** and **Delete**. Select one to edit it, and type its name under **Name**.
- **Preview** (middle): the formation around your ship, with North/South, West/East and Up/Down axes. Drag to turn it, scroll to zoom, or pick **Top**, **Front**, **Side** or **Reset**.
- **Probes** (right): each probe's distance from the ship to the West, Up and North (negative for East, Down and South), and its range. Type plain numbers for km, or add **m** or **au**; far-out positions are shown in AU. **Every probe's range** sets them all at once. A formation holds up to 8 probes.
- **Start from a preset** and **Pattern** replace the selected formation's probes. Patterns (ring, line, sphere, pinpoint) take a count, a spread and an axis. Presets such as **Drifter** and the **Stack** ones are close-range layouts, measured in km.
- **Transform** scales, rotates, mirrors or moves the whole formation.
- **Undo** and **Redo** step through your edits, and **Save** writes them, with a backup, like every other change.

**Keep formations centred.** In game, a formation is placed around the probes' current average position, not around your ship. So a formation whose probes don't average out on the ship drifts that far every time you apply it. Below the preview, EVEMA tells you how far off-centre a formation is, and **Balance** adds or moves one probe to centre it.

If the file changes while the window is open, for example because EVE saved it when you logged out, EVEMA offers **Reload**. Closing with unsaved changes asks first.
