# LTspice to KiCad Shortcuts Mapping

This configuration file maps standard KiCad keyboard shortcuts to LTspice to maintain consistent muscle memory between KiCad (PCB design) and LTspice (circuit simulation).

## Shortcut Mappings (Schematic Editor)

The primary shortcuts for the Schematic Editor are mapped as follows:

| Key | LTspice Action |
| :--- | :--- |
| `A` | Place Component[cite: 1] |
| `W` | Draw Wire Mode[cite: 1] |
| `M` | Move Mode[cite: 1] |
| `Ctrl+M` | Drag Mode[cite: 1] |
| `Ctrl+D` | Duplicate Mode[cite: 1] |
| `Ctrl+R` | Rotate[cite: 1] |
| `Ctrl+E` | Mirror[cite: 1] |
| `X` | Delete Mode[cite: 1] |
| `T` | Place Comment Text[cite: 1] |
| `N` | Place Netname[cite: 1] |
| `G` | Place Ground[cite: 1] |
| `V` | Place Voltage Source[cite: 1] |
| `R` | Place Resistor[cite: 1] |
| `C` | Place Capacitor[cite: 1] |
| `L` | Place Inductor[cite: 1] |
| `D` | Place Diode[cite: 1] |
| `S` | Place SPICE Directive[cite: 1] |
| `Space` | Zoom to Fit[cite: 1] |

## How to Import into LTspice 24

LTspice 24 manages keyboard shortcuts via its initialization (`.ini`) file. 

### Method 1: Modify the Default Configuration File (Recommended)

1. Close LTspice 24.
2. Navigate to the LTspice 24 configuration file in your AppData Roaming directory:
   `%APPDATA%\LTspice.ini`
3. Open `LTspice.ini` in a text editor.
4. Locate the shortcut definition sections. Replace or update the following sections with the contents of the shortcuts file:
   * `[SchKeyBoardShortCut]` (Schematic Editor)[cite: 1]
   * `[AsyKeyBoardShortCut]` (Symbol Editor)[cite: 1]
   * `[RawKeyBoardShortCut]` (Waveform Viewer)[cite: 1]
   * `[NetKeyBoardShortCut]` (Netlist Editor)[cite: 1]
5. Save `LTspice.ini` and launch LTspice 24.

### Method 2: Load via Command Line Switch

Use the `-ini` parameter to avoid overwriting the default configuration.

1. Ensure the shortcuts file is formatted as a complete `.ini` file.
2. Move the file to a permanent location (e.g., `C:\LTspice_Configs\kicad_shortcuts.ini`).
3. Right-click the LTspice 24 shortcut on your desktop or Start Menu and select **Properties**.
4. In the **Target** field, append `-ini "<path_to_file>"`. Example:
   `"C:\Program Files\ADI\LTspice\LTspice.exe" -ini "C:\LTspice_Configs\kicad_shortcuts.ini"`
5. Click **Apply** and **OK**. Launch LTspice using this modified shortcut.
