# CPU Project Hardware Parts List

This bill of materials covers the components required to build and test the transistor-level logic circuits for the CPU project, including the working full-adder prototype.

> **Pricing note:** Prices are approximate and may change. The total below does not include sales tax, shipping, or tools such as wire cutters and wire strippers.

## Bill of Materials

| Component | Selected Product | Quantity | Purpose | Estimated Price |
|---|---|---:|---|---:|
| Solderless breadboards | [BOJACK 3-Value Breadboard Kit](https://www.amazon.com/BOJACK-Values-Solderless-Breadboard-Flexible/dp/B08Y59P6D1) | 1 kit | Provides two 830-point and two 400-point breadboards for assembling the circuit | $9.99 |
| Solid-core hookup wire | [TUOFENG 22 AWG Solid Wire Kit](https://www.amazon.com/dp/B07TX6BX47?th=1) | 1 kit | Custom-length breadboard wiring; six colors simplify organization and debugging | $15.99 |
| NPN transistors | [BOJACK 2N3904 NPN Transistors, 200 Pack](https://www.amazon.com/BOJACK-2N3904-General-Purpose-Transistors/dp/B07T4ZJ76B) | 3 pack | Implements transistor-level RTL logic gates and the full-adder circuit | $9.99 |
| Resistors | [BOJACK 1,000-Piece Resistor Assortment](https://www.amazon.com/BOJACK-Values-Resistor-Resistors-Assortment/dp/B08FHPKF9V) | 1 kit | Includes 10 kΩ, 4.7 kΩ, and 470 Ω values for transistor biasing, pull-ups, and LED current limiting | $9.99 |
| LEDs | [DiCUNO 450-Piece 5 mm LED Assortment](https://www.amazon.com/DiCUNO-450pcs-Colors-Emitting-Assorted/dp/B073QMYKDM) | 1 kit | Red and blue LEDs indicate logic inputs and outputs | $11.99 |
| Three-pin switches | [EGSCST 110-Piece SPDT Slide Switch Kit](https://www.amazon.com/EGSCST-Switches-Position-Miniature-Vertical/dp/B0FNK8B1YV) | 1 kit | Supplies selectable logic-high and logic-low inputs for A, B, and carry-in | $9.99 |
| Power supply | [Blomiky 4.8 V NiMH Rechargeable Battery and Charger](https://www.amazon.com/Blomiky-2200mAH-Rechargeable-Battery-Charger/dp/B07FXVHT32) | 1 | Provides a portable 4.8 V supply close to the 5 V design voltage | $15.99 |

## Estimated Cost

| Category | Cost |
|---|---:|
| Breadboards and wiring | $25.98 |
| Transistors and resistors | $19.98 |
| LEDs and switches | $21.98 |
| Battery and charger | $15.99 |
| **Estimated component total** | **$83.93** |

A project budget of approximately **$90 before tax and shipping** is recommended to allow for price changes and a possible battery-connector adapter.

## Component Notes

- The resistor assortment contains **470 Ω** rather than exactly 450 Ω. A 470 Ω resistor is an appropriate substitute for LED current limiting in this project.
- Loose DuPont connector pins are not included because the 22 AWG solid-core wire can be cut, stripped, and inserted directly into the breadboards.
- The battery uses an **SM-2P connector**. A matching pigtail or adapter may be required to connect it to the breadboard power rails.
- Before constructing the full circuit, verify the **collector, base, and emitter pin order** of the purchased 2N3904 transistors.
