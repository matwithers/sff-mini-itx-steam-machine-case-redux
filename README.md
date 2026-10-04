# SFF Mini-ITX Steam Machine Case Redux

A modified and more easily editable version of the  
**SFF Mini ITX Steam Machine Case v2 Airflow** by **3DCatt (@josedelamora)**.

This repository contains my FreeCAD source files, development versions, and
printable exports while I work on a remix of the original case.

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

This repository is primarily my working source tree for modifications to the
case, with editable FreeCAD files retained alongside exported printable files.

The aim is to progressively replace one-off STL editing with cleaner,
parameter-driven FreeCAD features where practical.

Once the redesign reaches a suitable state, the finished parts will also be
published on Printables as a remix of the original model.

## Current version

**v0.4.0 — LED lightbar and unified front shell**

Completed:

- M3 heat-set insert conversion
- M3 clearance-hole conversion
- Front and rear fan screw clearance-hole conversion
- Integrated LED lightbar aperture and diffuser channel
- Separate parametric LED holder
- LED holder M3 mounting system
- Optional Steam Controller puck cutout
- Standard and Steam Controller front-shell variants merged into one model

Next:

- 2.5-inch drive mounting
- Improved rear GPU mounting

## Goals

The current goals of this remix are:

### 1. Heat-set inserts

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

### 2. Fan screw clearance

**Status: Complete**

The front and rear fan mounting holes have been enlarged so that standard PC
fan screws pass freely through the printed case parts.

The screws are intended to bite into the plastic fan frame rather than cutting
threads into the case itself.

The fan screws used for sizing measured approximately **4.9 mm** across the
thread, and the case clearance holes have been set to:

- Fan screw clearance hole: **5.2 mm**

This value is also stored as a FreeCAD spreadsheet parameter.

### 3. LED lightbar

**Status: Complete**

The front shell now includes an integrated LED lightbar system while preserving
the overall external appearance of the original case.

The lightbar design includes:

- a front-facing LED aperture
- a recessed diffuser channel
- rear clearance for the LED module components
- a separate removable LED holder
- M3 heat-set insert mounting for the holder
- recessed mounting screws in the front shell

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

### 4. Steam Controller puck support

**Status: Complete**

The Steam Controller puck front-shell variant has been merged into the main
front-shell FreeCAD model.

The puck opening was rebuilt as clean native FreeCAD sketch geometry rather
than retaining the heavily faceted STL-derived outline.

The puck opening can be enabled or disabled using the FreeCAD feature's
**Suppressed** property, allowing both front-shell variants to be maintained in
a single source model.

This removes the need to maintain a separate duplicate Steam Controller
front-shell file.

### 5. 2.5-inch drive mounting

**Status: Planned**

Add proper internal mounting for one or more 2.5-inch SATA SSDs / hard drives.

The aim is to add storage without significantly compromising airflow or the
compact layout of the original case.

### 6. GPU rear mounting

**Status: Planned**

Improve the rear GPU mounting arrangement.

The current design does not appear to provide a practical way to secure the GPU
bracket with a conventional retaining screw.

The aim is to add a more conventional and accessible GPU fixing point while
retaining compatibility with the compact case layout.

## Current changes

So far, the following modifications have been completed:

- Converted suitable screw locations to M3 heat-set inserts
- Enlarged mating holes to M3 clearance dimensions
- Enlarged front and rear fan mounting holes to provide fan-screw clearance
- Added integrated LED lightbar support to the front shell
- Added recessed diffuser and LED component clearance geometry
- Added a separate parametric LED holder
- Added M3 heat-set mounting for the LED holder
- Added recessed front-shell screw mounting for the LED holder
- Rebuilt the Steam Controller puck opening using clean native FreeCAD geometry
- Merged standard and Steam Controller front-shell variants into one model
- Added reusable FreeCAD spreadsheet parameters for common hardware and LED dimensions
- Retained editable FreeCAD source files for modified parts
- Exported updated printable geometry from the FreeCAD models

Current development priority:

1. 2.5-inch drive mounting
2. GPU rear mounting

## Repository layout

The repository will evolve as the redesign progresses, but will generally be
organised as:

```text
/
├── original/
│   └── Original/reference STL files
│
├── freecad/
│   └── Editable FreeCAD source files
│
├── stl/
│   └── Exported printable STL files
│
└── docs/
    └── Notes, dimensions, assembly information and development documentation
```

## FreeCAD workflow

The original STL files are imported into FreeCAD and converted to usable solid
geometry before modification.

Where practical, modified parts use:

- refined imported solids as Part Design base features
- parametric sketches
- spreadsheet-driven dimensions
- Part Design pads and pockets
- reusable shared dimensions for matching features across multiple parts
- optional features using FreeCAD suppression where useful

This makes the modified files easier to maintain than working directly with
successive STL edits.

Some source geometry remains derived from complex STL meshes, so recomputing
large models may be slower than with a fully native FreeCAD design.

## Front-shell configuration

The main front-shell model now incorporates multiple previously separate design
options.

The Steam Controller puck cutout can be enabled or disabled using the
**Suppressed** property on its Part Design feature.

The LED lightbar geometry and LED holder are maintained in the same FreeCAD
document so their shared dimensions and mounting geometry remain aligned.

This reduces duplicated source files and keeps related front-shell changes in
one parametric model.

## Work in progress

This is currently a development project.

Parts may change dimensions, mounting arrangements or interfaces between
revisions. Unless a release is specifically marked as complete, files should be
considered experimental.

Git is being used to retain the design history and make it easier to track the
many small changes involved in adapting the case.

## Licensing and attribution

The original design by **3DCatt** is licensed under the
**Creative Commons Attribution-NonCommercial 4.0 International License**.

This repository contains adaptations of that work.

Where files are derived from the original model, the original author's
CC BY-NC 4.0 licence and attribution continue to apply.

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