## PS2-PSU
The PS2-PSU is a custom regulator solution meant for powering Playstation 2 Slims that have had an Advanced Trim performed to them or untrimmed consoles with the existing power regulatory components removed.

<img width="822" alt="3DViewer" src="https://github.com/user-attachments/assets/b0e5cb3e-046a-427d-a615-5890939e0214">
<img width="822" alt="PCBNew" src="https://github.com/user-attachments/assets/ab8a14c8-f090-4cd7-b6ce-b54954423bfc">

## Disclaimer
This is **NOT** a "drop-in" power regulator solution for portable PS2's. This board is meant to **only** be powered externally via USB-C and should not be powered by a battery. It is meant to power PS2's that have been trimmed and require the [Advanced Trim voltage relocations](https://bitbuilt.net/forums/index.php?threads/the-definitive-ps2-trimming-guide.1841/); or PS2's that have had their existing power regulating components removed. This board has only been tested with a SCPH-79001 motherboard so far but should work with any SCPH-7900X PS2 Slim; or any Playstation 2 Slim that requires the necessary voltages. Revision 2 is planned to be a full "drop-in" solution to use for portables in conjunction with a separate battery protection PCB and will be released soon.

This board has **only** been tested with the [Adafuit 5803](https://www.mouser.ca/ProductDetail/Adafruit/5803?qs=QpmGXVUTftHXtVI1Nl%252BHoQ%3D%3D) 5V 4A output wall adapter outlined in the BOM but any USB-C charger should work as long as it can output at least 3A or more. It is also **strongly** recommended to only use 5V to power this board as the main TPS62A06DRLR regulators have a maximum input voltage rating of 5.5v and anything higher can and will have the potential to damage the components.

## Features
- Board Dimentions: 61mm x 25mm
- Powered via USB-C
- Uses more standard voltages and 1 less regulator as opposed to the voltages recommended in the PS2 Trimming Guide

## Gallery
![BoardTop](https://github.com/user-attachments/assets/9c9a4870-eda5-4197-b197-5a938f0c5fd9)![BoardBottom](https://github.com/user-attachments/assets/164fabf6-fbaa-4148-8643-a7400b846164)![WiredTop](https://github.com/user-attachments/assets/1923f9f9-16a5-4cd4-8d63-630d0b483fd3)![Boot](https://github.com/user-attachments/assets/849f347e-a979-4fd5-982b-d555fe61994a)

## Order & Assembly
- The gerber files can be uploaded to any PCB manufacturer of your choice for ordering
- While it is recommended to order this board with an ENIG surface finish, a HASL(with lead) finish will work as well
- It is **strongly** recommended to order a stencil for assembly and it is not recommended to hand solder the components
- There are 3 BOM file types included: a .xlsx BOM, a .pdf BOM and an iBOM.html
- The Bill of Materials for this board were ordered from Mouser however components can be ordered from the supplier of your choice so long as they are stocked. links to a supplier were left out in the BOM for users who may prefer a different supplier
- As per the disclaimer, the Adafruit 5803 outlined in the BOM is recommended for not only its voltage and amperage output, but it also has an external switch to utilize as the board will be powered once plugged in if not using an external switch

## Installation
Whereas the PS2-PSU uses more standard voltages than the those outlined in the [Definitive PS2 Trimming Guide](https://bitbuilt.net/forums/index.php?threads/the-definitive-ps2-trimming-guide.1841/), the connections are as follows:

- 1V on the PSU is required to be connected to the PS2's 1.25V area
- 1V8 on the PSU is required to be connected to **BOTH** the PS2's 1.75V **and** 2.5V areas
- 3V3 on the PSU is required to be connected to the PS2's 3.5V area
- 5V on the PSU is required to be connected to the PS2's 5V area

**Please note that all volatge relocations MUST be connected together on a trimmed PS2 as trimming cuts away the internal voltage layers that connects them together**

SCPH-79001 and alike (please note that the 2 8-pin IC's circled in red must be removed if they are present) ![Voltage_79001](https://github.com/user-attachments/assets/30253d28-cfe3-46c3-a2ba-7ce2b801d5b4)

SCPH-79003 and alike ![Voltage_79003](https://github.com/user-attachments/assets/a4515860-1464-4abe-9413-073ab2beb19c)

When using this PSU or any custom regulator solution to externally power a PS2, 3.5V (or 3V3) must be reconnected to this area on the 8-pin ic. If the 8-pin ic is not present, 3.5v (or 3V3) must be connected to the small capacitor above it 

![Voltage Relocation Back 79001_for PS2PMS](https://github.com/user-attachments/assets/8a2c9dfe-d5f6-4eba-8295-a256878574cd)

5V **must** be connected to the orange area in this photo as it powers both the DAC and the Ethernet IC and is a requirement for the PS2 to boot ![Video_Bottom](https://github.com/user-attachments/assets/3b70c36d-0a91-4fd8-ba82-9969246ad2db)


## License
[Solderpad Hardware License v2.1](https://solderpad.org/licenses/SHL-2.1/)




