# LTspice files

## Baseline schematic

`09_final_ignition_coil_detector.asc` is the unchanged simulation file supplied after the successful rerun on 18 July 2026.

## Comparator dependencies

The following dependency files are included beside the schematic:

```text
LM2903B.asy
lm393.lib
```

The symbol contains:

```text
SYMATTR Value LM2903B
SYMATTR ModelFile lm393.lib
```

Its Spice pin order is `IN+`, `IN-`, `Vcc`, `GND`, `OUT`, matching the model declaration:

```text
.SUBCKT LM2903B IN+ IN- Vcc GND OUT
```

Keeping the symbol, model and `.asc` file together preserves the existing relative reference and avoids the original user-specific Windows dependency path.

The model identifies itself as Texas Instruments LM2903B PSpice model version 1.0, dated 30 September 2021. Retain its complete copyright and disclaimer header. Review [third-party notices](../THIRD_PARTY_NOTICES.md) before changing repository visibility or redistributing the model.

Generated `.raw`, `.op.raw` and `.net` files are intentionally excluded from version control because they can be regenerated. One baseline log is retained under `results/`.

