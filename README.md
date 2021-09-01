# christmas 2021
The PCB outline can be generated from the included svg file `star template` using the [svg2shenzen](https://github.com/badgeek/svg2shenzhen) plugin.


## current idea
ESP12F has 15 (17 including rx tx) gpio available. There are 45 signals required to controll each color individually. By combining the same color every 5 leds, all leds can be controlled. Issue that remains is the current requirement per GPIO which far exceeds the limit of the pin.
The current can be increased by adding transistors/fets or something like 2 of the ULN2803 and common anode leds.


kicad lib: [https://github.com/jdunmire/kicad-ESP8266](https://github.com/jdunmire/kicad-ESP8266)
## Possible parts
- ESP32 wroom/wrover -> most expensive option but has plenty of IO, does require a pad to be soldered, hot air required
- ESP01 -> very few pins but cheap
- ESP12F/E -> Good option but almost same price as ESP32 but reduced functionality and soon to be replaced by ESP32-C3