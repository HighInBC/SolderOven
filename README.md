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
It features an auto reset circuit on the DTR line to mimic the behaviour of an arduino nano but with an external FTDI chip.

When not being used for programming the port can be used for peripherals such as a wifi bridge or sd card logger.

###Thermocouple sensor

A MAX6675 is used to read and digitize the signal from a type-k thermocouple. Two female 4mm banana plug sockets are on the board for easy connection. This is used to monitor the temperature of the oven.

###External temperature sensor

A port to attach a DS18B20 temperature sensor is available. This is used to monitor the temperature of the relay and its housing. Has a built in 4.7K pull-up resistor on the data pin for the 1-wire interface.

###Relay output

A port to attach the logic side of a relay to. It is expected that the relay takes a logic level signal and does its own current limiting under 40mA.
