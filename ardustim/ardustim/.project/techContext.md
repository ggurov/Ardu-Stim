# Tech Context: ArduStim

## Technologies Used
- **Arduino Mega 2560**: Microcontroller platform
- **Arduino IDE/Platform**: Development environment
- **C/C++**: Programming language
- **EEPROM**: Non-volatile storage for configuration
- **Timer/Counter (Timer1)**: Hardware timer for ISR-based signal generation
- **ADC**: Analog-to-digital conversion for potentiometer inputs
- **Serial Communication**: UART for configuration and control

## Development Setup
- Arduino Mega 2560 hardware
- Arduino IDE or compatible toolchain
- Serial monitor for configuration and debugging
- Potentiometers for RPM and wheel selection (optional)

## Technical Constraints
- Limited RAM: Wheel patterns stored in PROGMEM to conserve RAM
- Timer precision: ISR timing must be accurate for signal generation
- EEPROM size: Limited storage for configuration data
- Maximum RPM: Limited by ISR execution time and pattern complexity
- Pattern complexity: More edges = lower maximum RPM capability

## Dependencies
- Arduino core libraries (EEPROM, avr/pgmspace)
- Hardware: Arduino Mega 2560
- External: Potentiometers (optional), serial connection

## Tool Usage Patterns
- Compile and upload via Arduino IDE
- Serial monitor for configuration and testing
- EEPROM used for configuration persistence
- PROGMEM for storing large wheel pattern arrays

