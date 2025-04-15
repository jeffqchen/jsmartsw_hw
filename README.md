# jsmartsw_hw

This is the hardware repository of the jSmartSW project.

The hardware is consistend of two parts. The jSmartSW mainboard contains the main I/O and logic board. The keypad contains visual feedback interfaces and tactile inputs.

Detailed building guides and technical details are documented in the project wiki pages.

## Primary Parts

### Main Board

The main board interfaces with and utilizes a Raspberry Pi Pico to run the logic programs of this project. The main board is needed for the project.

The main board has many ports for power and I/O:
- **Power**
  - **DC 5V barrel jack** (optional)

    The preferred source to power jSmartSW.
    
  - **USB-C jack** (optional)
 
    USB functionality is provided via this port. You can also power the jSmartSW from this port.

  - **Toggle switch** (optional)
    
    For turning the power from the barrel jack and USB-C jack on or off.
    
 
- **Video & Audio**
  - **HD15 video/audio passthrough input** (optional, recommended):
    
    Since the project communicates to the RetroTink 4K primarily via the HD15 port, you can connect HD15 sources to this port and feed it to the RetroTink 4K.
    
  - **HD15 video passthrough output** (optional):
    
    The video input from the passthrough input port is output from this port. The serial control commands are sent from this port to the RetroTink 4K if a USB-C connection is not present to the RetroTink 4K.
    
  - **3.5mm TRS barrel jack**:
    
    Audio signal input from the passthrough input pin 12 & 15 is broken out to this port, so you can use a 3.5mm TRS audio cable and feed it to the RetroTink 4K.
    

- **Communication**
  - **2x4 right-angle pin header**:
  
    Communicates with the gSCARTsw.
    
  - **2x7 right-angle pin header** (optional):

    Communicates with the optional keypad.
    
  - **HD15 video passthrough output** (already listed):

    The serial control commands are sent from this port to the RetroTink 4K if a USB-C connection is not present to the RetroTink 4K.
    
  - **USB-C jack** (already listed):

    When connected to the RetroTink 4K, it will become the preferred channel of communication. It also supplies power into the RetroTink 4K. In this case, the 5V barreljack must be populated as the main source of power.

### Keypad

The keypad is the primary user interface of jSmartSW. It has a screen, addressable RGB LEDs, and 8 key switches.

- Screen

  A 0.91 inch OLED SSD1306 screen at 128x32 resolution.

- 16 (8x2) WS2812b OR WS2812b 2020 addressable RGB LEDs.

  An array of addressabvle RGB LEDs for indicating device running state and prodiving visual assistance.
  
- 8 Cherry MX keyboard switches

  An array of keyboard switches for controlling functionalities of jSmartSW.

- Keypad Faceplate Panel

  Cosmetic face panel with markings. Markings will be illuminated by the RGB LEDs.

- 3D printed Keypad body shell & light shrould
