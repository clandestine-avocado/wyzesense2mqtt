# WyzeSense2mqtt

Currently running [wyzesense2mqtt](https://github.com/raetha/wyzesense2mqtt) on the Pi 3B using the [Linux Systemd method](https://github.com/raetha/wyzesense2mqtt#linux-systemd). Pi3B is also running Deconz, which hosts the Conbee II USB Zigbee coordinator.


Initially had some issues getting set up -  resolved via [this thread](https://github.com/raetha/wyzesense2mqtt/issues/38#issuecomment-686837295) and another issue [here](https://github.com/raetha/wyzesense2mqtt/issues/46).


## Files are located here, nav via:
```cd /opt/wyzesense2mqtt``` 

## Enable once, will start on boot:
```sudo systemctl enable wyzesense2mqtt.service```

## Enable once, will start on boot:
```sudo systemctl disable wyzesense2mqtt.service```


## Reload before starting
```sudo systemctl daemon-reload```

## Start service
```sudo systemctl start wyzesense2mqtt```

## Check service
```sudo systemctl status wyzesense2mqtt```

## Run tool
```sudo python3 /opt/wyzesense2mqtt/bridge_tool_cli.py --device /dev/hidraw0```
- L - List paired sensors
- P - Pair new sensors
- U <mac> - Unpair sensor
- F - Fix invalid sensors
- X - Exit tool


## View Logs after starting service
```sudo journalctl -fu wyzesense2mqtt```

More info on [journalctl](https://manpages.debian.org/stretch/systemd/journalctl.1.en.html)
