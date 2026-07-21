# General Troubleshooting

Common issues encountered when running modern software on Windows 7, and general fixes — separate from app-specific pages.

## App won't install / installer refuses to run

- Check if the installer detects OS version and blocks Win7 explicitly — sometimes running it in Windows 8/10 Compatibility Mode (right-click → Properties → Compatibility) is enough on its own, without needing VxKex.
- If that fails, try through VxKex.

## App installs but crashes on launch

- Missing runtime is the most common cause: install/update the Visual C++ Redistributable (both x86 and x64 versions) and the relevant .NET Framework version first.
- Then retry, with VxKex if the app needs it.

## Low RAM / low-spec machines (2–4GB RAM)

- Increase virtual memory (paging file) size manually: System Properties → Advanced → Performance Settings → Advanced → Virtual Memory. A larger paging file often resolves crashes on installers that assume more physical RAM than the machine has.
- Close background services/antivirus real-time scanning temporarily during installation if an installer hangs or fails silently — some antivirus products interfere with older/unsigned installers, mistaking them for threats.
- Prefer lightweight browsers (Pale Moon, Midori) over Chromium-based ones on very low-RAM machines.

## Antivirus flags legitimate installers

- Older or archived installers (e.g. from Internet Archive) sometimes get flagged by antivirus heuristics simply because they're unsigned or uncommon, not because they're actually malicious.
- Verify the source is a known-good archive/mirror before whitelisting — don't blanket-disable antivirus permanently, just temporarily during the specific install.

## 32-bit vs 64-bit Windows 7

- Always confirm which architecture you're running (Control Panel → System) before downloading VxKex or any installer — 32-bit Win7 has a smaller set of compatible modern software than 64-bit Win7.
