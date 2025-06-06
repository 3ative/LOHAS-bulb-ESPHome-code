# LOHAS Bulb ESPHome code
This is the ESPHome code I use on my RGBW LOHAS WiFi Bulbs

```yaml
esphome:
  name: bulb_main_light
  platform: ESP8266
  board: esp01_1m
wifi:
  ssid: !secret wifi_ssid
  password: !secret wifi_password

logger:
api:
ota:
  platform: esphome

light:
  - platform: rgbww
    name: "Bulb Main Light"
    id: bulb_main_light
    red: red
    green: green
    blue: blue
    warm_white: ww
    cold_white: cw
    cold_white_color_temperature: 6536 K
    warm_white_color_temperature: 2000 K

output:
  - platform: esp8266_pwm
    id: red
    pin: GPIO5
  - platform: esp8266_pwm
    id: green
    pin: GPIO4
  - platform: esp8266_pwm
    id: blue
    pin: GPIO13
  - platform: esp8266_pwm
    id: ww
    pin: GPIO12
  - platform: esp8266_pwm
    id: cw
    pin: GPIO14
    
   ```

---
### 🤝 Found this useful, want to say 'Thanks' and support my efforts. CHEERS🍺
| Buy me a Coffee | PATREON |
|-----------------|---------|
| [![Buy Me A Coffee](https://img.shields.io/badge/Buy%20Me%20A%20Coffee-donate-yellow.svg?style=flat-square&logo=buy-me-a-coffee)](https://www.buymeacoffee.com/3ative) | [![Patreon](https://img.shields.io/badge/Patreon-support-red.svg?style=flat-square&logo=patreon)](https://www.patreon.com/3ative) |
---
