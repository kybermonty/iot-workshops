# Návod k rozchození Zigbee

- Instalace MQTT ([Eclipse Mosquitto](http://mosquitto.org/)) - dle distribuce - např. `dnf install mosquitto`
  (nebo jako [kontejner v Dockeru](https://hub.docker.com/_/eclipse-mosquitto)).  
  Pokud nevíte, co to je, tak o MQTT vyšel hezký článek na [Rootu](https://www.root.cz/clanky/protokol-mqtt-komunikacni-standard-pro-iot/).
- Instalace Zigbee2mqtt dle [instrukcí na jejich webu](https://www.zigbee2mqtt.io/getting_started/running_zigbee2mqtt.html)
  ([může běžet i v Dockeru](https://www.zigbee2mqtt.io/information/docker.html)).
- V [konfiguraci](https://www.zigbee2mqtt.io/information/configuration.html) nastavit připojení na MQTT a povolit párování nových zařízení (`permit_join: true`).
- Mezi [podporovanými zařízeními](https://www.zigbee2mqtt.io/information/supported_devices.html) najít své (např. [Xiaomi MiJia wireless switch](https://www.zigbee2mqtt.io/devices/WXKG01LM.html)) a přečíst si postup párování. Pozor, IKEA zařízení musí být při párování hodně blízko brány.
- Po úspěšném párování již budou chodit zprávy do MQTT, můžeme je sledovat přes `mosquitto_sub -v -t '#'`.
- Instalaci [Node-RED](https://nodered.org/) si můžeme zjednodušit pomocí [instalačního skriptu pro Linux](https://github.com/node-red/linux-installers) (nebo opět [rozjet v Dockeru](https://nodered.org/docs/getting-started/docker)).
- Teď už si můžeme definovat libovolné akce spojováním bloků v Node-RED, např. `mqtt in`, který poslouchá topic tlačítka a pak `exec`, který spustí skript na serveru a zakáže dětem přístup na WiFi.
- Pro Node-RED existuje i hezký [dashboard](https://flows.nodered.org/node/node-red-dashboard) s grafy, tlačítky apod.
- Další hezké GUI poskytuje [Home Assistant](https://www.home-assistant.io/) - dá se nainstalovat
  ve [virtuálním prostředí pro Python](https://www.home-assistant.io/docs/installation/raspberry-pi/)
  nebo [v Dockeru](https://www.home-assistant.io/docs/installation/docker/)
- Pak je potřeba správně [nakonfigurovat MQTT](https://www.zigbee2mqtt.io/integration/home_assistant.html), aby fungovala integrace se Zigbee2mqtt.
  Všechny spárované Zigbee zařízení se tak samy nakonfigurují v Home Assistantovi.
