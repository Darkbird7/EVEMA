# Partnership

The **Partnership** tab helps run in-game giveaways: it builds a list of pilots you've fought from your combat logs, then randomly assigns skins from your inventory to them. It only reads the logs and never changes them.

The tab has three parts: **Pilot Scan**, **Skin Inventory** and **Assignment**.

## 1. Find the pilots (Pilot Scan)

1. Check the **Combat log folder:**. It's your EVE `Gamelogs` folder, found automatically; use **Browse…** if yours is elsewhere.
2. Optional: set a date range with **From:** and **To:** (`yyyy-mm-dd`). Leave both blank to scan everything.
3. Under **Count as fought:**, choose what counts as an encounter:
   - **Damage / EWAR**: weapon hits or misses and energy neutralization, in either direction.
   - **Healed me**: remote armour, shield or hull repair you received.
   - **Tackled me**: warp scrambles, disruptors or webs applied to you.
4. Click **Scan Logs**.

The table lists each pilot with how often you met them, the ships you saw them in, and when you last saw them. Only pilots ticked in the **In Pool** column take part in the draw.

Tidy the list:

- **Add Pilot** adds someone by hand.
- The checkbox in the **In Pool** column's header puts every pilot in the pool, or takes every pilot out. **⋯** → **Invert Selection** swaps them.
- While any pilots are ticked, a bar under the table offers **Remove Checked**, which takes them out of this list, and **Blacklist Checked**, which moves their names (NPCs, drones, your own alts) to the blacklist so future scans skip them. **⋯** → **Manage Blacklist…** edits that list.

## 2. Load the prizes (Skin Inventory)

- **Import** replaces the inventory with a pasted list. In game, open the container holding the skins, select the items, copy them, and paste into the **Import Skin Inventory** window. One line per skin, name then count.
- **Add Skin** and **Remove** edit the list by hand.

## 3. Run the draw (Assignment)

1. Optional: under **Options**, enter a **Seed**. The same seed always gives the same draw, so you can preview a result, or let others check it.
2. Optional: under **Options**, set **Max winners**.
3. Click **Run Draw**. Pilots and skins are shuffled separately and paired off one to one until either runs out.

The results list who gets which skin, plus **Pilots with no skin left** and **Leftover skin inventory**.

- **⋯** → **Copy Results** or **Export to File…** to share the result.
- **Apply to Inventory** takes each assigned skin off the inventory, ready for the next giveaway.
