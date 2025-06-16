# TC3Controller
This is a controller board for three K-type thermocouples. In addition to the standard components, it contains:
- three MAX31855KASA thermocouple amplifiers
- optional filtering capacitors on thermocouple inputs
- three 2-terminal 2.54mm pitch screw terminals for thermocouples
- STATUS and FAULT LEDs
The board itself is 35.0mm x 37.3mm and uses M2 mounting holes.

We considered designing our own thermocouple amplifier to save cost, but decided not to. If necessary, this could be implemented as follows:
- Using a low noise amplifier such as the LMP7716MMX/NOPB (dual), produce a desired gain with feedback.
- Use another amplifier device, likely in the same dual package, to buffer a resistor divider and offset the voltage to allow reading of temperatures below the cold junction temperature.
- Separately, connect a temperature sensor such as the TMP126EDBVRQ1 and perform cold junction compensation in software.
Cold junction compensators and buffers could be reused between individual thermocouples.
