# ESPHome based E-Ink Dashboard

![Front Picture](screenshots\front_picture.jpg)

## Components
### Hardware
- **ESP32 Board**: Universal e-Paper Raw Panel Driver Board by Waveshare: [Universal e-Paper Raw Panel Driver Board](https://www.waveshare.com/product/e-paper-esp32-driver-board.htm)
- **E-Ink Display**: 7.5-inch E-Paper E-Ink Display Module by Waveshare: [7.5inch E-Paper E-Ink Display Module](https://www.waveshare.com/pico-epaper-7.5-b.htm)

The firmware supports a large amount of the available E-ink displays. These components can then be added to a cheap picture frame to create a low cost e-ink display, see https://esphome.io/components/display/waveshare_epaper.html for more details. 

![Rear Picture](screenshots\back_picture.jpg.jpg)

### Firmware
was used in this example and loaded with the firmware using https://esphome.io/. The configuration is defined in the and then set up with the [esphome-eink.yaml](esphome-eink.yaml), note: the following secrets need to be provided in your esphome dashboard's secrets file and if using a different display module, the substitution in the yaml must be changed.

| Substitutions Key | Value |
|---|---|
| `display_model` | E-Ink display model, valid list available [here](https://esphome.io/components/display/waveshare_epaper.html) |

| Secret Key | Value |
|---|---|
| `wifi_ssid` | Your Wi-Fi SSID |
| `wifi_password` | Your Wi-Fi password |
| `ap_password` | Access Point password (for reconnection) |
| `ota_password` | Password for over-the-air updates |

### Server
The project uses [sibbl/hass-lovelace-kindle-screensaver ](https://github.com/sibbl/hass-lovelace-kindle-screensaver) to connect with Home Assistant and display Lovelace dashboards. However any server serving PNG files can be used to allow the frame to be used for pictures in a frame.
Please refer to that respective project's documentation and resources for detailed setup instructions and further customization options.