# keyboard-esp32

Firmware for a custom PS/2 keyboard built on the ESP32-S3. Work in progress.

## What it is

A keyboard controller that scans a 5×6 key matrix and outputs PS/2 scan codes to a connected PC. The ESP32-S3 handles both the matrix scanning (using the dedicated GPIO peripheral) and PS/2 signal generation (using a hardware timer ISR).

## Hardware

- **MCU**: ESP32-S3 (DevKitC-1 for development)
- **Matrix**: 5 rows × 6 columns = 30 keys, interrupt-driven with debounce
- **Output**: PS/2 (Clock + Data), scan code set 2

## Status

- [x] Matrix keyboard component (from ESP-IDF example, adapted for ESP32-S3)
- [ ] PS/2 transmitter component (hardware timer ISR + FreeRTOS queue)
- [ ] Keymap (row/col → PS/2 scan codes)
- [ ] Main application wiring it together
- [ ] Hardware build
