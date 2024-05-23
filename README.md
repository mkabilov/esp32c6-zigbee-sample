# ESP32C6 Zigbee sample project 

## Wiring

RGB led with common cathode is used

```
LED            ESP32
---            -----
LED_RED   -->  GPIO_NUM_21
LED_GREEN -->  GPIO_NUM_22
LED_BLUE  -->  GPIO_NUM_23

LED_GND   -->  GND
```

## Build
```bash
idf.py build erase-flash flash
```

optionally monitor:
```bash
idf.py monitor
```

## Zigbee2MQTT side:
put `esp32_lamp.js` into the `/opt/zigbee2mqtt/data` dir, 
edit configuration.yaml:
```yaml
...
external_converters:
  - esp32_lamp.js
...
```