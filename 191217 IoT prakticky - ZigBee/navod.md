# Návod k rozchození Zigbee

- Instalace MQTT ([Eclipse Mosquitto](http://mosquitto.org/)) - dle distribuce - např. `dnf install mosquitto`  
  (o MQTT vyšel hezký článek na [Rootu](https://www.root.cz/clanky/protokol-mqtt-komunikacni-standard-pro-iot/))
- Instalace Zigbee2mqtt dle [instrukcí na jejich webu](https://www.zigbee2mqtt.io/getting_started/running_zigbee2mqtt.html)
- V [konfiguraci](https://www.zigbee2mqtt.io/information/configuration.html) nastavit připojení na MQTT a povolit párování nových zařízení (`permit_join: true`)
- Mezi [podporovanými zařízeními](https://www.zigbee2mqtt.io/information/supported_devices.html) najít své (např. [Xiaomi MiJia wireless switch](https://www.zigbee2mqtt.io/devices/WXKG01LM.html)) a přečíst si postup párování
- Po úspěšném párování již budou chodit zprávy do MQTT, můžeme je sledovat přes `mosquitto_sub -v -t '#'`
- Instalaci [Node-RED](https://nodered.org/) si můžeme zjednodušit pomocí [instalačního skriptu pro Linux](https://github.com/node-red/linux-installers)
- Teď už si můžeme definovat libovolné akce spojováním bloků v Node-RED, např. `mqtt in`, který poslouchá topic tlačítka a pak `exec`, který spustí skript na serveru a zakáže dětem přístup na WiFi
