# LOHAS-bulb-ESPHome-code
This is the ESPHome code I use on my RGBW LOHAS WiFi Bulbs

```yaml
esphome:
  name: bulb_main_light
  platform: ESP8266
  board: esp01_1m
wifi:
  ssid: !secret ssid
  password: !secret wifi_password

logger:
api:
ota:

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

<a href="https://www.buymeacoffee.com/3ative" target="_blank"><img src="https://cdn.buymeacoffee.com/buttons/default-blue.png" alt="Buy Me A Coffee" style="height: 51px !important;width: 217px !important;" ></a>
