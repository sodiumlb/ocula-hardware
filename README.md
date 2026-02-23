# ocula-hardware
Hardware design files for the Oric OCULA ULA replacement project.

## Related projects
[User Documentation](https://github.com/sodiumlb/ocula-docs)
[Firmware](https://github.com/sodiumlb/ocula-pivic-firmware)

## Important notes
OCULA hardware has been designed for low cost assembled production. It is not recommended to attempt manual assembly of anything other than through-hole components (headers, connectors).

Currently only OCULA-is-the-RAM mode is supported by the firmware, which means 2 mux-bridges are required for normal operation. The Micro DVI adapter and cable is optional.

## Main OCULA PCB
See pcb directory for design files for PCB production and PCBA of all surface mounted components. Due to very low clearance inside Oric-1 and Atmos cases, it is recommended to use stacking pin-headers to create flat pins on OCULA to allow low-profile mounting in machines with sockets.

## Mux bridges
The mux bridges use thin PCBs - 0.6mm is the only tested PCB thickness. The 3D printed snap-on frame will require modification if the PCB is different. The mux bridge modification is extremely simple and other solutions can be created. The effort put into this particular mux bridge design is to allow non-destructive but reliable modification of the Oric most people can use.

The current design is best assembled by first snapping the PCB into the 3D printed frame, then soldering in the 8 required pins. Thin, flat, flexible pins are needed here to make good contact with the mux ICs, thus it is recommended making these from the same stacking pin-headers as for the OCULA pins. Take care not to apply too much heat or use too long time, the 3D printed snap-on-frame will warp easily.

## Micro DVI adapter
The micro DVI adapter is optional. See the dvi-micro-adapter for PCB and 3D print adapter design files. The required cable spec is FFC, 20cm, 20pin, 0.5mm pitch, reverse direction (contacts are on opposing side on each end).

The 3D printed Oric adapter is designed to fit in place of the RF modulator. To secure the adapter, a longer screw is needed in place of the original PCB mounting screw fitted next to the RF modulator.


## Using stacking pin row headers to create IC pins
While there are many options for adding IC pins to PCBs, the solution that has provided the best low-cost way to get close to compatible with original IC pins, is to create them from long pinned PCB stacking headers. These have flat pins in a more spring-like metal that serves this alternative application well. 

This example shows 1x20 row 11mm stacking pin row headers.  
![Example stacking pin headers](https://github.com/sodiumlb/ocula-hardware/raw/main/images/pin_row_1x20_11mm_stacking.jpg)
![OCULA low-profile pin jigg](https://github.com/sodiumlb/ocula-hardware/raw/main/images/ocula_low_profile_jigg.jpg)
![OCULA low-profile pins](https://github.com/sodiumlb/ocula-hardware/raw/main/images/ocula_low_profile_pins.jpg)
![OCULA low-profile mounted in system](https://github.com/sodiumlb/ocula-hardware/raw/main/images/ocula_low_profile_in_system.jpg)

# Disclaimer
OCULA is an open source project by and for Oric users. It is provided AS-IS. For more information see each sub-project license agreement.