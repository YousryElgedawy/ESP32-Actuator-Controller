# ESP32-Actuator-Controller
24V / 20-Channel Actuator Control Board is equipped with an ESP32-S3 and a W5500 Ethernet module for network connectivity, featuring 20 MOSFET-based SSRs to manage actuators along with protection against reverse polarity, overvoltage, short circuits, and ESD.
Board Design Details

- Structure: 4-layer board with a Sig/GND/PWR/Sig stackup, utilizing outer layers for signal traces and inner layers for power distribution.  
* Power Layers: Constructed with 2-ounce copper to handle load currents and withstand high ambient temperatures.  
*Ground Planes:
Layer 2 serves as the main solid GND plane to ensure overall stability. 
Layer 4 features a GND polygon copper pour, functioning as a heat sink and forming a solid ground plane under Layer 3 to create capacitance with the PWR plane. 
A small GND plane is added on Layer 3 over Ethernet and SPI tracks to maintain the same reference plane and minimize impedance mismatch during top-layer routing changes.  
*Power Distribution: Layer 3 incorporates multi-rail polygons for 24V, 5V, and 3.3V supplies.   
Input power polygons are duplicated across layers and connected with stitching vias to support high current demands and minimize temperature rise.  
*High-Speed Signals: Ethernet and SPI signals are routed on the top layer with minimal layer changes, kept as short as possible, and isolated from noise sources including the buck converter, input power connector, and ESP32 antenna, with maximum distance maintained from these sources.   
*RJ45 Connector: Equipped with an internal transformer, Bob-Smith termination, and common-mode choke for optimal signal integrity.   
*SPI Lines: Designed with extremely short traces, maintained at 50-ohm impedance, and implemented with series termination to preserve signal integrity.   
*Power Supply: A cascaded LDO paired with a buck converter delivers a low-ripple power supply to the ESP32.  
*Signal Management: Signal buffers are employed to limit current sourced or sunk by the MCU.  
*Manufacturing Considerations: 
Copper Balance: Meticulously maintained when connecting small components such as 0402 passives to prevent soldering defects such as tombstoning. 
Thermal Relief Polygon Connection: Utilized for high-power through-hole components to enhance solderability.  
*Draftsman PDF: Contains all assembly notes and fabrication notes, specifying complete documentation for manufacturing and assembly processes.  
