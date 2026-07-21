# Notion on Windows 7

Current Notion desktop builds require Windows 10+. An older version runs fine on Win7.

## Working version

**Notion 2.0.41**

## Steps

### Step 1: Get the right version

1. Search for "Notion 2.0.41 Windows installer" — since Notion's official site only offers the current build, you'll need an older-version archive or trusted third-party mirror.
2. Confirm the version number is exactly 2.0.41 before downloading.

### Step 2: Install

1. Run the installer directly — **no VxKex needed** for this version.
2. Complete the setup wizard and log in with your Notion account.

### Step 3: Disable auto-update immediately

1. Open Notion, click your workspace/profile icon (usually top-left).
2. Look for **Settings** → check for an update-related toggle or preference.
3. Disable automatic updates if the option exists.
4. If there's no in-app toggle in this version, avoid staying logged in for long unattended periods where a background update could trigger.

### If Notion already auto-updated and broke

1. Uninstall Notion (Control Panel → Uninstall a program).
2. Delete the leftover folder at `%AppData%\Notion` to clear cached update files.
3. Reinstall version 2.0.41 from Step 1.

## Notes

- Core note-taking, databases, and sync all function normally on this version.
- If Notion refuses to launch after an accidental update, reinstall 2.0.41 over it.
