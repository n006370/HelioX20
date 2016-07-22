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
|    12    | LED3201-LED3204 |   Can be defined by user                                  |
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

## System Block Diagram

<Insert System Block Diagram here>

## Getting Started

#### Prerequisites

Before you power up your Helio X20 Development Board for the first time you will need the following:

- Helio X20 Development Board.
- A 96Boards compliant power supply (sold separately ).
- A HDMI or DVI LCD Monitor that supports a resolution of 1080P/60Hz.
- HDMI-HDMI cable or HDMI-DVI cable to connect the board to the Monitor.
- A computer keyboard with USB interface.
- A computer mouse with USB interface.

#### Starting the board for the first time 

To start the board, follow these simple steps: 

1. Connect the HDMI cable to the Helio X20 Development Board connector (marked CON6501) and to the LCD Monitor. 
2. Set the the third pin (USB HOST SET) of switch SW3205 to the position ON and connect the keyboard to USB connector marked CON6402 and the mouse to the USB connector marked CON6401. (It doesn’t matter which order you connect them in. ) 
3. Plug the power supply into the power outlet.
4. Press down the button (marked SW3201), and keep more than 3 seconds, the Android system will start. 

> Note: If set the first pin (AUTO_BOOT_SET) of switch SW3205 to the position ON, the Android system will start automatically when the power supply is plugged into the power outlet.

## Component Details

### Processor
MT6797 is a highly integrated application processor which uses an industry-leading Tri-Cluster Deca-Core CPU Architecture. The chip integrates Dual-core ARM@Cortex-A72 MPCoreTM  operating at up to 2.3GHz, Quad-core ARM@Cortex-A53 MPCoreTM operating at up to 1.85GHz, Quad-core ARM@Cortex-A53 MPCoreTM  operating at up to 1.4GHz, Quad-core Mail T880 operating at up to 700MHz  and  an ARM@Cortex-R4 MCU . In addition, an extensive set of interfaces and connectivity peripherals are included to interface to cameras, touch-screen displays and MMC/SD cards.MT6797 also embodies wireless communication device, including WLAN, Bluetooth and GPS.

### PMIC

There are a PMIC and two dedicated DC - DC converters for MT6797 platform.
MT6351 is a power management system chip, containing 8 buck converters and 31 LDOs. 
DA9214 is a 4-phase high efficiency buck converter. It is applied to offer the kernel power of APU.

FAN53555 is high efficiency step-down switching regulator. It is applied to offer the DVDD power of GPU.

### Memory (DRAM)

The Helio X20 Development Board provides 2GB LPDDR3-SDRAM which is a 2-channel and 32bit width bus implementation interfacing directly to the MT6797 build-in LPDDR controller. The maximum DDR clock is 933MHz. It is mounted over the MT6797 using pop technology.

### Storage

The Helio X20 Development Board provides an 8GB EMMC which is compliant with EMMC 5.1.

### Micro SDHC

The Helio X20 Development Board SD slot signals are routed directly to the MT6797 MSDC1 interface. It meets the SD3.0 standard.

### Boot ROM

The Helio X20 Development Board boots up from the EMMC.

### Networking

#### WiFi

- Dual-band (2.4/5GHz) single stream 802.11 a/b/g/n/ac RF, 20/40/80MHz bandwidth.
- Integrated 2.4GHz PA with max. 20dBm CCK output power, 5GHz PA OFDM 54Mbps output power 17dBm and VHT80 MCS9 output power 15dBm.
- Typical Rx sensitivity :-76.5dBm at both 11g 54Mbps mode and 11a 54Mbps mode,-62dBm at 11ac VHT80 MCS9 mode
- Integrated power detector to support per packet Tx power control

The Helio X20 Development Board also has a RF connector to connect the external antenna or other RF device. If you want to use this function, you should put the R5072 on with 0ohm resistor and remove the R5071 from the board.

#### Bluetooth

- Bluetooth specification V2.1+EDR, 3.0+HS and 4.1+HS compliant
- Integrated PA with 8dBm (class 1) transmit power
- Typical Rx sensitivity: GFSK -94dBm, DQPSK -93dBm, 8-DPSK -87.5dBm.

#### GPS

The GPS implementation is based on MTK connectivity chip MT6631 (U5003) supporting GPS, Galileo, Glonass and Beidou. It can receive GPS, Galileo, Beidou / Glonass simultaneously for more accurate positioning. But there is no GPS antenna on the board. You need to connect an external antenna to the RF connector CON5006.

### HDMI 

The 96Boards specification calls for an HDMI port to be present on the board. The MT6797 doesn’t include a built-in HDMI interface. The Helio X20 Development Board deploys the built-in DPI interface as the source for the HDMI output. A peripheral Bridge IC (U6502, MT8193) performs this task and it supports a resolution from 480i to 1080p at 30Hz. 

### MIPI-DSI

The 96Boards specification calls for a MIPI-DSI implementation via the High Speed Expansion Connector. 

The Helio X20 Development Board implements a 4-lane MIPI_DSI interface meeting this requirement. It can support up to FHD(1080p@60fps). The Helio X20 Development Board routes the MIPI_DSI interface signals to the DSI-0 interface of the MT6797.

### Camera Interface

The 96Boards specification calls for two camera interfaces.
The Helio X20 Development Board supports two camera interfaces, one with a 4-lane MIPI_CSI interface and one with 2-lane MIPI_CSI interface, meeting this requirement. The 4-lane MIPI_CSI interface can support 25M camera and the 2-lane MIPI_CSI interface can support 8M camera. 

### USB Ports

The Helio X20 Development Board supports a USB device port and three USB host ports via a USB MUX(U6503). The input channel( D+/D-) of USB MUX is connected to the P0 port of the SOC MT6797, and the two output channels(1D+/1D-,2D+/2D-) are connected to micro USB port and USB hub respectively. The three USB host ports are connected to the downstream ports of the USB hub.The control of U6503 is done via a software controlled GPIO (USB_SW_SEL, EINT9 from the SOC MT6797). When this signal is logic low, ‘0’, the USB data lines are routed to the Micro USB connector and the MT6797 P0 port is set to device mode. When ‘USB_SW_SEL’ is logic level high, ‘1’, the USB data lines are routed to U6401 (a 3-port USB HUB) and the MT6797 P0 port is set to host mode. The user can overwrite the software control by sliding switch 3 of dip-switch SW3205 to the ‘ON’ position. That action forces the USB–MUX (U6503) to route the USB data lines to the USB HUB. The overwrite option exists for the host mode only, you cannot hardware overwrite the MUX to force device mode. 
<Insert image here>

### USB Host ports

The Helio X20 Development Board supports three USB host port via a USB2.0 hub (U6401 USB2513-AEZG). Its upstream signal is connected to USB_P0 interface of MT6797.

- Port 1 of the USB HUB is routed to CON6401, a Type ‘A’ USB Host connector. A current limited controller (U6402) sets the Power Current limit to 1.18A.  
- Port 2 of the USB HUB is routed to CON6402, a Type ‘A’ USB Host connector. A current limited controller (U6403) sets the Power Current limit to 1.18A. 
- Port 3 of the USB HUB is routed to the High Speed Expansion connector. No current limited controller is implemented on the board for this channel. 

### USB Device ports

The Helio X20 Development Board implements a device port. The port is located at CON6403, a Micro USB type B. It is routed to USB_P0 interface of MT6797.

> Note: the board can work in one mode at a time, Host mode or Device mode, not both. 

### Audio

The Helio X20 Development Board has four audio ports: BT, HDMI, PCM and analog port. The analog port which connected to MT6351 includes a stereo handset IO and two analog audio outputs.

### DC Power

The Helio X20 Development Board can be powered by two ways:

- 8V to 18V supply from a dedicated DC jack(J901) 
- 8V to 18V supply from the DC_IN pins on the Low Speed Expansion Connector(CON7001)

### Power Measurement

The Helio X20 Development Board has three current sense resistors R916\ R923\ R924.

| Reference |  Net    |  Description                                       |
|:----------|:--------|:---------------------------------------------------|
|    R916   |  DC_IN  |  To measure the current of total base board power  |
|    R923   |  SYS_5V |  To measure the current of SYS_5V power            |
|    R924   |  VBAT   |  To measure the current of VBAT power              |

### External Fan Connection

The 96Boards specification calls for support for an external fan. That can be achieved by using the 5V or the SYS_DCIN (12V), both present on the Low Speed Expansion connector.

### UART

The Helio X20 Development Board has two UART ports (UART1 / UART0), both present on the Low Speed Expansion connector. They are routed to the UART1 (UART1_TxD, UART1_RxD) and UART0 (UART0_TxD, UART0_RxD, UART0_CTS, UART0_RTS) interface of MT6797 separately. The UART1 is used for the serial console output.

### Buttons

The Helio X20 Development Board presents four buttons. They are Power key,VOL up key,VOL down key and Reset key. The power ON/OFF and RESET signals are also routed to the Low Speed Expansion connector.

#### Power Button 

The push-button SW3201 serves as the power-on/sleep button. Upon applying power to the board, press the power button for more than 3 seconds, the board will boot up. Once the board is running you can turn power-off by pressing the power button for more than 3 seconds. If the board is in a sleep mode, pressing the power bottom will wake up the board. Oppositely, if the board is in an active mode, pressing the power bottom will change the board into sleep mode. 

#### Reset Button

The push-button SW3204 serves as the hardware reset button. press the button for more than 1 seconds,the system will be rebooted.

#### Volume up

The Volume UP button is used to control the output speaker volume of the Helio X20 Development Board. 

#### Volume down

The Volume Down button is used to control the output speaker volume of the Helio X20 Development Board. 

#### Dip-switch

There is a four-channel dip-switch(SW3205) on the board.

- Channel 1:”AUTO BOOT”,used to boot the board automatically. If  set the switch on , the system will start automatically when the power supply is plugged into the power outlet. 
- Channel 2:NC.
- Channel 3:”USB HOST SET”,The user can overwrite the software control by sliding the switch to the ‘ON’ position.The overwrite option exists for the host mode only, you cannot hardware overwrite the MUX to force device mode. 
- Channel 4: NC


### LED Indicators

The Helio X20 Development Board has six LEDs.

#### Two activity LEDs

- WiFi activity LED –The Helio X20 Development Board drives this Yellow LED via BPI_BUS12, an IO from MT6797. 
- BT activity LED –The Helio X20 Development Board drives this Blue LED via BPI_BUS13, an IO from MT6797. 

#### Four User LEDs

The four user LEDs are surface mount Green in 0603 size located next to the micro USB connector. The Helio X20 Development Board drives the four LEDs from the MT6797 GPIO: BPI_BUS8, BPI_BUS9，BPI_BUS10 and BPI_BUS11.

### Additional Functionality

The Helio X20 Development Board also has a additional interface (CON9001)for user debugging. It includes JTAG , UART0 and UART1 interface. The position is reserved, but the component is not mounted in the mass production. The component of CON9001 is AXT640124 produced by Panasonic. This interface should be used with the MTK debug board.

## Expansion Connectors

### Low Speed Expansion Connector

|  Helio X20 Signals  |  96Boards Signals |  PIN  |  PIN  |  96Boards Signals  |  Helio X20 Signals  |
|:--------------------|:------------------|:------|------:|-------------------:|--------------------:|
|    GND              |     GND           |   1   |   2   |    GND             |    GND              |
|    UCTS0            |     UART0_CTS     |   3   |   4   |    PWR_BTN_N       |    PWRKEY           |
|    UTXD0            |     UART0_TxD     |   5   |   6   |    RST_BTN_N       |    SYSRSTB          |
|    URXD0            |     UART0_RxD     |   7   |   8   |    SPI0_SCLK       |    SPI0_CK          |
|    URTS0            |     UART0_RTS     |   9   |   10  |    SPI0_DIN        |    SPI0_MI          |
|    UTXD1            |     UART1_TxD     |   11  |   12  |    SPI0_CS         |    SPI0_CS          |
|    URXD1            |     UART1_RxD     |   13  |   14  |    SPI0_DOUT       |    SPI0_MO          |
|    SCL4             |     I2C0_SCL      |   15  |   16  |    PCM_FS          |    PCM0_SYNC        |
|    SDA4             |     I2C0_SDA      |   17  |   18  |    PCM_CLK         |    PCM0_CLK         |
|    SCL5             |     I2C1_SCL      |   19  |   20  |    PCM_DO          |    PCM0_DO          |
|    SDA5             |     I2C1_SDA      |   21  |   22  |    PCM_DI          |    PCM0_DI          |
|    EINT16           |     GPIO-A        |   23  |   24  |    GPIO-B          |    EINT5            |
|    EINT4            |     GPIO-C        |   25  |   26  |    GPIO-D          |    EINT3            |
|    EINT2            |     GPIO-E        |   27  |   28  |    GPIO-F          |    EINT1            |
|    DSI_TE           |     GPIO-G        |   29  |   30  |    GPIO-H          |    LCM_RST          |
|    CAM_RST0         |     GPIO-I        |   31  |   32  |    GPIO-J          |    CAM_PDN0         |
|    CAM_RST1         |     GPIO-K        |   33  |   34  |    GPIO-L          |    CAM_PDN1         |
|    VIO18_PMU        |     +1V8          |   35  |   36  |    SYS_DCIN        |    DC_IN            |
|    SYS_5V           |     +5V           |   37  |   38  |    SYC_DCIN        |    DC_IN            |
|    GND              |     GND           |   39  |   40  |    GND             |    GND              |










|  96Boards Signals  |  Helio X20 Signals |  PIN  |  PIN  |  96Boards Signals  |  Helio X20 Signals  |
|:-------------------|:-------------------|:------|------:|-------------------:|--------------------:|
|                    |                    |   1   |   2   |                    |                     |
|                    |                    |   3   |   4   |                    |                     |
|                    |                    |   5   |   6   |                    |                     |
|                    |                    |   7   |   8   |                    |                     |
|                    |                    |   9   |   10  |                    |                     |
|                    |                    |   11  |   12  |                    |                     |
|                    |                    |   13  |   14  |                    |                     |
|                    |                    |   15  |   16  |                    |                     |
|                    |                    |   17  |   18  |                    |                     |
|                    |                    |   19  |   20  |                    |                     |
|                    |                    |   21  |   22  |                    |                     |
|                    |                    |   23  |   24  |                    |                     |
|                    |                    |   25  |   26  |                    |                     |
|                    |                    |   27  |   28  |                    |                     |
|                    |                    |   29  |   30  |                    |                     |
|                    |                    |   31  |   32  |                    |                     |
|                    |                    |   33  |   34  |                    |                     |
|                    |                    |   35  |   36  |                    |                     |
|                    |                    |   37  |   38  |                    |                     |
|                    |                    |   39  |   40  |                    |                     |
