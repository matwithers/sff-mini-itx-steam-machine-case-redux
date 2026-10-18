# SFF Mini-ITX Steam Machine Case Redux

A fully parametric FreeCAD remix of the  
**SFF Mini ITX Steam Machine Case v2 Airflow** by **3DCatt (@josedelamora)**.

This repository contains editable FreeCAD source files, development versions,
printable exports, and an assembly model for a redesigned version of the
original case.

## Original design

The original model was created by **3DCatt**:

**SFF Mini ITX Steam Machine Case v2 Airflow**

https://www.printables.com/model/1766227-sff-mini-itx-steam-machine-case-v2-airflow

The original design is licensed under:

**Creative Commons Attribution-NonCommercial 4.0 International  
(CC BY-NC 4.0)**

https://creativecommons.org/licenses/by-nc/4.0/

This project is an independent remix and is not affiliated with or endorsed by
the original designer.

Many thanks to 3DCatt for making the original design available to the community.

## Why this repository exists

The original design is supplied as STL files.

This project began by importing those STL files into FreeCAD, converting them
to solids, and applying additional Part Design features.

That approach worked, but the resulting models were large, slow to recompute,
and difficult to maintain because the geometry retained the complexity of the
original triangulated meshes.

The case has now been rebuilt from scratch as native parametric FreeCAD
geometry.

The original STL files remain useful as dimensional and visual references, but
the editable case models no longer depend on imported STL geometry.

This provides:

- much smaller FreeCAD source files
- substantially faster recompute times
- cleaner and more readable feature trees
- reusable spreadsheet-driven dimensions
- easier modification of hardware clearances
- configurable design variants
- more robust long-term maintenance
- easier fit checking using the FreeCAD assembly model

Once the redesign reaches a suitable state, the finished parts will also be
published on Printables as a remix of the original model.

## Current version

**v0.7.0 — SATA drive mount and assembly**

Completed:

- Rebuilt all case parts from scratch as native parametric FreeCAD models
- Removed dependency on imported STL-derived solids
- M3 heat-set insert conversion
- M3 clearance-hole conversion
- Front and rear fan screw clearance-hole conversion
- Configurable 120 mm / 140 mm front fan support
- Integrated LED lightbar aperture and diffuser channel
- Separate parametric LED holder
- LED holder M3 mounting system
- Optional Steam Controller puck cutout
- Standard and Steam Controller front-shell variants merged into one model
- LED holder heat-set insert direction revised for improved retention
- Power-button nut recess enlarged for greater thread engagement
- Magnet-holder access holes added to aid magnet removal
- Improved rear GPU mounting using an M3 heat-set insert
- Parametric 2.5-inch SATA drive mount
- Corresponding drive-mount fixing holes added to the case
- FreeCAD assembly file added for fit and clearance checking
- Updated printable STL exports generated from the rebuilt models

Next:

- Optional three-panel cover variant for easier printing

## Goals

The current goals of this remix are:

### 1. Native FreeCAD source models

**Status: Complete**

All case parts have now been rebuilt from scratch using native FreeCAD
geometry.

The editable models use features such as:

- Part Design Bodies
- parametric sketches
- Pads
- Pockets
- Hole features
- Fillets
- Linear Patterns and MultiTransforms
- spreadsheet-driven expressions
- configurable feature suppression

Imported STL solids are no longer used as the working geometry for the case
parts.

This removes the large number of triangulated faces inherited from converted
STL meshes and makes the source files significantly easier to edit and
maintain.

As an example, the earlier STL-derived front-shell FreeCAD file was
approximately **12 MB**, while the rebuilt native version was approximately
**477 KB**.

### 2. Heat-set inserts

**Status: Complete**

The original printed/self-tapping screw arrangement has been converted to use
M3 heat-set threaded inserts where appropriate.

The corresponding mating holes have also been enlarged to proper M3 clearance
holes.

Current standard dimensions used in the FreeCAD source are:

- M3 heat-set insert bore: **4.7 mm**
- M3 heat-set insert depth: **4.3 mm**
- M3 clearance hole: **3.4 mm**

These values are stored as FreeCAD spreadsheet parameters so they can be
adjusted consistently across the modified parts if required.

### 3. Fan mounting and screw clearance

**Status: Complete**

The fan mounting holes have been designed so that standard PC fan screws pass
freely through the printed case parts.

The screws are intended to bite into the plastic fan frame rather than cutting
threads into the case itself.

The fan screws used for sizing measured approximately **4.9 mm** across the
thread, and the case clearance holes have been set to:

- Fan screw clearance hole: **5.2 mm**

This value is stored as a reusable FreeCAD spreadsheet parameter.

The front shell includes configurable geometry for both **120 mm** and
**140 mm** fans.

A single `Fan_Size` spreadsheet parameter controls suppression of the
appropriate fan aperture and screw-hole features.

For example:

- `Fan_Size = 120` enables the 120 mm fan geometry
- `Fan_Size = 140` enables the 140 mm fan geometry

The 140 mm fan retains the CPU / motherboard-side bias of the original design.

Its vertical position has been adjusted slightly to provide improved clearance
around the LED holder.

### 4. LED lightbar

**Status: Complete**

The front shell includes an integrated LED lightbar system while preserving
the overall external appearance of the original case.

The lightbar design includes:

- a front-facing LED aperture
- a recessed diffuser channel
- rear clearance for the LED module components
- a separate removable LED holder
- M3 heat-set insert mounting for the holder
- recessed mounting screws in the front shell
- wiring clearance for the LED modules

The LED holder is designed around three discrete LED modules.

Current key dimensions include:

- LED module length: **54 mm**
- LED module count: **3**
- LED aperture length: **165 mm**
- LED aperture height: **5.5 mm**
- Diffuser channel height: **9.0 mm**
- LED holder depth: **5.0 mm**
- LED holder side overlap: **5.0 mm**
- LED holder top overlap: **2.0 mm**
- LED holder bottom overlap: **12.0 mm**

The LED holder mounting holes and the corresponding front-shell holes are
derived from the same LED aperture geometry, keeping both parts aligned
parametrically.

The heat-set inserts in the LED holder are installed from the rear so that
screw loading tends to pull them further into the printed part rather than out
of it.

### 5. Steam Controller puck support

**Status: Complete**

The Steam Controller puck front-shell variant has been incorporated into the
main front-shell FreeCAD model.

The puck opening was rebuilt as clean native FreeCAD sketch geometry rather
than retaining the heavily faceted STL-derived outline.

The puck opening is controlled using a spreadsheet-driven expression on the
Part Design feature's **Suppressed** property.

This allows both front-shell variants to be maintained in a single source
model and removes the need for a separate Steam Controller front-shell source
file.

### 6. Magnet holders

**Status: Complete**

The front-shell magnet holders have been rebuilt as native parametric FreeCAD
geometry.

The magnet bosses and recesses are driven by spreadsheet parameters.

The rounded upper edge of each holder is derived from the boss and magnet
diameters rather than being manually approximated.

Additional access holes have been added behind the magnet holders so magnets
can be pushed out more easily during assembly, maintenance, or replacement.

### 7. GPU rear mounting

**Status: Complete**

The rear GPU mounting arrangement has been improved to provide a conventional
and durable fixing point.

An M3 heat-set insert is used to provide a threaded mounting point for the GPU
bracket.

This replaces the less practical original retention arrangement and makes the
GPU easier to install and remove securely.

### 8. 2.5-inch drive mounting

**Status: Complete**

A dedicated parametric mount has been added for a standard 2.5-inch SATA SSD or
hard drive.

The mount is designed to provide a secure fixing point without significantly
compromising airflow or the compact internal layout of the case.

The drive cavity provides approximately **0.5 mm clearance per side** to allow
for print tolerance and small differences between drive enclosures while still
keeping the drive securely located.

Corresponding fixing holes have also been added to the case so the mount can be
installed as part of the complete assembly.

### 9. Optional three-panel cover

**Status: Complete**

An alternative version of the main cover is available as three separate
printable components:

- top panel
- left side panel
- right side panel

The original one-piece cover remains available.

The split version was created to make the cover easier and less risky to print.
The original single-piece cover takes approximately 24 hours to print, so the
three-piece version allows individual sections to be printed or replaced
without repeating the entire cover.

The panels are joined using M3 countersunk machine screws and heat-set inserts,
providing a rigid assembly while allowing the cover to remain removable and
serviceable.

## Current changes

The redesign currently includes:

- All case parts rebuilt as native parametric FreeCAD models
- Imported STL-derived working solids removed from the editable models
- Suitable screw locations converted to M3 heat-set inserts
- Mating holes enlarged to M3 clearance dimensions
- Fan mounting holes enlarged to provide fan-screw clearance
- Configurable 120 mm / 140 mm front fan support
- Integrated LED lightbar support
- Recessed diffuser and LED component-clearance geometry
- Separate parametric LED holder
- M3 heat-set mounting for the LED holder
- LED holder insert direction revised for improved mechanical retention
- Recessed front-shell screw mounting for the LED holder
- Power-button nut recess enlarged for improved thread engagement
- Steam Controller puck opening rebuilt as native FreeCAD geometry
- Standard and Steam Controller front-shell variants consolidated
- Magnet holders rebuilt as native parametric geometry
- Magnet-removal access holes added
- Rear GPU mounting improved using an M3 heat-set insert
- Parametric 2.5-inch SATA drive mount added
- Matching case fixing holes added for the drive mount
- FreeCAD assembly file added
- Reusable FreeCAD spreadsheet parameters added for hardware and case geometry
- Updated printable STL exports generated from the native models

Current development priority:

1. Optional three-panel cover variant

## Parametric configuration

The rebuilt models make extensive use of FreeCAD spreadsheets.

Common dimensions and configurable options are stored as parameters rather than
being duplicated throughout individual sketches and features.

Examples include:

- shell dimensions
- M3 clearance dimensions
- heat-set insert dimensions
- screwhead recess dimensions
- fan position
- fan size
- fan screw-hole spacing
- USB opening dimensions
- power-button geometry
- magnet geometry
- LED aperture geometry
- LED holder dimensions
- drive-mount dimensions
- fillet radii
- repeated feature spacing

Optional and mutually exclusive features can be controlled using expressions
on the Part Design **Suppressed** property.

This makes it possible to maintain several design variants from the same source
model without duplicating complete FreeCAD files.

## Repository layout

The repository will evolve as the redesign progresses, but will generally be
organised as:

```text
/
├── original/
│   └── Original/reference STL files
│
├── freecad/
│   ├── Native editable FreeCAD source files
│   └── Assembly file
│
├── stl/
│   └── Exported printable STL files
│
└── docs/
    └── Notes, dimensions, assembly information and development documentation
```

## FreeCAD workflow

The original STL files are retained as reference geometry for checking
dimensions and reproducing the intent of the original design.

The working models themselves are now native FreeCAD designs.

Typical modelling techniques used throughout the project include:

- stable datum planes and sketch attachment
- fully constrained sketches
- spreadsheet-driven dimensions
- Part Design Pads and Pockets
- Part Design Hole features for repeated hardware holes
- Sub-ShapeBinders where live cross-body geometry references are useful
- Linear Patterns and MultiTransforms for repeated geometry
- feature suppression for configurable variants
- native fillets and arcs instead of retaining STL facets
- shared parameters for matching geometry across separate parts

Where possible, geometry is constrained according to design intent rather than
arbitrary coordinates.

For example:

- corner hardware remains relative to shell edges
- centered features are tied to appropriate centerlines
- repeated hardware uses shared dimensions
- matching parts derive geometry from common parameters or references

This makes resizing and modifying the design substantially safer than editing
the original triangulated STL geometry.

## Hardware holes

FreeCAD's Part Design **Hole** feature is used where practical for conventional
hardware holes.

For example, an M3 recessed mounting hole can be represented as a single Hole
feature containing:

- M3 clearance diameter
- counterbore diameter
- counterbore depth
- through-hole depth

This replaces multiple separate Pocket features and makes repeated fastener
geometry easier to understand and modify.

## Front-shell configuration

The front-shell model incorporates several previously separate design options
within one parametric FreeCAD document.

Current configurable features include:

- 120 mm or 140 mm front fan geometry
- optional Steam Controller puck cutout
- LED lightbar geometry
- matching LED holder and mounting geometry

The LED lightbar and LED holder are maintained together so their shared
dimensions and mounting features remain aligned.

This reduces duplicated source files and keeps related front-shell changes
within one parametric model.

## Test parts and hardware fit

Small test pieces are used where practical to validate hardware dimensions
before committing to large prints.

These test pieces allow checks for:

- M3 screw clearance
- screwhead recess diameter and depth
- heat-set insert fit
- magnet fit
- power-button fit
- USB opening dimensions
- other press-fit and clearance-sensitive geometry

This makes it possible to tune spreadsheet parameters for the actual printer,
material and hardware without repeatedly printing a complete case part.

## Assembly

A separate FreeCAD assembly file is included in the project.

The individual printed parts remain maintained as separate FreeCAD source
files, while the assembly brings them together for:

- fit checking
- clearance checking
- component placement
- visualisation
- assembly planning
- bill-of-materials generation

Keeping the assembly separate allows individual part files to continue to be
edited independently while those changes can be reflected in the assembled
model.

The assembly is intended to become the main reference for checking interactions
between parts as the design evolves.

## Work in progress

This is currently a development project.

Parts may change dimensions, mounting arrangements or interfaces between
revisions.

Unless a release is specifically marked as complete, files should be
considered experimental.

Git is being used to retain the design history and make it easier to track the
many small changes involved in adapting and rebuilding the case.

## Licensing and attribution

The original design by **3DCatt** is licensed under the
**Creative Commons Attribution-NonCommercial 4.0 International License**.

This repository contains adaptations of that work.

Where geometry or designs are derived from the original model, the original
author's CC BY-NC 4.0 licence and attribution continue to apply.

Original work:

**SFF Mini ITX Steam Machine Case v2 Airflow**  
Copyright / design by **3DCatt (@josedelamora)**  
https://www.printables.com/model/1766227-sff-mini-itx-steam-machine-case-v2-airflow

Changes and additional design work in this repository are by the maintainer of
this repository.

See the `LICENSE` file for further information.

## Disclaimer

This is a hobby project involving custom PC hardware and 3D-printed structural
parts.

Check clearances, temperatures, wiring, screw lengths and component dimensions
for your own build before assembly.