# Phantom-MX

##   what is this??
Phantom-mx is cutom made keyboard with 87 mechincal switches, roatary encoder and custom built case and qmk firmware. It has 2 layer of functions to switch between as per your need. the case type is integrated plate mount which mean you dont need to lock the plate with case with 1000's of screw

---
##   why phantom-mx??
you may find many other custom keyboard with more features and better than this, but the one thing you will never find is perfect keyboard which is in budget and also meet your needs perfectly. it was built to meet my needs and also in budget. 
<br>
**bonus point**:- it has some really cool silkscreen

---
##   how to assemble it??
### 1. Ordering the PCB
1. **Download Production Files**: Navigate to the `PCB/` directory in this repository and download the Gerber zip file (e.g., `Gerber_Phantom-MX.zip`). Do not extract it.
2. **Choose a Manufacturer**: Upload the zip file to a PCB fabrication service such as JLCPCB, PCBWay, or OSH Park.
3. **Configure Board Settings**: Use the following standard specifications:
   * **Layers**: 2 Layers
   * **Thickness**: 1.6 mm
   * **Surface Finish**: HASL (or ENIG for better pad durability)
4. **Assembly (Optional)**: If you prefer factory assembly for surface-mount components (diodes/sockets), upload the BOM (Bill of Materials) and CPL (Component Placement List / Centroid file) provided in the repository to their PCBA service.

---

### 2. Sourcing Components
Before starting assembly, ensure you have the following components:
* **Microcontroller**: Raspberry Pi Pico (or compatible RP2040 board specified by the schematic)
* **Diodes**: 1N4148 switching diodes (SMD or Through-Hole depending on layout)
* **Switches & Keycaps**: MX-compatible mechanical switches and keycaps
* **Sockets**: Kailh hot-swap sockets (if using the hot-swap PCB variant)
* **Cable**: High-quality USB data cable

---

### 3. Hardware Assembly
1. **Solder Diodes**: Always solder small, low-profile components first. Align the black line (cathode) on each diode with the vertical line/bar indicated on the PCB silkscreen.
2. **Solder Sockets/Switches**: Attach the Kailh hot-swap sockets or directly solder the mechanical switches into position.
3. **Mount the Pi Pico**: Place the Pi Pico onto its designated footprint. You can solder it directly using its castellated edges, or use pin headers/sockets to make the microcontroller removable.
4. **Inspect Joints**: Check all joints under good lighting for solder bridges, cold joints, or missing connections. Clean off any residual flux with isopropyl alcohol.

---

### 4. Flashing the Firmware
The Raspberry Pi Pico handles firmware deployment via a standard mass-storage interface using `.uf2` files.

1. **Locate Firmware**: Find the pre-compiled `.uf2` firmware file in the `Firmware/` folder of this repository (or compile your own via QMK/Vial/KMK).
2. **Activate Bootloader**: Press and **hold** the physical `BOOTSEL` button on your Raspberry Pi Pico board.
3. **Connect to Computer**: While holding the button, plug the USB cable from the Pico into your computer. Release the button once it is plugged in.
4. **Deploy File**: Your computer will mount a new USB storage device named `RPI-RP2`. Drag and drop (or copy-paste) your `.uf2` file directly into this folder.
5. **Completion**: The Pico will automatically flash the firmware, unmount itself, and reboot as a functional USB mechanical keyboard.


    
