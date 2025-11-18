# System Patterns: ArduStim

## System Architecture
- **Main Loop**: Handles serial communication, configuration updates, and RPM mode management
- **ISR (Interrupt Service Routine)**: Generates precise timing for wheel pattern output
- **Configuration System**: EEPROM-based storage for persistent settings
- **Wheel Pattern System**: Array-based definitions stored in PROGMEM

## Key Technical Decisions
- Use of PROGMEM for wheel pattern storage (saves RAM)
- ISR-based timing for accurate signal generation
- EEPROM for configuration persistence
- RPM scaling based on edge count relative to 60-2 pattern (120 edges = reference)
- Two-pin output system (crank and cam)

## Design Patterns in Use
- **Array-based Pattern Definition**: Wheel patterns defined as arrays of edge states
- **Enum-based Wheel Selection**: WheelType enum maps to wheel definitions
- **Structure-based Configuration**: configTable struct holds all configuration
- **ISR Pattern Iteration**: Interrupt service routine iterates through wheel pattern arrays

## Component Relationships
- `wheel_defs.h`: Defines all wheel patterns and WheelType enum
- `globals.h`: Defines wheel structures, configuration structs, and global variables
- `ardustim.ino`: Main program loop and ISR setup
- `storage.ino`: EEPROM read/write for configuration
- `comms.cpp`: Serial communication command parser

## Critical Implementation Paths
1. **Pattern Generation**: ISR reads pattern from PROGMEM → applies RPM scaling → outputs to pins
2. **Configuration Load**: EEPROM read → validate → apply to config struct
3. **RPM Control**: Pot/Serial input → calculate RPM → adjust ISR timing
4. **Wheel Selection**: Enum value → lookup in Wheels[] array → set active pattern pointer

