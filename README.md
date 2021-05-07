# PCB-Shield-Design
Custom "Shield" Design to be mounted on MicroMod ATP Carrier board seen in Avionics Repo. Here are its [dimensions](https://cdn.sparkfun.com/assets/4/8/6/f/7/MicroMod_ATP_Carrier_Board_Dimensions.png).

## Requirements
- Sensors on board: IMU and pressure sensor. Current sensor will be hooked up inline with lipo batteries and the appropiate wires will be fed to the board. Voltage readings from battery will be read from the balance lead using voltage divider (10k resistors) - only one cell will be read. GPS will be mounted in electronics module and not on the board as it will be wired using qwicc connect.
- Voltage alarm buzzer will be hooked into board inline with the balance lead.
- Female headers will be used to connect the shield to the carrier board.
- Ability to read 8 channels from receiver.
- Servos will plug into pin connectors on board (3x8).
- micro SD card holder will be mounted on the board
- [Reverse polarity protection](https://www.youtube.com/watch?v=IrB-FPcv1Dc) will be incorporated into the design.
    - Voltage regulator :[LM338T/NOPB](https://www.ti.com/lit/ds/symlink/lm338.pdf?HQS=dis-dk-null-digikeymode-dsf-pf-null-wwe&ts=1620410292369)
    - Find linear voltage regulator at this [website](https://www.digikey.com/en/products/filter/pmic-voltage-regulators-linear/699?s=N4IgjCBcpgTAnFUBjKAzAhgGwM4FMAaEAeygG1wA2AdgFZ4AWEIsAZjFveZFgAYPGIALpEADgBcoIAMriATgEsAdgHMQAXyKxatJCFSRMuQiXIhWADnj9ERS9dZMRICVNmLVGorWqs9Bo3wiUkgKagZaDm4LamowC254bQRo%2BDBYxPDePxZs2gZYbjBeGIKiuEpeXRYwSlpeW3AGS2yiyKsElnpYBmoiyjAGdP7HOP66cKKLCPhO8EZppi0OViqi4TFJSBl5ZTVNcF46-3RsINNQ8A2XLZAASSVxPBU8OS8mlOh9U%2BNgsx60mMtKtrHNYKs6pRuOCOLxeND2NpqjxWD1eH1gasLFDMbQaAihrwlij7PDgREyloaBFClpIoNkdo4L5oZxYGxoRYKoy4qx4DkeNMOLTBQwucSENR4ECQHVpRjZZR2ArqJQCo0LKt2YlkhqLBYjpkGK1cqx8iLZgxKI1ZpRKHNiqURYMWn5nK5tu49u8ALSFL4GeQAVxMIQouiE6ijQA)
    - [P-Channel MOSFET](https://www.mouser.com/Semiconductors/Discrete-Semiconductors/Transistors/MOSFET/_/N-ax1sf?P=1z0z7ptZ1yzxnagZ1z0y3dt&Rl=ax1sfZgjdhp2Z1yw74nrZ1yw78hpSGTax1sfZgjdhp5Z1ys05aaZ1yw8q5sSGT)
    - Consider circuit behavior and power loss
    - Keep servo and avionics power SEPERATE
- Keep easy access to the USB for debugging
- Mounting holes on shield and carrier board must match
- What types of LEDs do we want on board, quantity, type of LED, will this require any additional componets (e.g. resistor)?
- Add LEDs onto board (most likely 2) and current limiting resistors
- Add additional sensors (air speed sensor)
- 3D print a mount for avionics package (modular design)
- Add in DBF logo
- Label pins (silk screen)

### Dedicated Pin Usage (e.g. General I/O, Analog and digital pins, SPI pins, I2C pins)
TBD

### Componets required
- P-channel mosfet (Manfac. #: IRF????????)
- 0.100" (2.54 mm) Breakaway Male Header: 3×40-Pin, Straight, Black
- LEDs?
- Additional Sensors?
