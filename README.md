* ESP8266 mqtt node

#### Server ####
- mqtt broker : mosquitto
- db : influxdb
- web : grafana, node-red
- collect : mqtt2graphite
- alert : mqttwarn 


### Library ###
- https://github.com/knolleary/pubsubclient
- https://github.com/milesburton/Arduino-Temperature-Control-Library
- https://github.com/adafruit/DHT-sensor-library
- https://github.com/bogde/HX711
- https://github.com/Makuna/Rtc
- LiquidCrystal_I2C.h
- https://github.com/openenergymonitor/EmonLib
- https://github.com/bblanchon/ArduinoJson
- https://github.com/MajenkoLibraries/Average
- https://github.com/Yveaux/arduino_vcc
- https://github.com/PaulStoffregen/Time
- https://github.com/z3t0/Arduino-IRremote




#### _01-door-alarm ####
- esp-12 +(gpio) pro mini
- active buzzer, magnetic door sw, capacitor, battery
- pub door status, using pro mini as external interrupt


#### _02-mqtt-sw ####
- esp-12
- power(5v + 3.3V), fuse(10A + 73°C thermal), 1CH relay, SW(top + lamp), PIR, DS18B20(in + out), DHT22
- on/off lamp using mqtt, pub temp(inside of box + outside)/humidity/pir


#### _03-hx711-scale ####
- esp-12 +(i2c) pro mini
- hx711, load cell, tilt sw
- pub measured weight of pet


#### _04-mqtt-lcd-dust-sensor ####
- esp-01 +(i2c) nano
- lcd(i2c), rtc(i2c), level convertor, Sharp dust sensor, IR sned/recv
- display clock, temp/humidity(mqtt sub), dust
- control LG_AC using Apple remote


#### _05-two-ds18b20 ####
- esp-12
- 2 x DS18B20, battery
- pub temp(inside + outside)


#### _06-power-meter ####
- esp-12
- CT sensor, line tracker
- pub power usage


#### _07-ac-ir-remote-time ####
- pro mini
- optical isolator
- add timer to LG air conditioner remote
- 30 min run, 60 min off

