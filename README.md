# Inkplate 6 weather station dashboard

<img src="https://github.com/kjordahl/inkplate6-weather-dashboard/blob/main/images/example.jpg" width="400">

This project uses an e-paper display and [ESPHome](https://esphome.io/index.html)
to display a real-time weather dashboard. I used an
[Inkplate 6](https://soldered.com/product/soldered-inkplate-6-6-e-paper-board)
from [Soldered](https://soldered.com), but any display supported by
ESPHome should be very similar.

## Requirements

This dashboard makes heavy use of sensors from [Home Assistant](https://www.home-assistant.io/)
to populate values in the dashboard. Integration between ESPHome and Home
Assistant is excellent. I am using my own sensors for some data,
including an [Ecowitt](https://www.ecowitt.com)
[outdoor temperature and humidity sensor](https://shop.ecowitt.com/collections/temp-humidity-sensor/products/wh32-outdoor)
and
[air quality sensor](https://shop.ecowitt.com/collections/air-quality-sensor/products/wh41).
These sensors are inexpensive and integrate well into Home Assistant,
but you can use any sensor that HA can interact with, including
building your own. If you don't have any sensors, you can also use
weather integrations in Home Assistant for weather data.

This version makes use of 3 different fonts. Two of them (Roboto and
[MDI](https://pictogrammers.com/library/mdi/)) are fetched remotely
at compile time. The third,
[Weather Icons](https://erikflowers.github.io/weather-icons/), should
be downloaded from the
[source](https://github.com/erikflowers/weather-icons/blob/master/font/weathericons-regular-webfont.ttf)
and placed in the fonts subdirectory on your ESPHome instance. It is
possible to use weather icons from MDI instead, and eliminate the
dependency on the Weather Icons font, but I preferred the glyphs
available there.

## References

- [Weatherman Dashboard for ESPHome](https://github.com/Madelena/esphome-weatherman-dashboard)
- [ESP32 based E-Paper Display to display Smart Home Data](https://github.com/krikk/esp32_E-Paper_Display)
- [Inkplate 10 Weather Calendar](https://github.com/chrisjtwomey/inkplate10-weather-cal)
- [Inkplate documentation from ESPHome](https://esphome.io/components/display/inkplate6.html)
- [Home Assistant](https://www.home-assistant.io)
