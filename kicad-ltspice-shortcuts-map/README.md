# LTspice to KiCad Shortcuts Mapping

This configuration file maps standard KiCad keyboard shortcuts to LTspice to maintain consistent muscle memory between KiCad (PCB design) and LTspice (circuit simulation).

## Shortcut Mappings (Schematic Editor)

The primary shortcuts for the Schematic Editor are mapped as follows:

| Key | LTspice Action |
| :--- | :--- |
| `A` | Place Component |
| `W` | Draw Wire Mode |
| `M` | Move Mode |
| `Ctrl+M` | Drag Mode |
| `Ctrl+D` | Duplicate Mode |
| `Ctrl+R` | Rotate |
| `Ctrl+E` | Mirror |
| `X` | Delete Mode |
| `T` | Place Comment Text |
| `N` | Place Netname |
| `G` | Place Ground |
| `V` | Place Voltage Source |
| `R` | Place Resistor |
| `C` | Place Capacitor |
| `L` | Place Inductor |
| `D` | Place Diode |
| `S` | Place SPICE Directive |
| `Space` | Zoom to Fit |

## How to Import into LTspice 24

LTspice 24 manages keyboard shortcuts via its initialization (`.ini`) file. 

### Method 1: Modify the Default Configuration File (Recommended)

1. Close LTspice 24.
2. Navigate to the LTspice 24 configuration file in your AppData Roaming directory:
   `%APPDATA%\LTspice.ini`
3. Open `LTspice.ini` in a text editor.
4. Locate the shortcut definition sections. Replace or update the following sections with the contents of the `kicad-keyshort.txt` file:
   * `[SchKeyBoardShortCut]` (Schematic Editor)
   * `[AsyKeyBoardShortCut]` (Symbol Editor)
   * `[RawKeyBoardShortCut]` (Waveform Viewer)
   * `[NetKeyBoardShortCut]` (Netlist Editor)
5. Save `LTspice.ini` and launch LTspice 24.

### Method 2: Load via Command Line Switch

Use the `-ini` parameter to avoid overwriting the default configuration.

1. Ensure the shortcuts file is formatted as a complete `.ini` file.
2. Move the file to a permanent location (e.g., `C:\LTspice_Configs\kicad-keyshort.txt`).
3. Right-click the LTspice 24 shortcut on your desktop or Start Menu and select **Properties**.
4. In the **Target** field, append `-ini "<path_to_file>"`. Example:
   `"C:\Program Files\ADI\LTspice\LTspice.exe" -ini "C:\LTspice_Configs\kicad-keyshort.txt"`
5. Click **Apply** and **OK**. Launch LTspice using this modified shortcut.
