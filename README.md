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

The project initially used refined STL-derived solids as the basis for further
Part Design work. As the redesign has progressed, key parts are being rebuilt
as clean native FreeCAD geometry instead.

This makes the models smaller, easier to edit, faster to recompute, and less
dependent on complex imported mesh topology.

Once the redesign reaches a suitable state, the finished parts will also be
published on Printables as a remix of the original model.

## Current version

**v0.5.0 — Native FreeCAD front-shell rebuild**

Completed:

- M3 heat-set insert conversion
- M3 clearance-hole conversion
- Front and rear fan screw clearance-hole conversion
- Integrated LED lightbar aperture and diffuser channel
- Separate parametric LED holder
- LED holder M3 mounting system
- Optional Steam Controller puck cutout
- Configurable 120 mm / 140 mm front fan support
- Standard and Steam Controller front-shell variants merged into one model
- LED holder heat-set insert direction revised for improved retention
- Power-button nut recess enlarged for greater thread engagement
- Front shell completely rebuilt as native parametric FreeCAD geometry
- Access holes added behind magnet holders to aid magnet removal

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

### 2. Fan mounting and screw clearance

**Status: Complete**

The front and rear fan mounting holes have been enlarged so that standard PC
fan screws pass freely through the printed case parts.

The screws are intended to bite into the plastic fan frame rather than cutting
threads into the case itself.

The fan screws used for sizing measured approximately **4.9 mm** across the
thread, and the case clearance holes have been set to:

- Fan screw clearance hole: **5.2 mm**

This value is stored as a FreeCAD spreadsheet parameter.

The rebuilt front shell also includes separate configurable geometry for
**120 mm** and **140 mm** fan installations.

A single `Fan_Size` spreadsheet parameter controls suppression of the relevant
fan aperture and screw-hole features, allowing the model to switch cleanly
between the two fan sizes.

The 140 mm fan remains offset toward the CPU / motherboard side, broadly
preserving the airflow bias of the original design.

The fan position has also been raised slightly in the rebuilt model to improve
clearance around the LED holder.

### 3. LED lightbar

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
screw loading tends to pull the inserts further into the printed part rather
than out of it.

### 4. Steam Controller puck support

**Status: Complete**

The Steam Controller puck front-shell variant has been merged into the main
front-shell FreeCAD model.

The puck opening was rebuilt as clean native FreeCAD sketch geometry rather
than retaining the heavily faceted STL-derived outline.

The puck opening is controlled by a spreadsheet-driven feature switch using the
Part Design feature's **Suppressed** property.

This allows both front-shell variants to be maintained in a single source model
and removes the need for a separate duplicate Steam Controller front-shell
file.

### 5. Native FreeCAD front shell

**Status: Complete**

The front shell has been completely rebuilt as native parametric FreeCAD
geometry.

The previous front-shell model was based on an imported STL converted into a
solid and then modified using Part Design features.

The rebuilt model now uses native:

- sketches
- pads
- pockets
- Hole features
- fillets
- spreadsheet-driven dimensions
- configurable suppressed features
- shared hardware parameters

No imported STL geometry is required for the rebuilt front shell.

This reduced the FreeCAD source file size from approximately **12 MB** to around
**477 KB**.

The native rebuild also substantially improves:

- recompute speed
- editability
- clarity of the feature tree
- parameter reuse
- resilience when changing dimensions
- maintainability of future variants

Repeated hardware features are now represented more directly where practical.
For example, recessed M3 mounting holes use FreeCAD's Part Design **Hole**
feature rather than separate through-hole and counterbore Pocket operations.

### 6. Magnet holders

**Status: Complete**

The front-shell magnet holders have been rebuilt as native FreeCAD geometry.

The magnet bosses and recesses are parameter-driven, and the rounded upper edge
of each holder is generated from the boss and magnet diameters.

Additional access holes have been added behind the magnet holders to make
magnet removal easier during assembly, maintenance, or future replacement.

### 7. 2.5-inch drive mounting

**Status: Planned**

Add proper internal mounting for one or more 2.5-inch SATA SSDs / hard drives.

The aim is to add storage without significantly compromising airflow or the
compact layout of the original case.

### 8. GPU rear mounting

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
- Added configurable 120 mm / 140 mm front fan support
- Added integrated LED lightbar support to the front shell
- Added recessed diffuser and LED component clearance geometry
- Added a separate parametric LED holder
- Added M3 heat-set mounting for the LED holder
- Revised LED holder insert direction for improved mechanical retention
- Added recessed front-shell screw mounting for the LED holder
- Enlarged the rear power-button nut recess for improved thread engagement
- Rebuilt the Steam Controller puck opening using clean native FreeCAD geometry
- Merged standard and Steam Controller front-shell variants into one model
- Rebuilt the entire front shell as native parametric FreeCAD geometry
- Removed the front shell's dependency on imported STL geometry
- Added access holes behind magnet holders for easier magnet removal
- Added reusable FreeCAD spreadsheet parameters for hardware, fan, LED,
  magnet, USB, power-button and shell geometry
- Retained editable FreeCAD source files for modified parts
- Exported updated printable geometry from the FreeCAD models

Current development priority:

1. 2.5-inch drive mounting
2. GPU rear mounting

## Parametric configuration

The rebuilt front shell is designed around a shared FreeCAD spreadsheet.

Common dimensions and configurable options are stored as parameters rather than
being duplicated throughout individual sketches.

Examples include:

- shell dimensions
- M3 clearance and heat-set dimensions
- screwhead recess dimensions
- fan position
- fan size
- fan screw-hole layout
- USB opening dimensions
- power-button geometry
- magnet geometry
- LED aperture geometry
- LED holder dimensions

Optional and mutually exclusive features are controlled using expressions on
the Part Design **Suppressed** property.

For example:

- `Fan_Size = 120` enables the 120 mm fan aperture and screw pattern
- `Fan_Size = 140` enables the 140 mm fan aperture and screw pattern
- the Steam Controller puck can be enabled or disabled independently
- LED-related features can be configured independently where required

This allows multiple front-shell variants to be generated from a single source
model.

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

The project started by importing the original STL files into FreeCAD, refining
them into usable solids, and applying Part Design modifications on top.

That workflow is still used where appropriate for parts that have not yet been
rebuilt.

The preferred direction for major modified parts is now native FreeCAD
geometry.

Where practical, models use:

- native Part Design Bodies
- parametric sketches
- spreadsheet-driven dimensions
- Part Design pads and pockets
- Part Design Hole features for repeated hardware holes
- shared parameters for matching geometry across multiple parts
- feature suppression for configurable variants
- fillets and finishing operations after the primary geometry is established

The rebuilt front shell is now fully native and no longer requires an STL-derived
BaseFeature.

This avoids much of the recompute overhead and topology complexity associated
with performing repeated boolean operations on imported triangulated geometry.

## Front-shell configuration

The front-shell model incorporates several previously separate design options
within one parametric FreeCAD document.

Current configurable features include:

- 120 mm or 140 mm front fan geometry
- optional Steam Controller puck cutout
- LED lightbar geometry
- matching LED holder and mounting features

The LED lightbar geometry and LED holder are maintained in the same FreeCAD
document so shared dimensions and mounting geometry remain aligned.

This reduces duplicated source files and keeps related front-shell changes in
one parametric model.

## Test parts and hardware fit

Small test parts are used where practical to validate hardware dimensions
before committing to a full front-shell print.

These test pieces allow checks for:

- M3 screw clearance
- screwhead recess diameter and depth
- heat-set insert fit
- magnet fit
- power-button fit
- USB opening dimensions
- other press-fit and clearance-sensitive geometry

This makes it easier to tune spreadsheet parameters for the actual printer,
material and hardware without repeatedly printing the complete shell.

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