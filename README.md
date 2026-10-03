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

Once the redesign reaches a suitable state, the finished parts will also be
published on Printables as a remix of the original model.

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

**Status: Planned**

Increase the front and rear fan mounting holes so that standard PC fan screws
pass freely through the printed case parts.

The screws should bite into the plastic fan frame rather than cutting threads
into the case itself.

The final clearance diameter will be based on the actual fan screws used in the
build.

### 3. LED light bar

**Status: Planned**

Add provision for an integrated LED light bar while keeping the external
appearance of the case clean.

The mounting system and electronics are still under development.

### 4. 2.5-inch drive mounting

**Status: Planned**

Add proper internal mounting for one or more 2.5-inch SATA SSDs / hard drives.

The aim is to add storage without significantly compromising airflow or the
compact layout of the original case.

### 5. GPU rear mounting

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
- Added reusable FreeCAD spreadsheet parameters for common hardware dimensions
- Retained editable FreeCAD source files for modified parts
- Exported updated printable geometry from the FreeCAD models

Current development priority:

1. Fan screw clearance
2. LED light bar
3. 2.5-inch drive mounting
4. GPU rear mounting

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
- Part Design pockets and other editable features

This makes the modified files easier to maintain than working directly with
successive STL edits.

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