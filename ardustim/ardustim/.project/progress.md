# Progress: ArduStim

## What Works
- Wheel pattern generation system with 60+ supported patterns
- RPM control modes (fixed, potentiometer, sweep)
- EEPROM configuration storage
- Serial communication interface for configuration
- ISR-based accurate timing generation
- Support for both crank and cam signals
- Multiple compression simulation types (2, 4, 6, 8 cylinder 4-stroke)

## What's Left to Build
- Additional wheel patterns as needed
- Potential GUI interface (currently serial-only)
- Enhanced documentation for end users

## Known Issues and Limitations
- Maximum RPM limited by pattern complexity (more edges = lower max RPM)
- Pattern accuracy depends on ISR timing precision
- EEPROM version management for configuration migration

## Evolution of Project Decisions
- Started with basic wheel patterns, expanded to 60+ patterns
- Added compression simulation for more realistic testing
- Implemented multiple RPM control modes for flexibility
- EEPROM storage added for configuration persistence
- Serial interface expanded for better control and monitoring

