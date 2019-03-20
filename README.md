## Steps to get setup

1. Copy tools/aws_config_quick_start/configure.json.templ to 
        tools/aws_config_quick_start/configure.json and fill it out.

2. Copy demos/espressif/esp32_devkitc_esp_wrover_kit/make/sdkconfig.templ to
        demos/espressif/esp32_devkitc_esp_wrover_kit/make/sdkconfig

3. Copy demos/common/include/aws_clientcredential.h.templ to
        demos/common/include/aws_clientcredential.h

4. Copy demos/common/include/aws_clientcredential_keys.h.templ to
        demos/common/include/aws_clientcredential_keys.h

## Steps to run

Reference: https://docs.aws.amazon.com/freertos/latest/userguide/getting_started_espressif.html

### SETUP

1. If not starting from scratch, you might have to delete (using the IoT Core Web Console)
  - IoT Things
  - Policies
  - Certificates

2. Checkout this repository and run the above 'Steps to get setup'

3. Update tools/aws_config_quick_start/configure.json

4. Ensure the afr_source_dir is set to the full path on your computer

5. Make sure you’re signed in to the AWS command line tool for the next step (using ‘aws configure’ and enter AWS Access Id and Secret Key)

6. Run ‘python SetupAWS.py setup’ from tools/aws_config_quick_start/

7. This should create certificates and register the device with Amazon IOT

### Running

1. If you’re debugging, you can subscribe to a MQTT Topic
2. Run make menuconfig from <BASE_FOLDER>/demos/espressif/esp32_devkitc_esp_wrover_kit/make
3. Configure stuff
4. Run make flash monitor from same folder

### If everything’s working already and you’re just changing WIFI

1. You should be able to just edit aws_clientcredential.h




## Getting Started

For more information on Amazon FreeRTOS, refer to the [Getting Started section of Amazon FreeRTOS webpage](https://aws.amazon.com/freertos).

To directly access the **Getting Started Guide** for supported hardware platforms, click the corresponding link in the Supported Hardware section below.

For detailed documentation on Amazon FreeRTOS, refer to the [Amazon FreeRTOS User Guide](https://aws.amazon.com/documentation/freertos).

## Supported Hardware

The following MCU boards are supported for Amazon FreeRTOS:
1. **Texas Instruments** - [CC3220SF-LAUNCHXL](http://www.ti.com/tool/cc3220sf-launchxl).
    * [Getting Started Guide](https://docs.aws.amazon.com/freertos/latest/userguide/getting_started_ti.html)
    * IDEs: [Code Composer Studio](http://www.ti.com/tools-software/ccs.html), [IAR Embedded Workbench](https://www.iar.com/iar-embedded-workbench/partners/texas-instruments)
2. **STMicroelectronics** - [STM32L4 Discovery kit IoT node](http://www.st.com/en/evaluation-tools/b-l475e-iot01a.html).
    * [Getting Started Guide](https://docs.aws.amazon.com/freertos/latest/userguide/getting_started_st.html)
    * IDE: [STM32 System Workbench](http://openstm32.org/HomePage)
3. **NXP** - [LPC54018 IoT Module](http://www.nxp.com/LPC-AWS-Module).
    * [Getting Started Guide](https://docs.aws.amazon.com/freertos/latest/userguide/getting_started_nxp.html)
    * IDEs: [IAR Embedded Workbench](https://www.iar.com/iar-embedded-workbench/partners/nxp), [MCUXpresso IDE](https://www.nxp.com/mcuxpresso/ide/download)
4. **Microchip** - [Curiosity PIC32MZEF](http://www.microchipdirect.com/product/search/all/dm320104-BNDL).
    * [Getting Started Guide](https://docs.aws.amazon.com/freertos/latest/userguide/getting_started_mch.html)
    * IDE: [MPLAB X IDE](http://www.microchip.com/mplab/mplab-x-ide)
5. **Espressif** - [ESP32-DevKitC](https://www.espressif.com/en/products/hardware/esp32-devkitc/overview), [ESP-WROVER-KIT](https://www.espressif.com/en/products/hardware/esp-wrover-kit/overview).
    * [Getting Started Guide](https://docs.aws.amazon.com/freertos/latest/userguide/getting_started_espressif.html)
6. **Infineon** - [Infineon XMC4800 IoT Connectivity Kit](https://www.infineon.com/connectivitykit)
    * [Getting Started Guide](https://docs.aws.amazon.com/freertos/latest/userguide/getting_started_infineon.html)
    * IDE: [DAVE](https://infineoncommunity.com/dave-download_ID645)
7. **Xilinx** - [Xilinx Zynq-7000 based MicroZed Industrial IoT Bundle](http://www.zedboard.org/product/microzed-iiot-bundle-afreertos)
    * [Getting Started Guide](https://docs.aws.amazon.com/freertos/latest/userguide/getting_started_xilinx.html)
    * IDE: [Xilinx SDK](https://www.xilinx.com/products/design-tools/embedded-software/sdk.html)
8. **MediaTek** - [MediaTek MT7697Hx Development Kit](https://www.mediatek.com/products/smartHome/mt7697h)
    * [Getting Started Guide](https://docs.aws.amazon.com/freertos/latest/userguide/getting_started_mediatek.html)
    * IDE: [Keil uVision](http://www2.keil.com/mdk5/install/)
9. **Renesas** - [Renesas Starter Kit+ for RX65N-2MB](https://www.renesas.com/us/en/products/software-tools/boards-and-kits/renesas-starter-kits/renesas-starter-kitplus-for-rx65n-2mb.html)
    * [Getting Started Guide](https://docs.aws.amazon.com/freertos/latest/userguide/getting_started_renesas.html)
    * IDE: [e2 studio](https://www.renesas.com/us/en/products/software-tools/tools/ide/e2studio.html)
10. **Cypress CYW54907** - [Cypress CYW954907AEVAL1F Evaluation Kit](https://www.cypress.com/documentation/development-kitsboards/cyw954907aeval1f-evaluation-kit)
    * [Getting Started Guide](https://docs.aws.amazon.com/freertos/latest/userguide/getting_started_cypress_54.html)
    * IDE: [WICED Studio](https://community.cypress.com/community/wiced-wifi)
11. **Cypress CYW43907** - [Cypress CYW943907AEVAL1F Evaluation Kit](https://www.cypress.com/documentation/development-kitsboards/cyw943907aeval1f-evaluation-kit)
    * [Getting Started Guide](https://docs.aws.amazon.com/freertos/latest/userguide/getting_started_cypress_43.html)
    * IDE: [WICED Studio](https://community.cypress.com/community/wiced-wifi)
12. **Windows Simulator**
To evaluate Amazon FreeRTOS without using MCU-based hardware, you can use the Windows Simulator.
* Requirements: Microsoft Windows 7 or newer, with at least a dual core and a hard-wired Ethernet connection
* [Getting Started Guide](https://docs.aws.amazon.com/freertos/latest/userguide/getting_started_windows.html)
* IDE: [Visual Studio Community Edition](https://www.visualstudio.com/downloads/)
