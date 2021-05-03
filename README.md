# PCB-Shield-Design
Custom "Shield" Design to be mounted on MicroMod ATP Carrier board seen in Avionics Repo. Here are its [dimensions](https://cdn.sparkfun.com/assets/4/8/6/f/7/MicroMod_ATP_Carrier_Board_Dimensions.png).

## Brainstorm
- Room for sensors (gps, IMU, pressure sensor, temperature sensor, current and voltage readings with balance lead (voltage divider 10k resistor))
- Work Buzzer into board
- Ability to read 8 channels from receiver (maybe up to 16).
- Use Female Headers conneecting boards
- Servos will plug into pin connectors on board (3x8 or 3x16 male header pins).
- Work in SD cards
- [Reverse polarity protection?](https://www.youtube.com/watch?v=IrB-FPcv1Dc)
    - Easy access to USB
    - Voltage regulator (LM338: https://www.ti.com/lit/ds/symlink/lm338.pdf)
    - [P-Channel MOSFET](https://www.mouser.com/Semiconductors/Discrete-Semiconductors/Transistors/MOSFET/_/N-ax1sf?P=1z0z7ptZ1yzxnagZ1z0y3dt&Rl=ax1sfZgjdhp2Z1yw74nrZ1yw78hpSGTax1sfZgjdhp5Z1ys05aaZ1yw8q5sSGT)
    - Consider circuit behavior and power loss at relatively low voltages.
    - Keep servo and avionics power seperate
- Route connections on board to carrier board pins to reduce number of solder connections.
- Mounting holes match
- Decide on dedicated pin usage on carrier board (General I/O, Analog and digital pins, SPI pins, I2C pins).
- use soldered connections for I2C saving qwicc for other devices.
- What types of LEDs do we want on board, quantity, type of LED, will this require any additional componets (e.g. resistor)?
- Add additional sensors (air speed sensor). 
- 3D print a mount for avionics package (modular design).
- Add in DBF logo.
- Label pins

### Componets required
- P-channel mosfet (Manfac. #: IRF????????)
- 0.100" (2.54 mm) Breakaway Male Header: 3×40-Pin, Straight, Black
- LEDs?
- Additional Sensors?
