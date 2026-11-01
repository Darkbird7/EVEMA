# Tools

The **Tools** tab keeps track of the community tools you use alongside EVE: where they're installed, which version you have, and whether a newer one is out. It can also download and update them for you, but only when you click.

EVEMA lists these tools; it doesn't vouch for them. Each built-in tool has a short note on what it does to the game (for example, whether it only reads files or arranges windows) so you can judge for yourself.

## Built-in tools

EVE-O Preview, Pyfa, EveLens and Priceall are listed out of the box. Most are Windows programs; where a tool doesn't run on your system, EVEMA says so instead of offering to launch it.

Select a tool on the left to see its details on the right. The main button under its name is the next thing to do: **Launch** once it's installed, or **Get latest…** if EVEMA can fetch it for you. Everything else is under the **⋯** button at the top right of the details.

## Point EVEMA at a tool you already have

EVEMA looks for each tool in the usual places. If it doesn't find yours, click **I already have it…**, then:

- **Choose folder…** if you have the tool's folder.
- **Choose program file…** to pick the program itself. Use this for a Linux `.AppImage`, which EVEMA accepts under any file name. (Mark the AppImage as executable first, or it won't start.)

Under **⋯**, **Open folder** shows the tool's folder, and **Forget location** makes EVEMA forget it. Neither moves or changes the tool's files.

## Launch a tool

Click **Launch**. The tool starts as its own program, exactly as if you had double-clicked it. EVEMA doesn't run anything inside itself and doesn't watch the tool afterwards.

## Install or update from GitHub

For tools published on GitHub:

1. Click **Get latest…** (for an installed tool, **Update…** when there's a newer release, or **⋯** → **Get latest…**). EVEMA looks up the newest release and shows exactly what it would download. Nothing is downloaded yet.
2. Click **Download and install** to go ahead.

EVEMA checks the download against the SHA-256 checksum GitHub publishes, and refuses it if the two don't match or no checksum exists. It unpacks into its own tools folder and leaves your other versions alone.

**Check for updates** (top of the list) compares every installed tool with its latest release. It only looks; nothing is downloaded.

## Uninstall

**Uninstall…** appears only for copies EVEMA downloaded itself, and deletes every version it downloaded for that tool. It never deletes a folder you pointed it at.

## Add your own tool

1. Click **Add…** and fill in at least a name and the **Program file** (the file that starts the tool, such as `MyTool.exe`), and tick the systems it **Runs on**.
2. Optional: fill in **Owner**, **Repository** and **Release file name** under **Updates from GitHub** to turn on **Get latest** and **Check for updates** for it. Fill in all three or none. The release file name must match the file on the release exactly.

**⋯** → **Edit details** changes any tool's entry later, and **⋯** → **Remove from EVEMA** takes it off the list. Both only affect EVEMA's list, never the tool's files.

Want a tool built in for everyone? [Suggest it](https://github.com/Darkbird7/EVEMA/issues/new/choose) with the **Add a tool to the Tools catalog** form.
