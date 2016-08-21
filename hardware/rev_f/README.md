Warning, this board revision has faults. Do not order.


Ordered from OSHPark for testing on 2016-08-05

Received and assembled August 8th, 2016. Results:

The following hardware features work correctly:

- ATMEGA328P-AU MCU
- Auto-program over serial port arduino nano style using external FTDI board
- WS2812B LED
- Buzzer
- Thermocouple reading
- Rotary encoder/button
- Reset button
- I2C display
- Relay ouput
- Power input

Errors on board:

- Mounting holes are too crowded and too close to the edges. Have to expand board size
- The DS18B20 is attached to ADC6, this port is only for analog reading and cannot control the port. Next revision has this moved to PD5
