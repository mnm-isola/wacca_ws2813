# WACCA WS2813 LED PCB Replacement

---

# WARNING: WORK IN PROGRESS

---

##### wacca_ws2813_rev1

Working design comfirmed by myself.

---

##### wacca_ws2813_rev20220814

"Improved" version of  ``wacca_ws2813_rev1`` which I did not order and verify if the design works (it should).

- Additional vent holes to help with cooling (Did not verify of they would cause light leaking into the diffusion parts)

- Unmasked copper platings under LEDs (May interfere with manufracturing, consult your PCB fab about this)

- SMD capacitor at C9 instead of a THT one

- Removed unused mounting hole

- 1mm shorter to help with tolerance and prevent potential PCB flex

---

## BOM

| Footprint               | Size   | Value  | Parts                       |
| ----------------------- | ------ | ------ | --------------------------- |
| C1,C2,C3,C4,C5,C6,C7,C8 | 0805   | 100nF  |                             |
| C9                      | ////// | 1000uF |                             |
| CN1,CN2                 |        |        | JST XA 3p                   |
| CN3                     |        |        | JST XA 4p                   |
| D1,D2,D3,D4,D5,D6,D7,D8 |        |        | Worldsemi WS2813B / WS2813E |
| R1,R2                   | 0805   | 100R   |                             |
| U1,U2                   |        |        | MMBD1503A                   |

---

## Manufracturing warnings

[Datasheet of WS2813](https://pdf1.alldatasheet.com/datasheet-pdf/view/1134580/WORLDSEMI/WS2813.html)

According to page 7: These LEDs are moisture sensitive, they need to be baked and dried before SMT assembly. Not all PCB fabs have this procedure  (eg JLCPCB's economic option), **be sure to consult and notify the fab of your choice before mass producing the PCBs, otherwise you may end up with extremely high failure rate**. (I learnt it the hard way so you don't have to.)



PCB thickness: 1.6mm

Color: White

---

##### What about a WS2812 clone?

I don't feel like spending time on a inferior design so no.
