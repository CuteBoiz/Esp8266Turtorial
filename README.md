# esp8266
MicroPython on ESP8266

## PART 1  GETTING STARTED WITH ESP8266

<img src="https://imgur.com/QLv7y19.jpg" height="400" width="350">

### Step 1 - Install Driver

There 2 kinds of esp8266:
- [CH340](https://sparks.gogo.co.nz/assets/_site_/downloads/CH34x_Install_Windows_v3_4.zip)
- [CP2102](https://www.silabs.com/documents/public/software/CP210x_Universal_Windows_Driver.zip)

*Note: Link download above*

After download and install, you plug-in the ESP and check Device Manage and check which COM the ESP does:

<img src="https://imgur.com/XQ1uemr.png" height="480" width ="203">

Mine case is COM3.

### Step 2 - Get a Firmware

There are many kinds of  Esp8266's firmwares: AT Command, Lua script, microPython, Arduino, ...

In this guide i'll use mircoPython.

**Dowload:** [miroPython](https://micropython.org/download)

### Step 3 - Flashing the Firmmware 

**! Attention:**

Keep in mind that the ESP8266 needs to be ***put in to flash mode*** before you can flash a new firmware!

**Puting Device Into Flash Mode**

- To enable ESP8266 firmware flashing GPIO0 pin must be pulled low before the device is reset. Conversely, for a normal boot, GPIO0 must be pulled high or floating.

- If you have a NodeMCU dev kit then you don't need to do anything, as the USB connection can pull GPIO0 low by asserting DTR and reset your board by asserting RTS.

- If you have an ESP-01 or other device without built-in USB, you will need to enable flashing yourself by pulling GPIO0 low or pressing a "flash" switch, while powering up or resetting the module.


#### NodeMCU Flasher:

**Download:**
[NodeMCU Flasher](https://github.com/nodemcu/nodemcu-flasher)

<ul>
<li><b>Operation Tab</b></li>

In **Operation** tab chose the ESP Port, you can check it at Device Manager:

<img src = "https://i.imgur.com/Km2JFhb.png" height="230" width="470">
<li><b>Config Tab</b></li>

In **Config** Tab chose the firmware we downloaded from **Step 2**:  

<img src ="https://i.imgur.com/F8GMwXI.png" height="230" width="470">

<li><b>Advanced Tab</b></li>

In **Advanced** Tab set the baurdrate to 9600:  

<img src="https://i.imgur.com/LrAB3gg.png" height="230" width="470">

<li><b>Start </b></li>
 Then the last step is start flashing the firmware to ESP:

<img src="https://i.imgur.com/rbCUNjx.png" height="230" width="470">

This will take a while.

</ul>

### Step 4 - Uploading Code

**Download:** [ESPlorer](https://esp8266.ru/esplorer/#download)

