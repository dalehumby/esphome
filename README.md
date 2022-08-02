# ESPHome config files

Mostly here as backup for me, but maybe someone else finds them useful:

- `particulate.yaml` for measuring 2.5 µg and 10 µg particulate, temperature, humidity and illuminance (lux)
- `samsungtv.yaml` to switch on/off my Samsung TV with IR, and get feedback from USB power
- `lounge.yaml` and `bedroom.yaml` for [Apple Watch presence detection](https://github.com/dalehumby/ESPHome-Apple-Watch-detection) and Mijia temperature/humidity logging
- `epaper213.yaml` 2.13 inch epaper clock, weather and next calendar appointment, connecting over internet to home MQTT

## Install ESPHome manually

```
python3 -m venv env
source env/bin/activate
pip install -r requirements.txt
```

Then build with 

```
esphome run epaper213.yaml
```
