# Discord on Windows 7

Current official Discord installers refuse to run on Windows 7. The fix is using an archived, older Windows 7-compatible installer.

## Solution

### Step 1: Get the right installer

1. Go to archive.org and search "Discord Windows 7 installer" (or similar terms).
2. Look for an older Discord build explicitly labeled as Windows 7-compatible — avoid anything labeled as the current/latest release.
3. Download the installer `.exe` to your machine.

### Step 2: Install

1. Run the downloaded installer directly — **no VxKex needed** for this one.
2. Let it install normally, following the on-screen prompts.
3. Log in with your Discord account once installed.

### Step 3: Stop it from auto-updating to an incompatible version

1. Once inside Discord, go to **User Settings** (gear icon near your username).
2. If there's an "Advanced" or update-related section, disable automatic updates if the option is present.
3. If Discord prompts you to update on startup, **decline/skip it** — updating breaks Win7 compatibility.

### If it stops working after an update slipped through

1. Uninstall Discord completely (Control Panel → Uninstall a program).
2. Delete leftover folders in `%AppData%\Discord` and `%LocalAppData%\Discord` to clear cached update files.
3. Reinstall the archived version from Step 1.

## Notes

- Newer Discord installers bundle Electron versions that drop Win7 support entirely, so there's no "just install the latest version" option here.
- If voice/video breaks after any auto-update, reinstall the archived version and disable auto-update if possible.
