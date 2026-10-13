# Block Sorting Algorithm and System

### A Two-Axis Stepper-Driven Machine for Automated Block Sorting

![Language](https://img.shields.io/badge/code-C%2B%2B-00599C)
![Controller](https://img.shields.io/badge/controller-Arduino%20Mega-teal)
![Actuators](https://img.shields.io/badge/actuators-2x%20stepper%20%2B%20servo-blue)
<!-- TODO: Add license badge -->

<p align="center">
  <img src="docs/images/hero.png" alt="Block sorting system" width="75%">
  <br>
  <em>PLACEHOLDER: Hero image of the assembled block sorting system.</em>
</p>

## Overview

This project is a mechatronic system that sorts blocks automatically using a two-axis gantry driven by stepper motors, with a servo for the pick-and-place action. An Arduino Mega controls the hardware, and the sorting algorithm is implemented in C++.


## Key Features

- **Two-axis motion** with independent X and Y stepper motor axes
- **Servo actuation** for block handling
- **Dedicated stepper drivers** powered from a 12 V supply
- **C++ sorting algorithm** with separate Arduino firmware
- **Full design files:** CAD models, electronics, and reference archive

## How It Works


1. The system initializes and homes the X and Y axes.
2. Block positions or properties are read in.
3. The sorting algorithm decides the order of moves.
4. Stepper commands move the gantry to each block's position.
5. The servo picks up and releases each block at its sorted destination.

## Hardware

| Component | Description |
|---|---|
| Microcontroller | Arduino Mega |
| Motors | 2x stepper motors (X axis and Y axis) |
| Motor Drivers | 2x stepper drivers, one per axis |
| Actuator | 1x servo motor |
| Power | 12 V input via breadboard power module |
| Frame / Mechanism | Custom CAD design (see `03_CAD_Models`) |

### Wiring

The circuit schematic is stored in `04_Electronics`. Each stepper driver receives step and direction signals from the Arduino and motor power from the 12 V supply. The servo is driven directly from an Arduino PWM pin.


> **Note:** Always power the motor drivers from the 12 V supply before connecting motors, and never disconnect a motor while the system is powered.

## Repository Structure

```
.
├── 01_Arduino_Code/        # Arduino firmware for motor and servo control
├── 02_CPP_Code/            # C++ sorting algorithm
├── 03_CAD_Models/          # Mechanical design files
├── 04_Electronics/         # Circuit schematic and wiring
├── 05_Archive_Reference/   # Earlier versions and reference material
└── README.md
```

## Getting Started

### Prerequisites

- Arduino IDE 
- C++ compiler (e.g. g++) 
- The hardware listed above, wired per the schematic in `04_Electronics`

### Upload the Firmware

1. Open the sketch in `01_Arduino_Code` with the Arduino IDE.
2. Select **Arduino Mega** as the board and the correct serial port.
3. Upload the sketch.

### Build and Run the Algorithm

```bash
# TODO: replace with your actual build and run commands
cd 02_CPP_Code
g++ -std=c++17 -o block_sorter main.cpp
./block_sorter
```

## Results

<!-- TODO: Add measured performance, e.g. sorting accuracy, time per block, repeatability -->

| Metric | Value |
|---|---|
| Sorting accuracy | TBD |
| Average time per block | TBD |
| Positioning repeatability | TBD |


## Author

Shivam Dave

## License

<!-- TODO: Choose a license and add a LICENSE file -->
Licensed under the **MIT Open Source LICENSE**. See `LICENSE` for details.
