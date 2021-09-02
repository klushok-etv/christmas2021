# christmas 2021
The PCB outline can be generated from the included svg file `star template` using the [svg2shenzen](https://github.com/badgeek/svg2shenzhen) plugin.


## current idea
ESP12F has 15 (17 including rx tx) gpio available. There are 45 signals required to controll each color individually. By combining the same color every 5 leds, all leds can be controlled. Issue that remains is the current requirement per GPIO which far exceeds the limit of the pin.
The current can be increased by adding transistors/fets or something like 2 of the ULN2803 and common anode leds.


kicad lib: [https://github.com/jdunmire/kicad-ESP8266](https://github.com/jdunmire/kicad-ESP8266)
## Possible parts
- ESP32 wroom/wrover -> most expensive and biggest option but has plenty of IO, does require a pad to be soldered so hot air is required
- ESP01 -> very few pins but cheap
- ESP M3 -> based on the 8285 chip with low memory and only a few GPIO's but has a small footprint and is cheap
- ESP12F/E -> Good option but almost same price as ESP32 but reduced functionality and soon to be replaced by ESP32-C3 [https://www.aliexpress.com/item/32963951195.html](https://www.aliexpress.com/item/32963951195.html)
- pl9823 led [https://nl.aliexpress.com/item/32963082574.html](https://nl.aliexpress.com/item/32963082574.html)
- APA106 led [https://www.aliexpress.com/item/4001066329177.html](https://www.aliexpress.com/item/4001066329177.html)
- buttons for reset and gpio0, 3x6x2.5mm: [https://www.aliexpress.com/item/32696590759.html](https://www.aliexpress.com/item/32696590759.html)