ArRPi
=====

Mock project to test Raspberry Pi and Arduino connection. It installs a server into the RPi and allow users to interact with sensors connected to an Arduino board.

ArRPi uses a lightweight server Flask.

[Prerrequisites]

We create a virtualenv and need to install the packages virtualenv and virtualenvwrapper.

mkvirtualenv <environment>

To work on that environment, we use

workon <environment>

Inside the environment, some tools are installed:

pip install flask
pip install pyserial

[For Arduino]

Just need to upload the ArRPi.ino to your Arduino. In the code, a LED lights up during 3 seconds when the Arduino reads a number '1' throught its serial port.

No dependencies are required.

[For RaspberryPi]

In order to print throught the serial, we need to install the pyserial library:

pip install pyserial

The server Flask is used. It is a lightweight server for RaspberryPi. It should be installed with

pip install flask


[First tests]

In order to test if everything is working, first of all the Arduino is connected to the RaspberryPi. The serial port is detected using the command "ls /dev/" before and after connecting the Arduino. With "diff dev.txt dev1.txt" the current port is shown.

To play with it, python terminal should be launched and the next code written:

>>> import serial
>>> s = serial.Serial("/dev/<port>", 9600)
>>> s.write('1')

When writing a '1' into the Arduino board, we can see the LED in the input #13 turns on during 3 seconds.

[Testing the server]
