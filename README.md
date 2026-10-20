# N64 → N64 L-Shaped Extension Adapter v1.1

This is an extension board designed to be inserted into the N64 slot of an existing "N64-to-Aleck64 conversion adapter," allowing an **N64 cartridge to be positioned upright** (parallel to the adapter board).

```
[N64 Cartridge]  ← Stands upright.
``` The label should face toward the front (opposite the adapter board).
│
┌────┴────┐  ← This board (horizontal)
│ L-shaped riser │
└──┬──────┘
│ Card edge
┌──┴───────┐
│ N64 to Aleck64 adapter (vertical) │
└──────────┘
```

## PCB Specifications
- Dimensions: 84 × 52 mm, **thickness: 1.2 mm**, 2-layer
- Bottom edge: N64 card edge (2.5 mm pitch, 25×2, gold fingers)
- Top side: N64 cartridge slot (2.5 mm pitch, 50-pin)
- Wiring: 1:1 straight-through for all 50 pins

## PCBWay Ordering Settings
| Item | Setting |
|---|---|
| Upload | `N64_to_N64_L_riser_v1_gerber.zip` |
| Layers | 2 |
| **Board Thickness** | **1.2 mm** |
| **Gold Fingers** | **Yes** + **Beveling (45°)** |
| Surface Finish | ENIG (recommended) |
| Min. Trace/Spacing | 0.2 / 0.2 mm, min. hole size 0.3 mm |

## Components
- **50-pin N64 cartridge slot** (a 2.5 mm pitch component, typically sold for console repair—search for "N64 50 pin cartridge slot connector" on sites like eBay, AliExpress, or Hexir).
- Mounting holes: φ0.9 mm (slightly larger than the φ0.85 mm holes on the original adapter, to account for potential fitment issues).

## Assembly and Usage
1. The slot should be soldered onto the board... Place the main unit on the side marked "THIS SIDE / THIS SIDE FACES UP" (Side B—the side that should face upward during use), and solder the pins from the opposite side (Side F). The square pad corresponds to pin 1.
- This side is the same side as the "pins 1–25" area on the card edge at the bottom. If you attach it to the Side F side, the cartridge will end up facing downward (toward the adapter board) and will not fit. 
- Note that the connector component itself has no inherent orientation (polarity); as long as it is attached to the correct side, the wiring will be connected properly.
2. Insert this board into the N64 slot of the N64-to-Aleck64 adapter. Ensure that the "THIS SIDE UP" silkscreen on the back (Side B) is facing upward. Inserting it the wrong way will reverse the wiring, so please double-check (the card edge has no key/notch).
3. Insert the N64 cartridge from above, ensuring that its label faces the side opposite the card edge (following the direction indicated by the silkscreen arrow labeled "CART LABEL FACES THIS WAY").

## Notes
- This board is supported only at the point of insertion into the original adapter's slot. Since the center of gravity shifts upward when a cartridge is inserted, it is recommended to provide some form of support (such as a spacer or mounting fixture). You can utilize the two φ3.2 mm holes located at the top.
- Because the cartridge stands upright, you will need over 10 cm of clearance above the unit.
- This is a new, unverified design. Please produce a prototype first to confirm that it fits into the slot and that the cartridge is correctly recognized. ## Verification
- KiCad DRC: 0 errors / 0 unrouted nets
- Generated Gerber files were converted to images, and electrical continuity was independently re-verified: all 50 pins (across 33 nets) match 1:1 (PASS).
- Confirmed that the check results in a FAIL when using a mapping table with the left and right sides swapped (verifying that pin orientation is correctly accounted for).

## License
CC BY-SA 4.0 / No warranty. Pinout information is based on the N64 connector table from the ConsoleMods Wiki and the N64-to-Aleck64 adapter (r001) design from arcade-projects.com.
