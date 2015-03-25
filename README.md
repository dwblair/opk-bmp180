# opk-bmp180

Hardware connections:

- (GND) to GND
+ (VDD) to 3.3V

(WARNING: do not connect + to 5V or the sensor will be damaged!)

You will also need to connect the I2C pins (SCL and SDA) to your
Arduino. The pins are different on different Arduinos:

Any Arduino pins labeled:  SDA  SCL
Uno, Redboard, Pro:        A4   A5
Mega2560, Due:             20   21
Leonardo:                   2    3


Try it:

- Upload 'pressure.ino' to Arduino
- Allow pull command to be executed:  'chmod 755 ./pull'
- ./pull -p /dev/ttyUSB0 
- Yields JSON packet: {"temp_Celsius": 23.41 ,"pressure_mb": 1025.69 }
