# LTspice files

## Baseline schematic

`09_final_ignition_coil_detector.asc` is the unchanged simulation file supplied after the successful rerun on 18 July 2026.

## Missing local dependencies

The simulator log shows that the design loads:

```text
C:\Users\kinzangrd_l\Documents\LTspice\lm393.lib
```

The schematic also references a custom `LM2903B` symbol. For reproducibility, add the following files to this directory in a future commit:

- `models/lm393.lib`
- `symbols/LM2903B.asy`

Then update the symbol/model reference so it uses a repository-relative dependency rather than a user-specific Windows path.

Generated `.raw`, `.op.raw` and `.net` files are intentionally excluded from version control because they can be regenerated. One baseline log is retained under `results/`.

