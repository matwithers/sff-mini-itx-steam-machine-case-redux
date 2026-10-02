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

The initial goals of this remix are:

### 1. Heat-set inserts

Replace printed/self-tapping screw threads where practical with proper
heat-set threaded inserts.

The intention is to make frequently assembled parts more durable and allow
normal machine screws to be used throughout the case.

### 2. LED light bar

Add provision for an integrated LED light bar while keeping the external
appearance of the case clean.

The mounting system and electronics are still under development.

### 3. 2.5-inch drive mounting

Add proper internal mounting for one or more 2.5-inch SATA SSDs / hard drives.

The aim is to add storage without significantly compromising airflow or the
compact layout of the original case.

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