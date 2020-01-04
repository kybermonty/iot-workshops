# Levné řešení domácí sítě ZigBee

## Hardware

### CC2531 USB dongle
[AliExpress](https://www.aliexpress.com/item/33011691700.html) - $7.55 - cca 172 Kč  
[Manuál](http://www.ti.com/lit/ug/swru221a/swru221a.pdf)

## Firmware

### Z-Stack coordinator firmware
[github.com/Koenkk/Z-Stack-firmware/tree/master/coordinator](https://github.com/Koenkk/Z-Stack-firmware/tree/master/coordinator)

## Software

### Zigbee2mqtt
[www.zigbee2mqtt.io](https://www.zigbee2mqtt.io/)

Konfigurace:
- nastavit připojení na mqtt a vlastní network_key
- LEDka hodně svítí, ale dá se vypnout (disable_led: true)
- výchozí je kanál 11, můžeme změnit dle zarušenosti WiFinama:

![ZigBee channels](zigbee-channels.png)

### MQTT broker
[Eclipse Mosquitto](http://mosquitto.org/)

### Home Assistant
[www.home-assistant.io](https://www.home-assistant.io/)

## Supported devices

### Xiaomi Mi

- Xiaomi Mi Wireless Switch  
  [Alza](https://www.alza.cz/xiaomi-mi-wireless-switch-d5668745.htm) - 349 Kč,
  [AliExpress](https://www.aliexpress.com/item/32818007384.html) - $7.64 - cca 175 Kč

- Xiaomi Mi Window and Door Sensor  
  [Alza](https://www.alza.cz/xiaomi-mi-window-and-door-sensor-d5668744.htm) - 399 Kč,
  [AliExpress](https://www.aliexpress.com/item/32714904459.html) - $7.85 - cca 180 Kč

- Xiaomi Mi Motion Sensor  
  [Alza](https://www.alza.cz/xiaomi-mi-motion-sensor-d5668746.htm) - 449 Kč,
  [AliExpress](https://www.aliexpress.com/item/32815770682.html) - $9.89 - cca 227 Kč

- Xiaomi Mi Temperature and Humidity Sensor  
  [AliExpress](https://www.aliexpress.com/item/32714410866.html) - $7.95 - cca 182 Kč

- Xiaomi Mi Wall Switch  
  [AliExpress](https://www.aliexpress.com/item/32875713201.html) - od $13.46 - cca 308 Kč  
  (i verze bez nuláku - [tady](https://www.aliexpress.com/item/32950175670.html) vyberte No neutral 1key)

- Xiaomi Mi Flood Detector  
  [AliExpress](https://www.aliexpress.com/item/32828708669.html) - $14.96 - cca 343 Kč

- Xiaomi Mi Relay Controller  
  [AliExpress](https://www.aliexpress.com/item/33014653752.html) - $18.98 - cca 428 Kč

### IKEA

- [Chytré osvětlení](https://www.ikea.com/cz/cs/catalog/categories/departments/lighting/smart_lighting/)
- [Bezdrátové rolety](https://www.ikea.com/cz/cs/catalog/categories/departments/living_room/44531/)

### Philips Hue

- [Alza](https://www.alza.cz/inteligentni-osvetleni-philips-hue/18860240.htm)

### SONOFF

- SONOFF BASICZBR3  
  [AliExpress](https://www.aliexpress.com/item/4000333044857.html) - $10.99 - cca 251 Kč
