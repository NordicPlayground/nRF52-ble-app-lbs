# nRF52-ble-app-lbs
Simple example application showing how to do a custom service. Fully explained in nAN-36, available on www.nordicsemi.com.

nrf52-ble-app-lbs
==================
This is the accompanying code for the application note nAN-36: "Creating Bluetooth Low Energy Applications Using nRF51822". It is an implemtation of a simple application that shows a custom service with two characteristics; one for a button and one for a LED. The button characteristic will send a notification with the button state when the button is pressed, while the LED characteristic can be used to control an on-board LED.

Requirements
------------
- nRF52 SDK version 0.9.2
- S132 SoftDevice
- nRF52822 DK (PCA10036 or PCA10040)

The project may need modifications to work with other versions or other boards. 

About this project
------------------
This application is one of several applications that has been built by the support team at Nordic Semiconductor, as a demo of some particular feature or use case. It has not necessarily been thoroughly tested, so there might be unknown issues. It is hence provided as-is, without any warranty. 

However, in the hope that it still may be useful also for others than the ones we initially wrote it for, we've chosen to distribute it here on GitHub. 

The application is built to be used with the official nRF52 SDK, that can be downloaded from https://www.nordicsemi.no, provided you have a product key for one of our kits.

Please post any questions about this project on https://devzone.nordicsemi.com.

How to get started
------------------
1. Clone the repository in the [SDK]/examples/ble_peripheral folder. (Directory structure should now look like [SDK]/examples/ble_peripheral/nrf52-ble-app-lbs).
2. Next either open the Keil project file in .../arm5_no_packs and build or type 'make' in .../armgcc.
3. Flash the s132 softdevice ('make flash_softdevice' command for gcc) and then flash the application ('make flash').
4. Now that the application is running on the nRF52 DK you can either test with one of the following:
  * nRF Blinky [Android](https://play.google.com/store/apps/details?id=no.nordicsemi.android.nrfblinky)
  * Master Control Panel ([Android](https://play.google.com/store/apps/details?id=no.nordicsemi.android.mcp)/[iOS](https://itunes.apple.com/us/app/nrf-master-control-panel-ble/id1054362403?mt=8) or [PC](https://www.nordicsemi.com/eng/nordic/download_resource/38907/28/19937796)).

You will be able to blink the LED on the nRF52 from nRF Blinky or by writing to the LED characteristic in MCP.
You can push Button 1 on the nRF52 DK and see the screen light up in nRF Blinky and see the Button characteristic updated in MCP.
