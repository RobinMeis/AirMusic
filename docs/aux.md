# AUX
AUX input can be enabled by going to child 47. Afterwards playinfo becomes available. Volume can be set using setvol

## playinfo
Endpoint: ```http://<Radio IP>/playinfo```

Returns the current volume and mute status.

Response:
```
<result>
   <vol>5</vol>
   <mute>1</mute>
</result>
```

## leave
AUX can be left using gochild?id=1
