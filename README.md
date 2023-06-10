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
* [Datasette]()

## Tasks

**NOTE**

* The "blue" Raspberry Pi Pico W sends **uplink** ⬆️ messages to the TTN
* The "purple" Raspberry Pi Pico W receives **downlink** ⬇️ messages from Adafruit IO

* [x] Set up "blue" Raspberry Pi Pico W with light sensor.
* [x] Set up "blue" Raspberry Pi Pico W to send uplink data to the TTN.
* [ ] Set up "blue" Raspberry Pi Pico W to show the intensity of the light sensor using the onboard Neopixels.
* [x] Set up "purple" Raspberry Pi Pico W with light LCD display.
* [x] Set up "purple" Raspberry Pi Pico W to connect to WiFi.
* [x] Set up "purple" Raspberry Pi Pico W to subscribe to the `mz23` topic from the Adafruit IO MQTT broker.
* [x] Install Datasette
* [x] Visualize `mqtt.db` SQLite database with Datasette
* [x] Develop `subscribe_to_ttn.py` Python script to subscribed to the MQTT TTN integration.
* [x] Develop `subscribe_to_ttn.py` Python script to store the received data to a local SQLite database.
* [x] Develop `publish_to_aio.py` Python script to read data from a local SQLite database.
* [x] Develop `publish_to_aio.py` Python script to publish data to the Adafruit IO MQTT broker.
* [ ] Dockerize the two Python scripts above.

## Instructions

### Datasette

[Install Datasette](https://docs.datasette.io/en/stable/getting_started.html#using-datasette-on-your-own-computer) in your Python environment:

```bash
pip install datasette
```

Run Datasette against a SQLite file on your computer using the following command:

```bash
datasette mqtt.db
```

Then open your browser at [http://127.0.0.1:8001](http://127.0.0.1:8001).
