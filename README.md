# GetMAC

This program will output the MAC address of the ESP32.

## How to Use

Before project configuration and build, be sure to set the correct chip target using `idf.py set-target esp32-s3`.

### Hardware Required

* An ESP32-S3-DevKitC-1 development board
* A USB cable for microcontroller power supply and programming

### Build and Flash
Run `idf.py menuconfig` in the project directory and open the "Lab 4 Example Configuration" menu to configure the peripherals, ensuring that the pin assignments match those in the schematic.

Run `idf.py -p PORT flash monitor` to build, flash and monitor the project.

(To exit the serial monitor, type ``Ctrl-]``.)

See the [Getting Started Guide](https://docs.espressif.com/projects/esp-idf/en/latest/get-started/index.html) for full steps to configure and use ESP-IDF to build projects.

Alternatively, this project can be developed using [VSCode](https://code.visualstudio.com) with the [PlatformIO IDE](https://platformio.org/platformio-ide) extension and the [Espressif 32 platform](https://registry.platformio.org/platforms/platformio/espressif32) installed.

## Example Output

```
ESP-ROM:esp32s3-20210327
Build:Mar 27 2021
rst:0x1 (POWERON),boot:0x2b (SPI_FAST_FLASH_BOOT)
SPIWP:0xee
mode:DIO, clock div:1
load:0x3fce3818,len:0x1750
load:0x403c9700,len:0x4
load:0x403c9704,len:0xc00
load:0x403cc700,len:0x2e04
entry 0x403c9908
I (27) boot: ESP-IDF 5.1.2 2nd stage bootloader
I (27) boot: compile time Feb 14 2024 22:44:35
I (27) boot: Multicore bootloader
I (30) boot: chip revision: v0.1
I (34) boot.esp32s3: Boot SPI Speed : 80MHz
I (38) boot.esp32s3: SPI Mode       : DIO
I (43) boot.esp32s3: SPI Flash Size : 8MB
I (48) boot: Enabling RNG early entropy source...
I (53) boot: Partition Table:
I (57) boot: ## Label            Usage          Type ST Offset   Length
I (64) boot:  0 nvs              WiFi data        01 02 00009000 00006000
I (72) boot:  1 phy_init         RF data          01 01 0000f000 00001000
I (79) boot:  2 factory          factory app      00 00 00010000 00100000
I (87) boot: End of partition table
I (91) esp_image: segment 0: paddr=00010020 vaddr=3c080020 size=1f91ch (129308) map
I (122) esp_image: segment 1: paddr=0002f944 vaddr=3fc96e00 size=006d4h (  1748) load
I (123) esp_image: segment 2: paddr=00030020 vaddr=42000020 size=7d7bch (513980) map
I (220) esp_image: segment 3: paddr=000ad7e4 vaddr=3fc974d4 size=03e40h ( 15936) load
I (224) esp_image: segment 4: paddr=000b162c vaddr=40374000 size=12dc8h ( 77256) load
I (251) boot: Loaded app from partition at offset 0x10000
I (251) boot: Disabling RNG early entropy source...
I (263) cpu_start: Multicore app
I (263) cpu_start: Pro cpu up.
I (263) cpu_start: Starting app cpu, entry point is 0x40375438
I (0) cpu_start: App cpu up.
I (281) cpu_start: Pro cpu start user code
I (281) cpu_start: cpu freq: 160000000 Hz
I (281) cpu_start: Application information:
I (284) cpu_start: Project name:     GetMAC
I (289) cpu_start: App version:      1
I (294) cpu_start: Compile time:     Feb 14 2024 22:43:40
I (300) cpu_start: ELF file SHA256:  e68412e2b1362b5a...
I (306) cpu_start: ESP-IDF:          5.1.2
I (310) cpu_start: Min chip rev:     v0.0
I (315) cpu_start: Max chip rev:     v0.99 
I (320) cpu_start: Chip rev:         v0.1
I (325) heap_init: Initializing. RAM available for dynamic allocation:
I (332) heap_init: At 3FC9EC68 len 0004AAA8 (298 KiB): DRAM
I (338) heap_init: At 3FCE9710 len 00005724 (21 KiB): STACK/DRAM
I (345) heap_init: At 3FCF0000 len 00008000 (32 KiB): DRAM
I (351) heap_init: At 600FE010 len 00001FD8 (7 KiB): RTCRAM
I (358) spi_flash: detected chip: generic
I (362) spi_flash: flash io: dio
I (366) sleep: Configure to isolate all GPIO pins in sleep state
I (373) sleep: Enable automatic switching of GPIO sleep configuration
I (380) app_start: Starting scheduler on CPU0
I (385) app_start: Starting scheduler on CPU1
I (385) main_task: Started on CPU0
I (395) main_task: Calling app_main()
I (425) pp: pp rom version: e7ae62f
I (425) net80211: net80211 rom version: e7ae62f
I (435) wifi:wifi driver task: 3fca8ddc, prio:23, stack:6656, core=0
I (445) wifi:wifi firmware version: 91b9630
I (445) wifi:wifi certification version: v7.0
I (445) wifi:config NVS flash: enabled
I (445) wifi:config nano formating: disabled
I (445) wifi:Init data frame dynamic rx buffer num: 32
I (455) wifi:Init static rx mgmt buffer num: 5
I (455) wifi:Init management short buffer num: 32
I (465) wifi:Init dynamic tx buffer num: 32
I (465) wifi:Init static tx FG buffer num: 2
I (465) wifi:Init static rx buffer size: 1600
I (475) wifi:Init static rx buffer num: 10
I (475) wifi:Init dynamic rx buffer num: 32
I (485) wifi_init: rx ba win: 6
I (485) wifi_init: tcpip mbox: 32
I (485) wifi_init: udp mbox: 6
I (495) wifi_init: tcp mbox: 6
I (495) wifi_init: tcp tx win: 5744
I (495) wifi_init: tcp rx win: 5744
I (505) wifi_init: tcp mss: 1440
I (505) wifi_init: WiFi IRAM OP enabled
I (515) wifi_init: WiFi RX IRAM OP enabled
I (515) phy_init: phy_version 620,ec7ec30,Sep  5 2023,13:49:13
I (565) wifi:mode : sta (f4:12:fa:fa:06:3c)
I (565) wifi:enable tsf
I (565) MAC address: MAC address: f4:12:fa:fa:06:3c
I (665) main_task: Returned from app_main()
```