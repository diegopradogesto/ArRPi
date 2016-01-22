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
