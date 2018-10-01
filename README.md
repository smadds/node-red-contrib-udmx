# node-red-contrib-udmx
A node for outputting DMX through a USB dongle

This node looks for a UDMX dongle with USB ID 16c0:05dc and allows a single DMX channel to be set to a value.

It works with the Chinese usb to DMX adapters readily available (e.g. search ebay for "usb dmx").

![alt text](/assets/usb-dmx-adapter.jpg "Example of USB DMX Adapter")

## Installation
Use the 'Manage Palette' option from the Node-Red admin panel, then search from the 'Install' tab.

If not found, you can install manually:

In your .node-red folder run:
`npm i node-red-contrib-udmx`
then restart the node-red service. 

## Usage

Set msg.topic to the DMX channel (1-512) and msg.payload to the value (0-255).

## Tips
* Restart node-red after inserting dongle to ensure it is detected

## Known Issues
* The dependency node-usb requires a library installing first on linux OS (inc. Raspberry Pi). Full details under Installation here: https://github.com/tessel/node-usb#readme. Be sure to do this before trying to install UDMX. 

* Some distributions do not include pkg-config, which is required by a dependancy. Run `sudo apt install pkg-config` if installation fails and then try again. 

