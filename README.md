# wyzesense2mqtt

https://github.com/raetha/wyzesense2mqtt/issues/38#issuecomment-686837295

# Files are located in:
```/opt/wyzesense2mqtt``` 

## Reload before starting
```sudo systemctl daemon-reload```

## Start service
```sudo systemctl start wyzesense2mqtt```

## Check service
```sudo systemctl status wyzesense2mqtt```

# Run tool
```sudo python3 bridge_tool_cli.py --device /dev/hidraw0```
- L - List paired sensors
- P - Pair new sensors
- U <mac> - Unpair sensor
- F - Fix invalid sensors
- X - Exit tool


## View Logs after starting service
```sudo journalctl -fu wyzesense2mqtt```

More info on [journalctl](https://manpages.debian.org/stretch/systemd/journalctl.1.en.html)
