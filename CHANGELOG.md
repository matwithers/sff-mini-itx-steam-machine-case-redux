# Changelog

## [Unreleased]

### Planned

- Add mounting for 2.5-inch SATA drives
- Improve rear GPU mounting

## [0.4.0] - 2026-10-04

### Added

- Integrated LED lightbar aperture in the front shell
- Diffuser channel and rear component clearance for the LED lightbar
- Separate parametric LED holder for the lightbar modules
- M3 heat-set insert mounting for the LED holder
- Recessed front-shell screw mounting for the LED holder
- Optional Steam Controller puck cutout in the main front-shell model
- Reusable FreeCAD spreadsheet parameters for LED and mounting geometry

### Changed

- Rebuilt the Steam Controller puck opening as clean native FreeCAD sketch geometry
- Merged the standard and Steam Controller puck front-shell variants into a single configurable model
- Removed the need for a separate Steam Controller puck front-shell source file
- Positioned LED holder mounting holes parametrically from the LED aperture geometry
- Added recessed screwhead pockets matching the existing front-shell fastener style

## [0.3.0] - 2026-10-03

### Changed

- Enlarged front and rear fan mounting holes to provide clearance for standard PC fan screws
- Set fan screw clearance diameter to 5.2 mm
- Added fan screw clearance as a reusable FreeCAD spreadsheet parameter
- Updated exported printable geometry

## [0.2.0] - 2026-10-03

### Changed

- Converted appropriate screw locations to M3 heat-set inserts
- Enlarged mating holes to M3 clearance dimensions
- Added spreadsheet-driven FreeCAD parameters for:
  - M3 heat-set insert bore
  - M3 heat-set insert depth
  - M3 clearance hole
- Updated modified parts to use editable Part Design features where practical
- Exported updated STL geometry

## [0.1.0]

### Added

- Initial repository structure
- Original reference STL files
- Initial FreeCAD source files
- Project README and licensing attribution