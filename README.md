# jsmartsw_hw

This is the hardware repository of the jSmartSW project.

The hardware is consistend of two parts. The jSmartSW mainboard contains the main I/O and logic board. The keypad contains visual feedback interfaces and tactile inputs.

## Main Board

The main board interfaces with and utilizes a Raspberry Pi Pico to run the logic programs of this project. The main board is needed for the project.

The main board has many ports for power and I/O:
- Power
  - DC barrel jack (optional)
  - USB-C jack (optional)
  - Toggle switch for turning the power on/off (optional)
 
- Video & Audio
  - HD15 video/audio passthrough input (optional, suggested): since the project connects to the RetroTink 4K via the HD15 port, you can connect HD15 sources to this port and feed it to the RetroTink 4K.
  - HD15 video passthrough output (optional): the video input from the passthrough input port is output from this port. The serial control commands are sent from this port to the RetroTink 4K if a USB-C connection is not present to the RetroTink 4K.
  - 3.5mm TRS barrel jack: audio signal input from the passthrough input pin 12 & 15 is broken out to this port, so you can use a 3.5mm TRS audio cable and feed it to the RetroTink 4K.

- Communication
  - 2x4 right-angle pin header: communicates with the gSCARTsw.
  - 2x7 right-angle pin header (optional): communicates with the optional keypad.
  - HD15 video passthrough output (already listed): The serial control commands are sent from this port to the RetroTink 4K if a USB-C connection is not present to the RetroTink 4K.
  - USB-C jack (already listed): When connected to the RetroTink 4K, it will become the preferred channel of communication. It also supplies power into the RetroTink 4K. In this case, the 5V barreljack must be populated as the main source of power.
  
