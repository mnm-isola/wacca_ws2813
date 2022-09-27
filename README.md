# WACCA WS2813 LED PCB Replacement

---

# WARNING: WORK IN PROGRESS

---

##### wacca_ws2813_rev1

Working design comfirmed by myself.

I put 2 sticks in service since 10-Aug-2022, still going fine (last update: 27-Sep-2022), C9 not installed.

---

##### wacca_ws2813_rev20220814

"Improved" version of  ``wacca_ws2813_rev1`` which I did not order and verify if the design works (it should).

- Additional vent holes to help with cooling (Did not verify of they would cause light leaking into the diffusion parts)

- Unmasked copper platings under LEDs (May interfere with manufracturing, consult your PCB fab about this)

- SMD capacitor at C9 instead of a THT one

- Removed unused mounting hole

- 1mm shorter to help with tolerance and prevent potential PCB flex

---

## BOM (for use with WS2813E / WS2813B-V4 or below)

| Footprint | Parts                  | Size | Value  | LCSC    | Remark                                    |
| --------- | ---------------------- | ---- | ------ | ------- | ----------------------------------------- |
| C1-C8     | Decoupling Capacitors  | 0805 | 100nF  | C49678  |                                           |
| C9        | Electrolytic Capacitor | TBD  | 1000uF | TBD     | Optional. THT on rev1, SMD on rev20220814 |
| CN1,CN2   | JST XA 3 pin           |      |        | C265055 | B03B-XASK-1(LF)(SN)                       |
| CN3       | JST XA 4 pin           |      |        | C264994 | B04B-XASK-1(LF)(SN)                       |
| D1-D8     | Worldsemi WS2813E      |      |        | C160214 |                                           |
| R1,R2     |                        | 0805 | 100R   | C17408  |                                           |
| U1,U2     | MMBD1503A              |      |        | C242273 |                                           |

---

## BOM (for use with WS2813B-V5)

| Footprint | Parts                  | Size | Value  | LCSC    | Remark                                    |
| --------- | ---------------------- | ---- | ------ | ------- | ----------------------------------------- |
| C1-C8     |                        |      |        |         | WS2813B-V5 do not require decoupling caps |
| C9        | Electrolytic Capacitor | TBD  | 1000uF | TBD     | Optional. THT on rev1, SMD on rev20220814 |
| CN1,CN2   | JST XA 3 pin           |      |        | C265055 | B03B-XASK-1(LF)(SN)                       |
| CN3       | JST XA 4 pin           |      |        | C264994 | B04B-XASK-1(LF)(SN)                       |
| D1-D8     | Worldsemi WS2813B-V5   |      |        | C965558 |                                           |
| R1,R2     |                        | 0805 | 100R   | C17408  |                                           |
| U1,U2     | MMBD1503A              |      |        | C242273 |                                           |

## Manufracturing warnings

[Datasheet of WS2813](https://pdf1.alldatasheet.com/datasheet-pdf/view/1134580/WORLDSEMI/WS2813.html)

According to page 7: These LEDs are moisture sensitive, they need to be baked and dried before SMT assembly. Not all PCB fabs have this procedure  (eg JLCPCB's economic option), **be sure to consult and notify the fab of your choice before mass producing the PCBs, otherwise you may end up with extremely high failure rate**. (I learnt it the hard way so you don't have to.)

PCB thickness: 1.6mm

Color: White

---

##### What about a WS2812 clone?

I don't feel like spending time on a inferior design so no.
