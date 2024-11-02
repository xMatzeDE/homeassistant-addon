# Changelog
**Warning:** This is not an official add-on and is not affiliated with SMA. Use at your own risk. This software is experimental.

## 0.0.6
- Add currentLogicSelection to see the current active Modus
- Check for broken pipe at modbus connection (also monitor count / time)
- make deviceId configurable
- Change Hardcoded deviceId to configurable deviceId

## 0.0.5
- Removed Check and Reset, which caused to remove the OverwriteLogicSelection to reset

## 0.0.4
- Fixed the Logic for Pause (charge ok)

## 0.0.3
- Fix an overwrite of BatteryControl on Startup
- Fix that control commands are not send on ReadIntervall

## 0.0.2
- Retain Configuration in MQTT and read them on startup

