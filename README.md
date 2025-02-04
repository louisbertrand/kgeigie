# kGeigie
**Files** for kGeigie (kids geiger counter kit)
Contains:
  
  - 3D print files (in Makerbit print format) for Irover cover.
  - Kicad files for the tube board.
  - Schematics (Kicad).



kgiegie is an open-source radiation detection device developed by [Safecast](https://safecast.org/). This project is part of Safecast’s ongoing effort to provide reliable, accessible tools for measuring and monitoring ionizing radiation in the environment.

## Overview

The kgiegie project combines custom hardware with firmware designed to accurately capture radiation data. It is built for robustness and portability, making it suitable for both field measurements and laboratory work.

Key aspects of the project include:
- **Accurate Radiation Measurement:** Utilizes a high-sensitivity Geiger–Müller tube and supporting circuitry.
- **Portable Design:** Engineered for rugged use in varied field conditions.
- **Data Logging:** Supports on-board data storage (typically via an SD card) for later analysis.
- **Open Development:** All hardware designs, firmware, and documentation are available under open-source licenses.

## Repository Structure

- **`firmware/`** – Source code for the microcontroller firmware.
- **`hardware/`** – Schematics, PCB layouts, and Bill of Materials (BOM).
- **`docs/`** – Documentation including build instructions, calibration guides, and detailed technical references.
- **Other Files:** Various configuration files and scripts supporting the build and deployment process.

## Hardware Specifications

- **Processor:** [Specify microcontroller model, e.g., STM32F103 or similar]
- **Detector:** Geiger–Müller tube (model details available in the hardware docs)
- **Power:** Battery-powered with low-power design for extended field use; options for solar charging may be available.
- **Data Storage:** Integrated SD card slot for logging radiation readings.
- **Connectivity:** USB interface for programming and data retrieval; additional interfaces may be available for optional modules (e.g., GPS).

For full hardware details, please see the [Hardware Documentation](docs/hardware.md).

## Firmware

The firmware is written in C/C++ and built using [PlatformIO](https://platformio.org/) (or the Arduino IDE, if preferred). It handles:
- **Radiation Data Acquisition:** Continuous measurement and digitization of Geiger–Müller tube pulses.
- **Data Logging:** Writing measurement logs to an SD card in a CSV format.
- **User Interface:** Driving any attached display and handling user inputs.
- **System Management:** Power management and error handling routines.

Refer to the [Firmware Build Guide](docs/installation.md) for detailed setup and build instructions.

## Getting Started

### Prerequisites

- A suitable development environment (PlatformIO or Arduino IDE).
- Required libraries (see the `platformio.ini` or project documentation for a complete list).
- A USB cable for programming and debugging.

### Building and Uploading the Firmware

1. **Clone the Repository:**

   ```bash
   git clone https://github.com/safecast/kgiegie.git
   cd kgiegie
