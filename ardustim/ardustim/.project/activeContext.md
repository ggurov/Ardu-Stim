# Active Context: ArduStim

## Current Work Focus
Initial memory bank creation and project documentation setup.

## Recent Changes
- Created memory bank structure
- Documented project overview and technical context

## Next Steps
- Continue development as needed
- Update memory bank as project evolves

## Active Decisions and Considerations
- Memory bank structure follows standard template
- Documentation based on existing codebase analysis

## Important Patterns and Preferences
- Wheel definitions stored in `wheel_defs.h` as PROGMEM arrays
- Configuration stored in EEPROM for persistence
- ISR-based timing for accurate signal generation
- RPM scaling based on wheel pattern edge count

## Learnings and Project Insights
- Project uses Arduino Mega 2560 with extensive wheel pattern library
- Supports multiple RPM control modes (fixed, pot, sweep)
- Wheel patterns defined as arrays of edge states (0=no tooth, 1=crank, 2=cam1, 4=cam2, combinations allowed)
- RPM scaling factor calculated based on number of edges relative to 60-2 pattern (120 edges = 1.0 scaling)

