# Temperature sensor


## Whats needed

1. Temperature sensor - [DHT21](https://botland.com.pl/czujniki-multifunkcyjne/1884-czujnik-temperatury-i-wilgotnosci-dht21-am2301-w-obudowie-5904422373269.html)
2. ESP32 board

[Reference doc](https://esphome.io/components/sensor/dht.html)


## Configuration

![plugscheme](../particulate_matter_sensor/images/ESP32-DOIT-DEV-KIT-v1-pinout-mischianti.png)

| PMS DHT21 | PURPOSE | ESP32 PIN |
|---------|--------|------------|
| Red   | Vcc        | VCC        |
| Yellow   | Data        | via 10kOhm pullup        |
| Black   | GND        | GND      |


**Note**
The [configuration](thsensor.yaml) stores secrtets in `secrets.yaml`, not included in this repo:
```
wifi_ssid: <REDACTED>
wifi_password: <REDACTED>
ap_ssid: <REDACTED>
ap_password: <REDACTED>
api_password: <REDACTED>
```

## Integration with HomeAssistant

The advantage of ESPHome is that HomeAssistant's ESPHome integration detects this device right away and imports the entities without any extra configs.
