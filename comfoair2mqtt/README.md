# Home Assistant Add-on: Comfoair 2 MQTT

HAOS Addon Wrapper for [hacomfoairmqtt](https://github.com/adorobis/hacomfoairmqtt).

## What does this Addon do? 
1. Expose [hacomfoairmqtt](https://github.com/adorobis/hacomfoairmqtt) Configuration in Homeassistant
2. Working Python Environment
3. Installation of [hacomfoairmqtt](https://github.com/adorobis/hacomfoairmqtt)

## Installation in HomeAssistant OS
1. If you don't have a MQTT broker yet; in Home Assistant go to Settings → Add-ons → Add-on store and install the Mosquitto broker addon.
2. Go back to the Add-on store, click ⋮ → Repositories, fill in
https://github.com/TimWeyand/homeassistant-addon and click Add → Check for Updates -> Close.
3. The repository includes one add-on:
   - **Comfoair 2 MQTT** is the latest tested release.
4. Click on the addon and press **Install** and wait till the addon is installed.
5. Click on Configuration
   - Fill in the serial details (e.g. port of your USB Serial Converter). If you don't know the port and you have just one USB device connected to your machine try `/dev/ttyUSB0`. Else use the [Home Assistant CLI](https://www.home-assistant.io/common-tasks/os#home-assistant-via-the-command-line) and execute `ha hardware info` to find out. 
   ```yaml
        /dev/ttyUSB0
   ```
   - If you are **not** using the Mosquitto broker addon fill in your MQTT details (leave empty when using the Mosquitto broker addon). Format can be found [here](https://www.zigbee2mqtt.io/guide/configuration/mqtt.html#server-connection), but skip the initial `mqtt:` indent. e.g.: <br>
        ```yaml
        host: localhost
        port: 1883
        user: my_user
        password: my_password
        keepalive: 45
        ```
6. Start the addon by going to **Info** and click **Start**

## Issues / Discussion Thread
Discussions about hacomfoair can be found [here](https://community.home-assistant.io/t/zehnder-comfoair-ca350-integration-via-serial-connection-rs232-and-mqtt/173243/249)

## Credits

- adorobis for the main work @ [hacomfoairmqtt](https://github.com/adorobis/hacomfoairmqtt)

