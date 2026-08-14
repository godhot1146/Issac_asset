# Stir-fry booth V2 layout basis

The approved visual reference is `볶음 수정도면.png` received on 2026-08-14.

## Selected table

Use three instances of `stirfry_stage_300x1150.urdf`.

- measured STEP size: 0.300 x 1.150 x 0.900 m
- bowl count per table: 4
- nominal bowl diameter: 0.250 m
- slot pitch: 0.250 m
- table-local slot coordinates: `(0, -0.375)`, `(0, -0.125)`, `(0, 0.125)`, `(0, 0.375)` m

The supplied STEP currently contains no circular cut-outs (zero circular
edges); it is the table/frame geometry only. When the four holes are modelled,
preserve the table origin, 0.300 x 1.150 m footprint and the slot coordinates
above so the scene and controller transforms do not need to change.

The other STEP variants measure 0.300 x 0.590 x 1.200 m and
0.300 x 0.870 x 1.200 m. Their 1.2 m working height and shorter row length do
not preserve the same four-slot geometry.

## Robot-centred placement

Use the A0509 base centre as world `(0, 0)` and the open/Bonitkit side as `+X`.

| Actor | XY centre (m) | Yaw |
|---|---:|---:|
| robot cabinet | `(-0.150, 0.000)` | 0 deg |
| A0509 base | `(0.000, 0.000)` | 0 deg |
| west table | `(-0.650, 0.000)` | 0 deg |
| north table | `(0.000, 0.650)` | +90 deg |
| south table | `(0.000, -0.650)` | -90 deg |
| Bonitkit | `(1.9885, 0.000)` | 0 deg |

The 150 mm cabinet offset places the robot toward Bonitkit while leaving 50 mm
between the cabinet and each table. The Bonitkit position assumes its measured
X width is 0.827 m and provides a 1.000 m passage from the east ends of the
north/south tables to the nearest Bonitkit face.

## Bowl centres

For slot coordinate `s in (-0.375, -0.125, 0.125, 0.375)` m:

- west: `(-0.650, s)`
- north: `(-s, 0.650)`
- south: `(s, -0.650)`

Corresponding slots have identical robot-centred radii on all three faces:

- outer slots: 0.7500 m
- inner slots: 0.6619 m

If the redesigned tabletop retains the previous bowl seating depth of 27.5 mm,
the bowl actor base is `z=0.8725 m` for this 0.900 m table.

## Booth footprint and plate decision

With the 1 m passage, the calculated overall footprint is approximately
3.202 x 1.600 m. The supplied `stirfry_plate_1500x2100` is only 1.500 x 2.100 m,
so it cannot cover the full booth in either orientation. Keep its converted
asset for reference but do not spawn it in the V2 scene.
