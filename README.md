# node-red-contrib-udmx
A node for outputting DMX through a USB dongle

This node looks for a UDMX dongle with USB ID 16c0:05dc and allows a single DMX channel to be set to a value.

It works with the Chinese usb to DMX adapters readily available (e.g. search ebay for "usb dmx").

![alt text](/assets/usb-dmx-adapter.jpg "Example of USB DMX Adapter")

Set msg.topic to the DMX channel (1-512) and msg.payload to the value (0-255).

Restart node-red after inserting dongle to ensure it is detected
