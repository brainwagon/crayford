# Crayford Focuser for Telescopes

STEP files for a Crayford-style telescope focuser, based on the excellent original
design by **aeberbach**:

> [1.25" Crayford Focuser for Telescopes](https://www.printables.com/model/125438-125-crayford-focuser-for-telescopes)
> by aeberbach on Printables.com

All credit for the original design goes to aeberbach. **For the draw tube design,
full assembly instructions, and bill of materials for the complete focuser, consult
the [original Printables page](https://www.printables.com/model/125438-125-crayford-focuser-for-telescopes).**
The parts here are my modifications, made mostly to simplify assembly and improve
reliability.

## Bill of Materials

Hardware required beyond the 3D printed parts:

| Item | Qty | Notes |
|------|-----|-------|
| M3 heat-set inserts | 6 | 4 for the front cap; 2 for the knobs (or substitute M3 set screws) |
| M3×10 socket head screws | 4 | Serve as bearing axles — thread directly into the base |
| 3×8×3mm bearings | 4 | |
| 10mm × 3mm aluminum bar, 64mm long | 3 | Cut to length from flat bar stock |
| 10mm × 3mm aluminum bar, 37mm long | 1 | Mounts to front cap |

## Parts

### Focuser Base
![Focuser Base](images/focuser_base.svg)

Main focuser body/base — `focuser_base.step`

**Changes from original:**

The original design uses nylon locknuts to retain the bearing axles, which creates
thin-walled geometry around the locknut voids that is fragile and prone to breaking
during assembly. In this version, M3×10 bolts serve directly as the axles, threading
cleanly into the holes without any additional hardware. Friction alone is sufficient
to keep them in place — there is no meaningful force trying to back them out during
normal use. Eliminating the locknut voids allows that section of the print to be
made thicker and more solid, improving both strength and printability.

The front face (where the front cap attaches) has also been modified to accept
M3 heat-set inserts rather than threading directly into plastic, giving the
cap-to-base joint a more durable and repeatable connection.

---

### Front Cap
![Front Cap](images/front_cap.svg)

Front cap for the focuser tube — `front_cap.step`

**Changes from original:**

The countersink holes use the ["Prusa trick"](https://blog.prusa3d.com/print-countersunk-screws-without-supports_52782/)
— the countersink is modeled as a polygon (rather than a cone) so it bridges cleanly
without supports. The part is oriented with its visible face flat against the build
plate, which produces a smooth finished surface for mounting the 37mm × 10mm × 3mm
plate.

---

### Pinion Block
![Pinion Block](images/pinion_block.svg)

Pinion block assembly — `pinion_block.step`

**Changes from original:**

The spring recesses have been enlarged to give more clearance for the springs that
press the 5mm drive rod against the aluminum strip on the draw tube. The corners
of the block have been slightly rounded, which reduces the sharp overhangs and
makes the part a little easier to print cleanly.

---

### Simple Knob
![Simple Knob](images/simple_knob.svg)

Focus knob — `simple_knob.step`

**New design** (not derived from original):

The original knobs fit too tightly on the 5mm drive shaft to be practical, so this
is a clean replacement design. The bore is sized correctly for a 5mm shaft, and the
knob incorporates a recess for an M3 heat-set insert. Once installed, the insert
accepts either an M3 set screw or an M3×6 socket head screw to lock the knob to
the shaft.

---

## License

This work is licensed under the
[Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-nc-sa/4.0/),
consistent with the original design's license. See [LICENSE](LICENSE) for details.
