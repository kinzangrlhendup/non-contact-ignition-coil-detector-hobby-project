# PCB design record

## Current status

The KiCad schematic and board have been created, routed and visually reviewed. The user previously reported that electrical-rules and design-rules checks completed without errors or violations. The native `.kicad_pro`, `.kicad_sch` and `.kicad_pcb` files have not yet been supplied for repository-level verification.

![KiCad schematic](../images/kicad-schematic.png)

![PCB layout](../images/pcb-layout.png)

## Documented design decisions

- Two-layer PCB with a front-copper meander pickup.
- J2 connects the pickup conductor to the sensing circuit.
- TP1 provides access to the raw pickup signal.
- Ground copper is excluded beneath and around the meander, TP1 and pickup feed to reduce pickup loading.
- Four M3 mounting holes are provided.
- SW1 is intended to be a normally-open momentary TEST button for hold-to-test operation.
- Silkscreen identifies the sensing coil, power supply, sensitivity control, firing LED and active buzzer.
- Bhutanese graphics, designer credit and fabrication date are included on the front silkscreen.

## Pre-fabrication review still required

- Import and inspect the native KiCad project.
- Confirm schematic-to-PCB synchronization.
- Confirm every footprint against the purchased part datasheet.
- Confirm electrolytic-capacitor, diode, LED, transistor, regulator and buzzer polarity.
- Confirm LM393 pin mapping and unused comparator treatment.
- Decide the final raw-input bleed resistance after sensitivity testing.
- Check silkscreen-to-pad clearance and text readability in the 3D Viewer.
- Refill copper zones and rerun ERC/DRC.
- Generate and inspect Gerber and drill files in an independent viewer.

## Manufacturing defaults proposed for the first prototype

- Two copper layers
- FR-4, 1.6 mm thickness
- 1 oz copper
- HASL lead-free or ENIG finish
- Green solder mask
- White silkscreen

These are proposed prototype parameters and should be confirmed before ordering.

