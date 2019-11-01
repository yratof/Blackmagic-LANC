# Blackmagic-LANC
A project to control the Black Magic line of cameras through the LANC port, probably with an arduino or ESP 8266

Based on the original plans found here:
https://create.arduino.cc/projecthub/L-Rosen/serial-to-lanc-control-l-70f735

Using the command codes found here:
https://forum.blackmagicdesign.com/viewtopic.php?f=2&t=16676

```
Name bytes[1:0]
---------------------------------
Nop = 0x0000,
RecordStart = 0x3318,
RecordStop = 0x198C,
IrisIncrement = 0x5528, // Used for IDLE state
IrisDecrement = 0x5328, // Used for IDLE state
IrisRecIncrement = 0x2A94, // Used for RECORD state
IrisRecDecrement = 0x2994, // Used for RECORD state
IrisAutoAdjust = 0xAF28,
FocusShuttleFar = 0xE028, // Used for IDLE state (value mask 0x0F00: 1 3 5 7 9 B D F)
FocusShuttleNear = 0xF028, // Used for IDLE state (value mask 0x0F00: 1 3 5 7 9 B D F)
FocusShuttleRecFar = 0x7094, // Used for RECORD state (value mask 0x0700: 0 1 2 3 4 5 6 7)
FocusShuttleRecNear = 0x7894, // Used for RECORD state (value mask 0x0700: 0 1 2 3 4 5 6 7)
FocusFar = 0x4528, // Used for IDLE state
FocusNear = 0x4728, // Used for IDLE state
FocusRecFar = 0x2394, // Used for RECORD state
FocusRecNear = 0x2294, // Used for RECORD state
```

Wifi AP server info found here:
https://42bots.com/tutorials/esp8266-example-wi-fi-access-point-web-server-static-ip-remote-control/
