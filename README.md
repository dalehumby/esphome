# ESPHome config files

Mostly here as backup for me, but maybe someone else finds them useful:

- [`particulate.yaml`](particulate.yaml) for measuring 2.5 µg and 10 µg particulate, temperature, humidity and illuminance (lux)
- [`samsungtv.yaml`](samsungtv.yaml) to switch on/off my Samsung TV with IR, and get feedback from USB power
- [`lounge.yaml`](lounge.yaml) and [`bedroom.yaml`](bedroom.yaml) for [Apple Watch presence detection](https://github.com/dalehumby/ESPHome-Apple-Watch-detection) and Mijia temperature/humidity logging
- [`epaper213.yaml`](epaper213.yaml) 2.13 inch epaper clock, weather and next calendar appointment, connecting over internet to home MQTT
- [`epaper47.yaml`](epaper47.yaml) 4.7 inch epaper desk picture frame with clock, weather, appointments, Spotify now-playing, connecting over internet to home MQTT
- [`sms-telegram.yaml`](sms-telegram.yaml) for forwarding SMSs and missed call notifications to a Telegram bot (uses Node-RED to interface to the Telegram Bot API)
- [`vindriktning.yaml`](vindriktning.yaml) relaces the standard IKEA Vindriktning controller with an ESP8266 and adds other air quality sensors and RGB status LEDs


## Install ESPHome manually

```bash
python3 -m venv env
source env/bin/activate
pip install -r requirements.txt
```

Then build with 

```bash
esphome run epaper213.yaml
```

## Connecting to ESP device

Usually I flash the ESPs over the WiFi using ESPHome's web interface. But the first time you flash ESPHome onto an ESP you need to do it by plugging the ESP into a USB port and flashing over serial.

You may need USB-to-serial drivers installed for the Mac to detect the serial chip on the "D1 mini" boards. (TODO where to get that from.)

Plug the "D1 mini" into a USB port on the Mac, run

```bash
ls /dev/cu.*
```

If you get something like

```bash
/dev/cu.usbserial-230
```

then the ESP has been detected.
