# Bluetooth
Bluetooth input can be enabled by going to child 104. Afterwards GetBTStatus becomes available. Volume can be set using setvol

## StartBTMatch
Endpoint: ```http://<Radio IP>/StartBTMatch```

Enabled bluetooth for peering

Response:
```
<result>OK</result>
```

## GetBTStatus
Endpoint: ```http://<Radio IP>/GetBTStatus```

Returns the current bluetooth status.

Response:
```
<result>
   <vol>5</vol>
   <mute>1</mute>
   <Status>3</Status>
</result>
```

Known values for Status:
* 2: Disconnected
* 3: Connected and playing
* 4: Connected and not playing

## BTCMD
Endpoint: ```http://<Radio IP>/BTCMD?cmd=1```

Sends a command to the playback source

Known values for cmd:
* 1: Play / Pause
* 2: Pause
* 3: Next track
* 4: Previous track

## leave
Bluetooth can be left using gochild?id=1
