# Turn that light off!

Repository for the ["Turn that light off!" project](https://now.makezurich.ch/project/90)
of [Make Zurich 2023](https://makezurich.ch/).

## The idea

* place light and motion sensors in a room
* if the light sensor detects that the light is on but the motion sensor detects that nobody is in the room, then a message is shown on a display
* you then have one minute of time to turn that light off
* if you turn it off within the agreed time window (default to one minute), then you get a point in a yet to be defined leaderbord
* once you get ten minutes, then you can buy yourself an icecream!

## Tools

* [CircuitPython](https://circuitpython.org/)
* [The Things Network (TTN)](https://www.thethingsnetwork.org/)
* [Adafruit IO](https://io.adafruit.com/)
* [seedstudio Grove](https://wiki.seeedstudio.com/Grove_System/)

## Tasks

* [x] Set up "blue" Raspberry Pi Pico W with light sensor.
* [x] Set up "blue" Raspberry Pi Pico W to send uplink data to the TTN.
* [ ] Set up "blue" Raspberry Pi Pico W to show the light sensor measurements.
* [ ] TBD
* [ ] TBD
