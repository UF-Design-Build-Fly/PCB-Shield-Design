# PCB-Shield-Design Description
Custom "Shield" Design to be mounted on MicroMod ATP Carrier board seen in Avionics Repo. Here are its [dimensions](https://cdn.sparkfun.com/assets/4/8/6/f/7/MicroMod_ATP_Carrier_Board_Dimensions.png).

## Features v2
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

TOP 3D             |  TOP PCB
:-------------------------:|:-------------------------:
![](https://github.com/UF-Design-Build-Fly/PCB-Shield-Design/blob/main/Figures/PCB/Top_3D.PNG)  |  ![](https://github.com/UF-Design-Build-Fly/PCB-Shield-Design/blob/main/Figures/PCB/Top_PCB.PNG)

BOTTOM 3D             |  BOTTOM PCB
:-------------------------:|:-------------------------:
![](https://github.com/UF-Design-Build-Fly/PCB-Shield-Design/blob/main/Figures/PCB/Bottom_3D.PNG)  |  ![](https://github.com/UF-Design-Build-Fly/PCB-Shield-Design/blob/main/Figures/PCB/Bottom_PCB.PNG)

## v3 Revisions
- Remove unnecessary parts on PCB: JST connectors for battery balance leads, alarm connector, voltage divider for monitoring 1st cell on battery, any useless female connectors that can free up space (e.g. we are not using I2S connectors or any UART but we are using I2C, etc.).
- Remove solder mask on servo PWR and GND. Change trace width to somewhere between 80 and 90 mil. Decide whether custom copper bus bar or a layer of solder will be used to increase the amount of current the traces can carry. Solder can be around 10 times less conductive resulting in greater power loss, but it is the simpler solution (silver solder is only around 5 to 2.5 times less conductive). Copper bus bar is the more complex solution and involves machining or plasma cutting bus bars from sheets of copper and then connecting them to the board with a thin layer of solder for an adequate connection. This solution provides better power delivery and will result in less heat being generated. Or we can just add a wire on top for the pins ```\ ___ :/ ___ /````
- Add connectors for airspeed sensor and voltage/current sensor
- Look at signal connections between receiver and board. Determine what type of molex connector should be used for a secure connection. 
- Decide on dedicated pin usage for PCB. 
- Should the width of the board be increased?
- Correct screw size for 0.1 inch.
- Servo PWR connector should be XT30
- Determine whether or not XT30 connectors should be horizontal and not vertical.
- Change Rfbb resistor (must be between 1k and 10k) on buck converter to a potentiometer. Probably buy a 2k potentiometer with a screw terminal. This allows us to tune the output voltage to 5V.
- Add power LED at Vout of LMZ12002
- Add piezo for sounds?

## Additional Ideas?
- Make another small board to send signals from angle of attack sensor

## Dedicated Pin Usage (e.g. General I/O, Analog and digital pins, SPI pins, I2C pins)
TBD
