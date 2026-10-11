# NAND-side component inventory

**Status: unverified.** Reference photos are original photographs, not AI-generated pad maps. Do not use generated annotations for solder placement.

![Unused NAND sites](../images/pcb-empty-footprints.jpg)

![Populated NAND support components](../images/nand-support-components.jpg)

## Recording template

Number only **verified separate two-terminal footprints** adjacent to each NAND site, not NAND BGA pads, vias, test pads, or individual rectangular lands that may be part of the NAND footprint.

| ID | NAND site | Position / photo reference | Component type | Measured value | Size | Voltage rating (if known) | Confidence / notes |
| --- | --- | --- | --- | --- | --- | --- | --- |
| P01 | TBD | TBD | TBD | TBD | TBD | TBD | Not verified |
| P02 | TBD | TBD | TBD | TBD | TBD | TBD | Not verified |
| P03 | TBD | TBD | TBD | TBD | TBD | TBD | Not verified |

## Measurement guidance

- Record each component's exact position **before** removing it.
- In-circuit capacitance measurements may include parallel components and other circuitry.
- Out-of-circuit measurements with an appropriate LCR meter are more trustworthy for tiny MLCCs.
- An identical-looking part is not proof of identical capacitance, tolerance, or voltage rating.
- Do not assume every unpopulated position should be fitted.
- Before energizing a modified board, check power rails for shorts and inspect all solder joints.
