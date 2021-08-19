# PCB-Shield-Design Description
Custom "Shield" Design to be mounted on MicroMod ATP Carrier board seen in Avionics Repo. Here are its [dimensions](https://cdn.sparkfun.com/assets/4/8/6/f/7/MicroMod_ATP_Carrier_Board_Dimensions.png).

## Features
- Sensors on board: IMU, pressure, temperature, voltage, current, airspeed. 
- 3 pin connectors for servos. 
- PWM signals from receiver are wired to the board and routed to the servos.
- Female headers will connect the shield to the carrier board (stacking boards).
- PWM signals will be wired to I/O pins to be read and logged.
- Micro SD will be used for data logging.
- Power for avionics and servos will be separate.
- Step down buck converter will be used to regulate a 5V supply voltage on the board (5V will also be fed to VIN for carrier board to be stepped down to 3.3V).
- Mounting holes on corners of the board (100 mil diameter).
- 2 LED light indicators to communicate state of device.

### Dedicated Pin Usage (e.g. General I/O, Analog and digital pins, SPI pins, I2C pins)
TBD
