# ESP32C6 Zigbee sample project 

## Build
```bash
idf.py build erase-flash flash
```

optionally monitor:
```bash
idf.py monitor
```

## Zigbee2MQTT side:
put `esp32_lamp.js` into the `/opt/zigbee2mqtt/data` dir
edit configuration.yaml:
```yaml
...
external_converters:
  - esp32_lamp.js
...
```