# Product Context: ArduStim

## Problem Statement
Engine management systems require accurate trigger wheel signals (crank and cam) for proper operation. Testing these systems typically requires a running engine, which is:
- Expensive to maintain
- Difficult to control precisely
- Potentially dangerous
- Time-consuming to set up

ArduStim solves this by providing a hardware-in-the-loop testing solution that generates accurate trigger wheel patterns without requiring a physical engine.

## User Experience Goals
- Simple configuration via serial commands or potentiometers
- Accurate signal generation matching real engine patterns
- Flexible RPM control for testing various engine speeds
- Easy selection of different wheel patterns for different engine types
- Persistent configuration that survives power cycles

## Success Metrics
- Accurate timing of generated signals (matches real engine patterns)
- Support for 60+ different wheel pattern types
- Stable operation across wide RPM range
- Reliable configuration persistence
- Clear serial communication interface

