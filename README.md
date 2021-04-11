# PCB-Shield-Design
Custom "Shield" Design to be mounted on MicroMod ATP Carrier board seen in Avionics Repo.

## Brainstorm
- Room for sensors (gps, IMU, pressure sensor, temperature sensor, current and voltage readings)
- Ability to read 8 channels from receiver (maybe up to 16).
- Servos will plug into pin connectors on board (3x8 or 3x16 male header pins).
- [Reverse polarity protection?](https://www.youtube.com/watch?v=IrB-FPcv1Dc)
    - Do we want avionics package to act only as a load or do we want the ability to debug board using serial monitor (voltage source from computer).
    - P-Channel MOSFET
    - Optimize parameters for MOSFET in application
    - fuse?
    - Powered by 5.5 V or more? Should we consider a higher voltager considering a voltage drop across drain to source.
    - Consider circuit behavior and power loss at relatively low voltages.
- Mount will connect to carrier board through long male male pins at the bottom. Will have female pins on the top.
- Route connections on board to carrier board pins to reduce number of solder connections.
- Add additional mounting holes in corners of board?
- Decide on dedicated pin usage on carrier board (General I/O, Analog and digital pins, SPI pins, I2C pins).
- Decide on whether to use pins for I2C using Qwicc connect or soldered connections. 
- What types of LEDs do we want on board, quantity, type of LED, will this require any additional componets (e.g. resistor)?
- Do we want to add additional sensors?
- Considerations in code. Are we going to use interrupts for any sensors? 
- Do we want to 3D print a mount for avionics package? Should the receiver have a box to be placed in? How compact?

## Componets required
- P-channel mosfet (Manfac. #: IRF????????)
- 3x40 male header pins
- LEDs?
- Additional Sensors
