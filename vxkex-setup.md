# VxKex Next Setup

[VxKex Next](https://github.com/vxsz/VxKex) is a compatibility layer that lets many Windows 10/11-targeted apps run on Windows 7 by backfilling missing APIs. Most entries in this guide assume it's already installed.

## Installation

1. Download the latest VxKex Next release from the official GitHub releases page.
2. Extract to a permanent location (e.g. `C:\VxKex`) — don't run it from a temp folder or USB stick, since apps will reference this path.
3. Run the installer/setup executable as Administrator.
4. Reboot after install (recommended, not always required).

## How to enable/activate VxKex for an app

VxKex Next integrates directly into the file's **Properties** dialog — there's no separate right-click "Run with VxKex" entry. Here's the real method:

![VxKex Properties tab](images/vxkex-properties-tab.jpeg)

### Steps

1. Right-click the app's `.exe` file → **Properties**.
2. A new tab called **VxKex** appears next to General, Compatibility, etc. (only shows up after VxKex is installed).
3. Click the **VxKex** tab.
4. Check **"Enable VxKex for this program"** under Compatibility mode.
5. Optional: check **"Report a different version of Windows"** and pick a version (e.g. Windows 10) from the dropdown if the app also does an OS version check on top of needing missing APIs.
6. Click **Apply**, then **OK**.
7. Launch the app normally by double-clicking it — VxKex now applies automatically every time, no need to relaunch through any special menu.

### Advanced options (only touch if the basic toggle isn't enough)

- **Use stronger version reporting** — for apps that check the Windows version more aggressively than normal.
- **Disable VxKex for child processes** — useful if the main app works but a sub-process/updater it launches breaks.
- **Disable all application-specific workarounds** — for troubleshooting only; turns off VxKex's built-in per-app fixes.

### Making it permanent

Nothing extra needed — once "Enable VxKex for this program" is checked in Properties, it stays enabled for that `.exe` every time you open it normally, no shortcut tricks required.

## Common issues

- **App still won't start**: Check whether the app needs a specific redistributable (VC++ Runtime, .NET version) installed separately first — VxKex bridges API gaps, it doesn't install missing runtimes.
- **Crashes on launch**: Try running VxKex itself as Administrator, then launching the target app from within it.
- **32-bit vs 64-bit**: Confirm you've got the correct VxKex build matching your Windows 7 architecture (32-bit or 64-bit).

## Notes

- VxKex is actively maintained on GitHub — check for newer builds periodically, since compatibility improves over time.
- Not every app needs VxKex — some (like certain browsers) run natively on Win7 with no shim required. Check the specific app page in this guide.
