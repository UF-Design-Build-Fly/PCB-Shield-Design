# PCB-Shield-Design
Custom "Shield" Design to be mounted on MicroMod ATP Carrier board seen in Avionics Repo. Here are its [dimensions](https://cdn.sparkfun.com/assets/4/8/6/f/7/MicroMod_ATP_Carrier_Board_Dimensions.png).

## Brainstorm
- Room for sensors (gps, IMU, pressure sensor, temperature sensor, current and voltage readings)
- Ability to read 8 channels from receiver (maybe up to 16).
- Servos will plug into pin connectors on board (3x8 or 3x16 male header pins).
- [Reverse polarity protection?](https://www.youtube.com/watch?v=IrB-FPcv1Dc)
    - Do we want avionics package to act only as a load or do we want the ability to debug board using serial monitor while reading pwm.
    - [P-Channel MOSFET](https://www.mouser.com/Semiconductors/Discrete-Semiconductors/Transistors/MOSFET/_/N-ax1sf?P=1z0z7ptZ1yzxnagZ1z0y3dt&Rl=ax1sfZgjdhp2Z1yw74nrZ1yw78hpSGTax1sfZgjdhp5Z1ys05aaZ1yw8q5sSGT)
    - Optimize parameters for MOSFET in application
    - fuse?
    - Powered by 5.5 V or more? Should we consider a higher voltager considering a voltage drop across drain to source.
    - Consider circuit behavior and power loss at relatively low voltages.
- Do we just want male to female header pins on the side and a bunch of solderable holes on the rest of the board?
- Mount will connect to carrier board through long male male pins at the bottom. Will have female pins on the top.
- Route connections on board to carrier board pins to reduce number of solder connections.
- Add additional mounting holes in corners of board?
- Decide on dedicated pin usage on carrier board (General I/O, Analog and digital pins, SPI pins, I2C pins).
- Decide on whether to use pins for I2C using Qwicc connect or soldered connections. 
- What types of LEDs do we want on board, quantity, type of LED, will this require any additional componets (e.g. resistor)?
- Do we want to add additional sensors?
- Considerations in code. Are we going to use interrupts for any sensors? 
- Do we want to 3D print a mount for avionics package? Should the receiver have a box to be placed in? How compact?
- Add in DBF logo for good measure.

### Componets required
- P-channel mosfet (Manfac. #: IRF????????)
- 0.100" (2.54 mm) Breakaway Male Header: 3×40-Pin, Straight, Black
- LEDs?
- Additional Sensors?
