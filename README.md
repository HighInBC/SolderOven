# SolderOven
A control board to turn a toaster oven and a relay into a solder oven

While this is a public project I am not planning on documenting it until it is somewhat ready.

Consider this to be at the pre-alpha development stage. Things **DO NOT WORK** yet.

##Purpose

The purpose of this board is to act as a solder oven control board.
In addition to providing a user interface it will use a relay to control a toaster oven to provide the functionality of a solder oven.

##Features

Not all of these features are functional yet.

###Microcontroller

An ATMEGA328P-AU sits at the heart of the device controlling all of the other components.

###I2C display

Using an I2C port for an external display will allow a wide variety of choices that can be implemented in firmware

###Rotary encoder

A rotary encoder with a push button will be the primary source of user interaction.

###RGB LED

A ws2812b LED will be able to switch to any color or brightness to act as an indicator.

###Buzzer

A small piezo buzzer is used to make audio signals to the user

###Reset button

To reset the unit

###Serial port

The serial port can be used to reprogram the device.
It features an auto reset circuit on the DTR line to mimic the behaviour of an arduino nano but with an external FTDI bpard.

When not being used for programming the port can be used for peripherals such as a wifi bridge or sd card logger.

###Thermocouple sensor

A MAX6675 is used to read and digitize the signal from a type-k thermocouple. Two female 4mm banana plug sockets are on the board for easy connection. This is used to monitor the temperature of the oven.

###External temperature sensor

A port to attach one or more DS18B20 temperature sensors is available. This is used to monitor the temperature of the relay and its housing, further sensors can be added as it is a 1-wire protocol. Has a built in 4.7K pull-up resistor on the data pin for the 1-wire interface.

###Relay output

A port to attach the logic side of a relay to. It is expected that the relay takes a 5V logic level signal and does its own current limiting under 40mA. If your relay needs more than that then you need to add a suitable transistor.

##Associated datasheets

* [ATMEGA382P-AU](http://www.atmel.com/images/Atmel-8271-8-bit-AVR-Microcontroller-ATmega48A-48PA-88A-88PA-168A-168PA-328-328P_datasheet_Complete.pdf)
* [WS2812B](https://cdn-shop.adafruit.com/datasheets/WS2812B.pdf)
* [MAX6675](https://datasheets.maximintegrated.com/en/ds/MAX6675.pdf)
* [DS18B20](https://datasheets.maximintegrated.com/en/ds/DS18B20.pdf)
* [S8050](http://www.gangyi.com.cn/UploadFiles/2007828165749876.pdf)
