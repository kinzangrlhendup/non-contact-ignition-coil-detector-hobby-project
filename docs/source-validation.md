# KiCad source validation

## Import record

The native KiCad files were supplied and imported on 18 July 2026.

| File | SHA-256 |
| --- | --- |
| `Ignition_Coil_Detector.kicad_pro` | `6140f48b9ffbdea2eed19285a9f2ac122120039b180e78674a9bb66ca77e1df9` |
| `Ignition_Coil_Detector.kicad_sch` | `0b0b4e3ca8055a142972ef1ba0f5a271d50540577bd7f7c8e5fec9de8ce2572b` |
| `Ignition_Coil_Detector.kicad_pcb` | `b03db34e6e72c35c124d9934e2080887b5cfa8cce189beba1c0e14caec3a8f7f` |

The repository copies were compared byte-for-byte with the supplied files before publication.

## Structural checks

| Check | Result |
| --- | --- |
| Project-file JSON parsing | Valid |
| Schematic S-expression balance | 6,050 opening and 6,050 closing parentheses |
| PCB S-expression balance | 32,711 opening and 32,711 closing parentheses |
| KiCad file generator/version | KiCad 10.0 |
| PCB thickness setting | 1.6 mm |
| Electrical/component footprints | 29 |
| Board-only M3 mounting holes | 4 |
| Routed segments | 207 |
| Copper zones | 2 |
| Vias | 0 |

The component references present on the PCB are:

```text
BZ1, C1-C6, D1-D5, J1-J2, Q1, R1-R8, R10,
RV1, SW1, TP1, U1 and U2
```

The four board-only mounting holes use KiCad's `REF**` placeholder, which is expected for non-schematic mechanical footprints.

## ERC and DRC status

The designer previously ran KiCad ERC and DRC and reported no errors or violations. This environment does not contain `kicad-cli`, so those checks were not independently rerun during repository import.

Before manufacturing, open the project in KiCad 10.0, refill the zones, rerun ERC and DRC, and save the generated reports or screenshots under `manufacturing/reports/`.

## Excluded session files

The following supplied files were intentionally not committed:

- `~Ignition_Coil_Detector.kicad_pcb.lck`
- `~Ignition_Coil_Detector.kicad_pro.lck`
- `~Ignition_Coil_Detector.kicad_sch.lck`
- `Ignition_Coil_Detector.kicad_prl`

Lock files identify an active editing session. The `.kicad_prl` file stores local PCB-editor preferences. Neither is required to reproduce the design.
