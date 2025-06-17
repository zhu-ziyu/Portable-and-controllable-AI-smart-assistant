# ZhiTech AI Assistant NOVA

> A portable, controllable AI smart assistant with edge‐AI inference, visual UI, high-fidelity audio, and a modular, sculptural design.

[![GitHub Stars](https://img.shields.io/github/stars/zhu-ziyu/Portable-and-controllable-AI-smart-assistant.svg)](https://github.com/zhu-ziyu/Portable-and-controllable-AI-smart-assistant/stargazers)  
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)  
[![Issues](https://img.shields.io/github/issues/zhu-ziyu/Portable-and-controllable-AI-smart-assistant.svg)](https://github.com/zhu-ziyu/Portable-and-controllable-AI-smart-assistant/issues)  

---

## Table of Contents

1. [Introduction](#introduction)  
2. [Key Features](#key-features)  
3. [Hardware Design](#hardware-design)  
   - [Core Processor: ESP32-S3](#core-processor-esp32-s3)  
   - [Front Panel: ABS-GF](#front-panel-abs-gf)  
   - [Backplane & Vents: ASA](#backplane--vents-asa)  
   - [Structural Supports: PA6-GF](#structural-supports-pa6-gf)  
   - [Magnetic Fold-Flat Stand](#magnetic-fold-flat-stand)  
   - [Six-Mic PDM Array](#six-mic-pdm-array)  
   - [High-Fidelity Audio Codec](#high-fidelity-audio-codec)  
4. [Enclosure Materials & Finishes](#enclosure-materials--finishes)  
5. [Software Architecture](#software-architecture)  
   - [Embedded Firmware](#embedded-firmware)  
   - [Visual UI Routines](#visual-ui-routines)  
   - [Over-The-Air Updates & Dashboard](#over-the-air-updates--dashboard)  
6. [Performance Comparison](#performance-comparison)  
7. [Installation & Setup](#installation--setup)  
8. [Usage](#usage)  
9. [Customization & Community](#customization--community)  
10. [Development & Contribution](#development--contribution)  
11. [Project Roadmap](#project-roadmap)  
12. [Acknowledgements & Credits](#acknowledgements--credits)  
13. [License](#license)  
14. [Contact](#contact)  

---

## Introduction

Welcome to **ZhiTech AI Assistant NOVA**—a next-generation, pocket-sized AI companion that processes speech, executes commands, and displays real-time feedback entirely on-device. Boasting a powerful ESP32-S3 edge-AI core, a crisp 0.96″ OLED screen, a six-mic array, and a fold-flat magnetic kickstand, NOVA delivers privacy, responsiveness, and style at a fraction of the cost of cloud-dependent smart speakers. Whether you’re an AI enthusiast, a busy professional, a student, or a tech hobbyist, NOVA adapts to your world: as a desktop ornament, a smart remote, or an always-on voice assistant.

---

## Key Features

| Feature                                | Description                                                                                                                          | Competitive Edge                                                                                                                                                                                                                        |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Edge AI Core**                       | ESP32-S3 dual-core Xtensa LX7 @ 240 MHz with vector extensions for on-device NN acceleration                                           | Sub-50 ms wake-word detection & command parsing vs. host-dependent ML on Raspberry Pi Pico W                                                                                                                                            |
| **Industrial-Grade Front Panel**       | ABS-GF (glass-fiber–reinforced ABS) for +50 % tensile strength, HDT ~ 93 °C, Shore D ≈ 82                                                  | Far more rigid and heat-stable than Echo Dot’s fabric shell                                                                                                                                                                             |
| **Advanced Thermal Management**        | ASA backplane with “lightning” vents, k = 0.18 W/m·K, Vicat softening point ~ 96 °C                                                    | Sustains heavy AI loads without thermal throttling, unlike Nest Mini’s simple plastic enclosure                                                                                                                                          |
| **Low-Power Visual UI**                | 0.96″ SSD1306 monochrome OLED @ < 5 mA, high contrast and self-lit display                                                            | Provides real-time animations, volume meters, and status—whereas most smart speakers lack any screen                                                                                                                                     |
| **Magnetic Fold-Flat Stand**           | Integrated magnetic alloy hinge; folds flush for fridge-magnet use or pops out on carbon-fiber struts                                  | Eliminates need for aftermarket mounts; doubles as decorative refrigerator magnet                                                                                                                                                       |
| **Ultra-Light, High-Rigidity Support** | Carbon-fiber rods with > 200 % strength-to-weight ratio                                                                                | Outclasses generic ABS/nylon kickstand brackets for rock-solid stability with minimal bulk                                                                                                                                                |
| **Six-Mic PDM Array**                  | Beamforming array, six MEMS mics @ 30 mm radius captures clear voice up to 5 m in noisy environments                                   | Better range & SNR vs. Echo Dot’s 3-mic layout and Google Nest Mini’s 3-mic design                                                                                                                                                      |
| **High-Fidelity Audio Codec**          | Dedicated TLV320ADC5140 chipset provides 40 dB lower noise floor vs. basic ADCs                                                      | Crystal-clear voice pickup & recording; eliminates digital noise and EMI artifacts                                                                                                                                                       |
| **Programmable Visual Keys**           | Touch-sensitive, LED-backlit buttons fully configurable via firmware                                                                   | Macros, status indicators, and custom shortcuts, vs. rigid fixed-function buttons on Echo Show 5                                                                                                                                         |
| **Sculptural Tech Aesthetic**          | Transparent rigid resin, matte-metal finishes, sharp bevels, and clean lines that transform NOVA into a desktop art piece when idle    | Unique combination of form & function; stands out in a market of purely functional, fabric-wrapped speakers                                                                                                                              |

---

## Hardware Design

### Core Processor: ESP32-S3
- **Processor**: Dual-core Xtensa LX7 @ 240 MHz  
- **ML Acceleration**: Integrated vector extensions for convolutional and fully connected layers  
- **Connectivity**: Wi-Fi 802.11 b/g/n, Bluetooth 5.0 LE  
- **Memory**: 512 KB SRAM + PSRAM support  
- **Inference Performance**: < 50 ms latency for common wake-word and intent-classification models  
- **Power**: ~ 80 mA active, < 5 mA deep sleep  

### Front Panel: ABS-GF
- **Material**: ABS with 10 % chopped glass fibers  
- **Tensile Strength**: ~ 45 MPa (+50 % vs. pure ABS)  
- **Heat-Deflection Temp**: ~ 93 °C  
- **Shore D Hardness**: ~ 82  
- **Manufacturing**: High-precision injection molding for tight tolerances around screen & button cutouts  

### Backplane & Vents: ASA
- **Material**: Acrylonitrile Styrene Acrylate  
- **Thermal Conductivity**: 0.18 W/m·K  
- **Vicat Softening Point**: ~ 96 °C  
- **UV & Weather Resistance**: Suitable for sunlit or humid environments  
- **Vent Pattern**: “Lightning” geometry for maximized passive airflow without compromising aesthetics  

### Structural Supports: PA6-GF
- **Material**: Nylon 6 with 30 % glass fiber  
- **Tensile Strength**: > 140 MPa  
- **Chemical & Impact Resistance**: Ideal for internal brackets, side rails, and kickstand housing  
- **Print-In-Place**: Precision clearance optimized at 0.2 mm for hinge action  

### Magnetic Fold-Flat Stand
- **Hinge**: Embedded magnetic alloy; 360° rotation, self-locking  
- **Stowed Mode**: Flush to backplane; friction fit as refrigerator magnet  
- **Deployed Mode**: Supported by carbon-fiber rods for stable viewing angles  
- **Lifetime**: > 10,000 cycles of fold/unfold without play  

### Six-Mic PDM Array
- **Configuration**: Circular array, 30 mm radius spacing  
- **Beamforming**: Real-time DSP for direction-of-arrival and noise cancellation  
- **Range**: Clear command capture up to 5 m in > 70 dB ambient noise  
- **Interface**: I²S to high-performance codec  

### High-Fidelity Audio Codec
- **Chipset**: TI TLV320ADC5140  
- **Dynamic Range**: +100 dB  
- **Noise Floor**: –103 dBFS (~ 40 dB improvement vs. basic ADCs)  
- **Features**: Programmable gain, differential inputs, headphone amp  

---

## Enclosure Materials & Finishes

1. **Surface Treatments**  
   - Front ABS-GF: Low-temperature UV-curable powder coat for scratch resistance  
   - Back ASA: Matte UV-stable paint to preserve color fidelity  
   - Resin Accent: Transparent rigid resin window over ESP32 for a “glow” effect  

2. **Post-Processing**  
   - Snap-fit joins with ultrasonic welding—dust-proof and seamless  
   - Solvent-bonded logos and accent stripes for premium feel  
   - Optional electroplating of bezel ring for metallic shine  

3. **Customization Options**  
   - Color variants: Onyx Black, Graphite Gray, Arctic White  
   - Logo inlays: Laser-etched or solvent-filled for contrast  

---

## Software Architecture

### Embedded Firmware
- **Language**: C / C++ (ESP-IDF framework)  
- **RTOS**: FreeRTOS for task scheduling  
- **Modules**:  
  - Wake-word engine (Porcupine / custom)  
  - Intent parser (TensorFlow Lite Micro)  
  - Mic array DSP (beamforming & denoise)  
  - Display driver (SSD1306)  
  - GPIO management for visual keys and kickstand sensor  
- **Unit Testing**: Screen, mic, JSON parser, OTA agent  

### Visual UI Routines
- **Framework**: Custom lightweight animation engine  
- **Features**:  
  - Volume meters, wake-word ripple effect  
  - Routine progress bars, emoji & text notifications  
  - Customizable skins via JSON theming  

### Over-The-Air Updates & Dashboard
- **Server**: AWS S3 + Lambda update broker  
- **Client**: Secure OTA agent with rollback protection  
- **Dashboard**:  
  - Web/mobile app with drag-and-drop routine builder  
  - Real-time device logs and metrics  
  - Theme & firmware management  

---

## Performance Comparison

| Specification               | NOVA                                  | Echo Dot (5th Gen)       | Google Nest Mini         | Raspberry Pi Pico W    |
|-----------------------------|---------------------------------------|--------------------------|--------------------------|------------------------|
| Edge AI Inference Latency   | < 50 ms                               | N/A (cloud required)     | N/A (cloud required)     | > 200 ms (host-based)  |
| Wake-Word Support           | Offline (Porcupine / TFLM)            | Alexa cloud             | Google cloud            | DIY only               |
| Display                     | 0.96″ OLED @ < 5 mA                    | None                     | None                     | None                   |
| Mic Count                   | 6 (beamforming PDM)                   | 4 (3+1 reserved)         | 3                        | 0                      |
| Audio Codec                 | TLV320ADC5140 (–103 dBFS noise floor) | TLV320ADC5140 onboard    | SGTL5000                 | DIY ADD-ON             |
| Thermal Management          | ASA vents + passive metal inserts     | Plastic enclosure        | Plastic enclosure        | N/A                    |
| Dimensions                  | 80 × 60 × 20 mm                        | 100 × 100 × 89 mm         | 98 × 98 × 42 mm          | 51 × 21 × 3 mm          |
| Price Point                 | < \$60                                | \$49.99                  | \$49                     | \$4                     |

---

## Installation & Setup

1. **Clone the Repository**  
   ```bash
   git clone https://github.com/zhu-ziyu/Portable-and-controllable-AI-smart-assistant.git
   cd Portable-and-controllable-AI-smart-assistant
