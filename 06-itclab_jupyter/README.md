# iTCLab Jupyter Heat Monitoring and Controlling System
A jupyter based application to explore different control techniques of a simple temperature plant

**Overview**

This code was written to showcase an Arduino based Temperature Control Lab (https://apmonitor.com/pdc/index.php/Main/ArduinoTemperatureControl) for a Lecture on Advanced Control Techniques.

The iTCLab system is built with two temperature sensors and two heaters. A Matlab or Python interface is provided to read the temperature data from the board and control the heaters power output. Two classes were created, one that aims to control the Arduino System (**control_arduino.py**) and another one replacing the Arduino interface with a simulator (**control_demo.py**), so the app can be used without the real hardware, as a demonstration.

This project implements four different control techniques (Manual, On-Off, PID and MPC) so the user can test and visualize the differences between them.

There is also a configurations window that presents some parameters that can be adjusted for the whole simulation or for each control technique.

The interface was build using ipywidgets and bqplot. The dynamic plant simulation is done using scipy `odeint` function, whilst the MPC is implemented using the gekko library. For more information regarding the MPC options refer to the gekko documentation (https://gekko.readthedocs.io/en/latest/).

**Dependencies**
- numpy
- scipy
- ipywidgets (https://github.com/jupyter-widgets/ipywidgets)
- bqplot==0.11.9 (https://github.com/bloomberg/bqplot)
- gekko (https://github.com/BYU-PRISM/GEKKO)
- tclab (only for the control_arduino.py)

**Documentation**
