# 3D LiDAR Scanner 

This repository contains all the source code, 3D-printable mechanical files, and hardware schematics required to build an open-source **DIY 3D LiDAR Scanner**. 

The project captures environment details by rotating a time-of-flight (ToF) laser range finder sensor over two independent axes (yaw and tilt) via a mechanical swashplate design, creating detailed 3D point clouds.

---

## Key Specifications

* **Resolution:** ρ = 1cm, θ = 0.15°, φ = 0.3°
* **Max Range:** 8 meters (with TF-Luna module)
* **Data Interface:** Serial over USB @ 115200 baud
* **Rotational Speed:** Recommended 60 RPM (Max 150 RPM)
* **Core Microcontroller:** STM32 "Blue Pill" (32-bit ARM Cortex-M3 @ 72 MHz)

---

## Repository Structure

This repository is organized into the following direct directories:

* **`/STL/Files`:** Contains all the 3D-printable `.stl` files for mechanical fabrication.
* **`/SLDPTR`:** Contains your native SolidWorks part source models.
* **`/Circuit`:** Includes hardware schematics, wiring layouts, and electronics setup.
* **`/Ardunio Code`:** The core MCU firmware code written for the STM32 microcontroller.
* **`/Processing Code/Lidar Viewer`:** The processing sketches used to render and view the 3D point cloud interface.

---

## Bill of Materials (BOM)

The estimated cost to build this unit is approximately **₹3,700** (~$40 USD). Below is the itemized component breakdown with current Indian Rupee (INR) market pricing:

| Qty | Item | Approximate Cost (INR) |
| :---: | :--- | :--- |
| 1 | STM32F103 "Blue Pill" Development Board | ₹189 |
| 1 | TF-Luna LiDAR ToF Range Finder Module | ₹2,350 |
| 1 | DRV8825 Stepper Motor Driver Module | ₹85 |
| 1 | NEMA 17HS4023 "Pancake" Stepper Motor | ₹690 |
| 2 | SG90 9g Miniature Servo Motors | ₹245 |
| 1 | Mini 360 DC-DC Buck Converter Module | ₹95 |
| 1 | USB 2.0 to UART Serial Converter Module | ₹95 |
| 15 | M3 × 6mm Screws | ₹189 |
| 2 | M2.5 Screws | ₹95 |
| 1 | 40×40mm Flat Glass Mirror Piece | ₹50 |
| 1 | Solderless Breadboard | ₹95 |
| - | PLA Filament (approx. 100g) | ₹280 |
| **Total** | **Estimated Hardware Investment** | **~ ₹4,758** |

*Note: Prices may vary slightly depending on your preferred e-commerce vendor or local electronics store.*

---
## Software & Toolchain Requirements

To compile and execute the system files, you will need:
1. **Arduino IDE** (with the `stm32duino` board manager library installed).
2. **Processing IDE** (Java framework) to compile and view the live `LidarViewer` environment.

---

## 📝 License

This project is open-source software and is licensed under the **MIT License**. See the accompanying `LICENSE` file for full terms and details.
