# ESPHome Projects

## About
[ESPHome](https://esphome.io/) is the perfect solution for creating custom firmwares for your ESP8266/ESP32 boards. This is a repo with my projects.

## Running

This is based on [Getting Started with the ESPHome Command Line](https://esphome.io/guides/getting_started_command_line.html)

I've initially tried with bare commandline but hit dependency hell and decided that docker solution is cleaner.

### Initialization
Initial programming is via a PC with ESP chip connected via USB.

Get the tools image:
```
docker pull esphome/esphome
```

Projects are defined as the YAML files in subdrs.

Initial uploading:
```
docker run --rm -v "${PWD}":/config --device=/dev/ttyUSB0 -it esphome/esphome run livingroom.yaml
```

### Dashboard

The tool comes with a nice dashboard:
```
# On Docker, host networking mode is required for online status indicators
docker run --rm --net=host -v "${PWD}":/config -it esphome/esphome
```
Access the dashboard at [localhost:6052](http://localhost:6052)
