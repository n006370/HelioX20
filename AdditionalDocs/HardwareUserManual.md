# Helio X20 Development Board Hardware User Manual

### Table of Contents
- Table of Contents
- Introduction
- What's in the Box
- Board Overview
- Key Components
- System Block Diagram
- Getting Started
   - Prerequisites
   - Starting the board for the first time
- Component Details
   - Processor
   - PMIC
   - Memory (DRAM)
   - Storage
   - Micro SDHC
   - Boot ROM
   - Networking
   - WiFi
   - Bluetooth
   - GPS
   - HDMI
   - MIPI-DSI
   - Camera Interface
   - USB Ports
   - USB Host ports
   - USB Device ports
   - Audio
   - DC Power
   - Power Measurement
   - External Fan Connection
   - UART
   - Buttons
   - LED Indicators
   - Additional Functionality
- Expansion Connectors
   - Low Speed Expansion Connector
   - High Speed Expansion Connector
   - Analog Expansion Connector
- Power Management Overview
   - Block Diagram
   - DC Power Input
   - Power Source Selection and Sequencing
   - Voltage Rails
-Mechanical Specification

## Introduction

The Helio X20 Development Board is a 96Boards compliant community board based on MediaTek HELIO X20 platform.The following table lists its key features:

- **Processor**:
   - MediaTek HELIO X20 MT6797
   - Dual-core ARM@Cortex-A72 MPCoreTM  operating at up to 2.3GHz
   - Quad-core ARM@Cortex-A53 MPCoreTM operating at up to 1.85GHz
   - Quad-core ARM@Cortex-A53 MPCoreTM operating at up to 1.4GHz
   - Quad-core Mail T880, operating at up to 700MHz
   - Two ARM@Cortex-R4 processors operating  at up to 800MHz for MD MCU
   - Embedded connectivity system including WLAN/BT/FM/GPS
- **Memory / Storage**:
   - 2GB LPDDR3 2CH, 933MHz
   - 8GB eMMC 5.1
   - SD 3.0 (Micro SD card slot)
- **Video**:
   - HEVC decoder 2160p@30fps
   - VP9 decoder 2160p@30fps
   - H.264 decoder  2160p@30fps
   - Sorenson H.263/ H.263 decoder: 1080p@60fps/40Mbps
   - MPEG-4 SP/ASP decoder: 1080p@60fps/40Mbps
   - DIVX4/ DIVX5/ DIVX6/ DIVX HD/XVID decoder: 1080p@60fps/40Mbps
   - MPEG-4 encoder: Simple profile D1@30fps
   - H.263 encoder: Simple profile D1@30fps
   - H.264 encoder:  High profile 2160p@30fps
   - HEVC encoder:  Main profile 2160p@30fps
- **Camera Support**:
   - Main camera IO supports 25M camera module
   - Sub camera IO supports 8M camera module
- **Audio**:
   - Audio encoding: AMR-NB, AMR-WB,AAC,OGG,ADPCM
   - Audio decoding:WAV,MP3,MP2,AAC,AMR-NB,AMR-WB,MIDI,Vorbis,APE,AAC-plus v1/2,FLAC,WMA,ADPCM
- **Connectivity**:
   - WLAN 802.11a/b/g/n 2.4GHz and 5GHz(On-board BT and WLAN antenna )
   - Bluetooth 4.1 +HS compliant
   - GPS (with antenna connector)
   - One USB 2.0 micro B (device mode only)
   - Two USB 2.0 (host mode only)
- **I/O Interfaces**:
   - One 40-pin Low Speed (LS) expansion connector
      - UART, SPI, I2S, I2C x2, GPIO x12, DC power
   - One 60-pin High Speed (HS) expansion connector
      - 4L-MIPI DSI, USB, I2C x2, 2L+4L-MIPI CSI
   - One 16-pin analog expansion connector
      - Stereo headset/line-out, speaker and analog line-in
- **EXternal Storage**:
   - Micro SD card slot (SD 3.0)
- **User Interface**:
   - 4 Buttons :Power/Reset/Volume Up/down
   - 6 LED indicators
      -  4 -user controllable
      -  2 -for radios (BT and WLAN activity)
- **OS Support**:
   - Android 6.0
- **Mechanical**: 
   - Dimensions: 54mm by 85mm meeting 96Boards™ Consumer Edition standard dimensions specifications.
- **Environmental**:
   - Operating Temp: -20°C to +45°C
   - RoHS and Reach compliant

## What's in the Box

The box contains one Helio X20 Development Board and a quick start guide.

<Insert Helio X20 Board image>
<Insert Dev Board manual image>

## Board Overview

| Position |    Reference    | Description                                               |
|---------:|:---------------:|:----------------------------------------------------------|
|    1     |     CON7001     |   Low Speed Expansion Connector                           |
|    2     |      U4001      |   8GB EMMC                                                |
|    3     |      U1001      |   MediaTek Helio X20 MT6797 Soc + 2GB LPDDR3              |
|    4     |      U2001      |   PMIC  MT6351                                            |
|    5     |      U1001      |   Analog Expansion Connector                              |
|    6     |      U5003      |   WLAN/Bluetooth/GPS                                      |
|    7     |      J901       |   Power Outlet                                            |
|    8     |     CON4101     |   Micro SD Card Socket                                    |
|    9     |     CON6501     |   HDMI Type A Port                                        |
|    10    |     CON7101     |   High Speed Connector                                    |
|    11    |     CON6403     |   Micro USB Type B Connecto                               |
|    12    | LED3201-LED3204 |   LED3201,LED3202,LED3203,LED3204 can be defined by user  |
|          |     LED3205     |   LED3205 is WLAN LED                                     |
|          |     LED3206     |   LED3206 is Bluetooth LED                                |
|    13    |     CON6402     |   USB Host2 Connector                                     |
|    14    |     CON6401     |   USB Host1 Connector                                     |
|    15    |      SW3201     |   Power Button                                            |
|          |      SW3202     |   Vol up Button                                           |
|          |      SW3203     |   Vol down Button                                         |
|          |      SW3204     |   Reset Button                                            |
|    16    |     ANT5001     |   Bluetooth/WLAN Antenna                                  |
|    17    |     CON5006     |   GPS Antenna connector                                   |
|    18    |     SW3205      |   Switch for Auto boot and USB HOST set                   |

