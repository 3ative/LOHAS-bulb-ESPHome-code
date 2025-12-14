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

<div align="center">

### 💖 Support This Project

Found this useful? Want to say thanks and fuel future creations?

**Your support keeps the creativity flowing!** 🍺✨

<table>
  <tr>
    <td align="center">
      <a href="https://www.buymeacoffee.com/3ative">
        <img src="https://img.shields.io/badge/Buy%20Me%20A%20Coffee-Support-yellow.svg?style=for-the-badge&logo=buy-me-a-coffee&logoColor=white" alt="Buy Me A Coffee"/>
        <br/>
        <b>☕ Buy me a Coffee</b>
      </a>
    </td>
    <td align="center">
      <a href="https://www.patreon.com/3ative">
        <img src="https://img.shields.io/badge/Patreon-Become%20a%20Patron-red.svg?style=for-the-badge&logo=patreon&logoColor=white" alt="Patreon"/>
        <br/>
        <b>💖 Join on Patreon</b>
      </a>
    </td>
  </tr>
</table>

**Every contribution helps bring more awesome projects to life!** 🚀

</div>

---
