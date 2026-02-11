# ESPHome-bed-presence-sensor
Smart Bed Presence Sensor (Thread Ready) An intelligent bed presence sensor based on the ESP32-C6 microcontroller. The device uses strain gauges (FSR or similar) to separately monitor the two halves of the bed.

**Features**

• ESP32-C6 & OpenThread: Support for the modern Thread protocol for stable and energy-efficient operation in the smart home ecosystem.

• Dual-zone monitoring: Separate sensors for the left and right sides of bed.

• Dynamic configuration: Response thresholds and delays (false alarm filtering) are configurable directly from Home Assistant without re-flashing the firmware.

• Smart filtering: Using a moving average (sliding_window_moving_average) to smooth out ADC noise.

**Connection diagram**
The sensors are connected to the ESP32-C6 analog (ADC) pins. The current configuration uses:
• Right side: GPIO1
• Left side: GPIO6

**Note:** For operation of tape type strain gauges, it is recommended to use a voltage divider circuit with a resistor (usually 10kOhm).
