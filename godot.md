# Godot Engine on Windows 7

Godot 4.0 runs on Windows 7, but the default renderer (Vulkan) doesn't work reliably on older Win7 hardware/drivers. Forcing the OpenGL3 renderer fixes this.

## Working version

**Godot 4.0**

## Steps

### Step 1: Download

1. Download the standard Godot 4.0 Windows build from godotengine.org — no special Win7 build exists or is needed.
2. Extract the zip to a folder of your choice (Godot is portable, no installer).

### Step 2: Launch with the OpenGL flag

**Option A — one-time, via Command Prompt:**
1. Open Command Prompt and navigate to the folder containing `Godot_v4.0-stable_win64.exe`.
2. Run:
   ```
   Godot_v4.0-stable_win64.exe --rendering-driver opengl3
   ```

**Option B — permanent shortcut (recommended):**
1. Right-click `Godot_v4.0-stable_win64.exe` → **Create shortcut**.
2. Right-click the new shortcut → **Properties**.
3. In the **Target** field, add the flag after the existing path, so it reads:
   ```
   "C:\Path\To\Godot_v4.0-stable_win64.exe" --rendering-driver opengl3
   ```
4. Click OK. Now double-clicking this shortcut always launches Godot with OpenGL — no terminal needed going forward.

### Step 3: If exporting projects for other Win7 machines

1. In Godot's Project Export settings, ensure the export preset also targets the OpenGL/Compatibility renderer (not Vulkan/Forward+), matching Step 2 above.
2. Test the exported build with the same `--rendering-driver opengl3` flag if it doesn't launch correctly on its own.

## Notes

- Without the flag, Godot 4.0 may fail to open the editor window or crash on start on Win7 — this flag resolves that in testing.
- If you're also building/exporting Godot projects, exports should still target OpenGL for the same reason if the exported game needs to run on similar old hardware.
