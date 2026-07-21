# Perplexity Desktop on Windows 7

Perplexity's desktop app isn't officially supported on Windows 7, but it runs successfully through VxKex Next.

## Steps

1. Install [VxKex Next](../vxkex-setup.md) first if you haven't already.
2. Download the standard Perplexity Desktop Windows installer.
3. **Enable VxKex on the installer itself first:**
   - Right-click the downloaded installer `.exe` → **Properties** → **VxKex** tab → check **"Enable VxKex for this program"** → Apply → OK
   - Double-click to run the installer normally — it now installs through the shim
4. After install, the main app `.exe` (usually in `C:\Program Files\Perplexity\`) needs the same treatment: right-click → **Properties** → **VxKex** tab → check **"Enable VxKex for this program"** → Apply → OK
5. From then on, just launch the app normally (double-click, shortcut, Start Menu) — VxKex is remembered per-file, no need to repeat this each time.

## Notes

- Running it directly without VxKex fails to launch in testing — the shim step is required, unlike some of the browsers in this guide.
- If you don't need the desktop app specifically, the web version works in any of the Win7-compatible browsers listed in [browsers.md](browsers.md) with no compatibility work needed at all.
