# Changelog

## [2.0.1] - 2026-04-22

### Fixed
- **Spray Boom Rotation**: Fixed reversed spray direction caused by inverted boom rotation axes. The left and right boom rotation values were swapped, causing spray effects to apply in the opposite direction than intended.
  - Left boom: Changed from `-90°` to `+90°` rotation
  - Right boom: Changed from `+90°` to `-90°` rotation  

- **Cabin Entry Position**: Fixed player positioning issue where entering the vehicle would push the player under the vehicle or leave them on the ground level.
  - Adjusted `player_root` Y-axis translation from `-0.000892583` to `1.2` to properly seat the player in the cabin
  - Adjusted `indoorCamera` Y-axis translation from `1.2066` to `1.4` for improved camera positioning inside the cabin

### Technical Details
- Files Modified:
  - `FS22_Fendt_Rogator_6x5/rogator.xml` (boom rotation animation parameters)
  - `FS22_Fendt_Rogator_6x5/Models/rogator.i3d` (node positioning)

### Testing
- Tested spray direction on left and right booms - now applies correctly
- Tested cabin entry - player now properly positioned in seat
- Tested camera positioning - no clipping or out-of-bounds views

### Credits
- Fixes based on community feedback and code analysis
- Branch: `fix/spray-and-cabin-issues`

---

## Previous Versions
See git history for earlier versions and changes.
