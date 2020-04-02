# Tronxy X1 earl working version 0.92 

This is based on Marlin Tronxy X1 version 0.92 firmware file that I have been editing (taken from the original version by Bram den Ouden) - trying to get Hot Bed to work but I think my thermistor tables are wrong. As a result, I am trying to also fork pessimism's Marlin version 2 firmware version, but so far I cannot get it to compile as it says that the configuration.h file "#error "You are using an old Configuration.h file, update it before building Marlin."" (but that is another version). 

Known issues:
If you try and start  another print without a full cool down it throws an error.
Cannot successfully add a hot bed

I have tried to use all the thermistor options on the bed but cannot find an option that matches my ebay thermistor correctly and I get errors on heat up that stop the print and show as an out of temparature scope error on the screen etc.

The thermistor was described as: -
Ebay hotbed thermister
3D Printer 100K Wired NTC Thermistor reprap hot end prusa gregs extruder

Here are my PID tests:

Bed temp
153.7 ohms at about 10 Deg
171k ohm atfirst test PID settings

Recv:  bias: 79 d: 79 min: 147.58 max: 152.56
Recv:  Ku: 20.23 Tu: 71.20
Recv:  Classic PID
Recv:  Kp: 12.14
Recv:  Ki: 0.34
Recv:  Kd: 108.03
Recv: Info:PID Autotune finished ! Place the Kp, Ki and Kd constants in the
_________________________________________________

second pass

Recv:  bias: 117 d: 117 min: 210.58 max: 219.97
Recv:  Ku: 15.87 Tu: 70.78
Recv:  Classic PID
Recv:  Kp: 9.52
Recv:  Ki: 0.27
Recv:  Kd: 84.23
_________________________________________________
Third pass

Recv:  bias: 117 d: 117 min: 210.72 max: 219.79
Recv:  Ku: 16.43 Tu: 70.75
Recv:  Classic PID
Recv:  Kp: 9.86
Recv:  Ki: 0.28
Recv:  Kd: 87.15
Recv: Info:PID Autotune finished ! Place the Kp, Ki and Kd constants in the Configuration.h or EEPROM
_________________________________________________ 

freezing
159 at freezing
130 at 19 Deg
About1k ohm on soldering iron, maybe 190 Deg
320k at 0
250k ohm at 3
200k at 5 deg
117.5k ohms at 17 deg95
120k ohm at 19 Deg
110k ohm at 20 Deg QQ
86k ohms at 27 Deg
66.6k ohms at 29 Deg
79.5 ohms at 29 Deg
54k at 38 deg
36k at 49 Deg
_____________________________________________
Below calculated values......
Resistance 1 (Ω)
250000
Resistance 2 (Ω)
36000
Temperture 1 (°C)
3
Temperature 2 (°C)
49
β (K)
3,747.88
______________________________________________________

Resistance 1 (Ω)
320000
Resistance 2 (Ω)
36000
Temperture 1 (°C)
0
Temperature 2 (°C)
49
β (K)
3,923.52
________________________________________________________


