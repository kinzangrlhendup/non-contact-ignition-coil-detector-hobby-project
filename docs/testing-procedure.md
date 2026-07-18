# Prototype testing procedure

This procedure is provisional and must be updated after the native KiCad files and actual component datasheets are reviewed.

## 1. Unpowered inspection

1. Inspect solder joints, tracks and component orientation under magnification.
2. Verify that the 9 V and 5 V rails are not shorted to ground.
3. Check continuity through the TEST button and reverse-polarity diode.
4. Check that the PCB pickup is connected to J2/TP1 and isolated from ground.

## 2. Current-limited power-up

1. Use a current-limited bench supply set initially to 9 V and approximately 50 mA.
2. Hold the TEST button and check for abnormal current or heating.
3. Measure the regulated rail; target approximately 5 V.
4. Release the button and verify that the circuit powers down.

## 3. Controlled signal-injection test

1. Keep the board away from an engine ignition system.
2. Couple a low-voltage pulse generator through a small test capacitor or an insulated nearby wire; do not directly apply high voltage.
3. Start with a low pulse amplitude and adjust the sensitivity control.
4. Confirm the voltage at TP1, the `ENVELOPE` waveform, comparator switching, LED operation and buzzer operation.
5. Record the minimum repeatable coupled signal that produces detection.

## 4. Bench ignition-coil proximity test

Only perform this with a safely controlled ignition-coil test arrangement, insulated fixtures and appropriate high-voltage precautions. Do not touch the coil, secondary terminal, spark lead or detector during firing.

1. Begin at the lowest sensitivity and a relatively large separation.
2. Move the detector closer gradually while maintaining insulation.
3. Record coil type, distance, orientation, supply voltage and firing frequency.
4. Repeat with several known-good coils to establish a normal response range.

## 5. Vehicle test

1. Place the assembled detector in an insulated enclosure.
2. Secure loose clothing, cables and the tester away from hot and moving parts.
3. Hold the TEST button and bring the marked pickup region near one coil-on-plug unit.
4. Adjust sensitivity until firing is detected without responding excessively to adjacent coils.
5. Compare cylinders under identical placement and engine conditions.

## Interpretation limitation

A beep confirms that the instrument detected a nearby transient. It does not by itself establish secondary-voltage magnitude, spark duration, available spark energy or performance under cylinder pressure. A coil that triggers the detector may still be defective, and a non-trigger may result from distance, orientation, shielding or threshold setting.

