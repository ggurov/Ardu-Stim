# Project Brief: ArduStim

## Overview
ArduStim is an Arduino-based project that simulates crank and cam angle wheel patterns for use with engine management systems. The system uses an Arduino Mega 2560 microcontroller to output defined patterns to two pins (crank and cam), simulating various patterns of teeth and cam pulses for different engine types and configurations.

## Core Requirements
- Generate accurate crank and cam angle wheel patterns for engine management system testing
- Support multiple wheel pattern definitions (60+ different engine patterns)
- Output signals to two pins: crank and cam
- Allow configuration of RPM (fixed, pot-controlled, or swept)
- Store configuration in EEPROM for persistence
- Support serial communication for configuration and control

## Goals
- Provide accurate simulation of engine trigger wheel patterns for testing engine management systems
- Support a wide variety of engine configurations and wheel patterns
- Enable easy configuration and testing without physical engine hardware
- Maintain high timing accuracy for reliable engine management system testing

## Project Scope
**In Scope:**
- Wheel pattern generation and output
- RPM control (fixed, potentiometer, sweep modes)
- Serial communication interface
- EEPROM configuration storage
- Support for multiple wheel pattern types

**Out of Scope:**
- Physical hardware design (assumes Arduino Mega 2560)
- Engine management system logic (only simulates trigger signals)
- User interface beyond serial commands

