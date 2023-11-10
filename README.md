# Raspberry Pi Pico Screw Terminal Board with W5500 Ethernet module
Some notes:

This is a repo for my personal Raspberry Pi pico project board which has a goal to make an easily connectable simple smart home control board connected via Ethernet.

I have no formal electrical engineering training, just learning as I go, so sorry in advance for any mistakes made.

![soldered-pi-pico-w5500-ethernet-board-with-screw-therminals](https://github.com/wangeris/Pi-Pico-Screw-Terminal-Board-with-W5500-Ethernet-module/blob/main/Images/real1.JPG?raw=true)

# Why I decided to make this.

I have a prototype system based on an Arduino Uno and W5500 Ethernet board connected up using pigtais, that's been used in my garrage as a security and control center integrated via MQTT with Home Assistant. My goal for this was to clean up the whole thing and make it easier to connect up new sensors as it's a pain to solder up pigtails on wires each time. Also decided to upgrade to Pi Pico as it's much more powerfull and cheaper than Arduino at this point.

I decided to go with Pi Pico over an ESP32 based board, because Pi Picos are standartized, so not as confusing to source, I also expect the software support to be much better based on Raspbery Pi SBC support in the past.

I went with W5500 for connection/internet just as a personal preference for stability and security over WiFi, but Pi Pico W could be used with this as well.

# Technical side
Most pins are labeled on the PCB itself.

![pi-pico-w5500-connection](https://github.com/wangeris/Pi-Pico-Screw-Terminal-Board-with-W5500-Ethernet-module/blob/main/Images/raspberry_w5500.PNG?raw=true)

W5500 module to Pi Pico is connected using these pins:<br>
SCLK - GPIO2<br>
MOSI - GPIO3<br>
MISO - GPIO4<br>
CS   - GPIO5<br>
RST  - GPIO6<br>
W5500 module itself is powered from 3.3V output of the Pi Pico

PCB is 2-layer and is designed using EasyEDA<br>
3.5mm pitch screw terminals and USR-ES1 type W5500 Ethernet module are used. Both Raspberry Pi Pico and W models should work. Pi pico can be soldered directly or connected via soldered on 2.54mm female headers.

Gerber file is in the Hardware folder.

![pi-pico-w5500-screw-pcb-gerber-design](https://github.com/wangeris/Pi-Pico-Screw-Terminal-Board-with-W5500-Ethernet-module/blob/main/Images/pcb.JPG?raw=true)
