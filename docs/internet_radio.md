# Internet Radio
Internet Radio can be enabled by going to child 52 Volume can be set using setvol

## AddRadioStation
Endpoint: ```http://<Radio IP>/AddRadioStation?name=<Stream Name>&url=<Stream URL>```

Adds a new radio station

Response:
```
<result>
   <rt>OK</rt>
</result>
```

## setfav
Endpoint: ```http://10.1.13.114/setfav?id=59_0&item=0&favpos=6```

Sets an existing station as favourite. Station id can be found using listid=75

Response:
```
<result>
   <rt>OK</rt>
</result>
```

## delfav
Endpoint: ```http://<Radio IP>/delfav?item=6```

Deletes a radio station. Stations can be found by using listid=75

Response:
```
<result>OK</result>
```

## playhotkey
Endpoint: ```http://<Radio IP>/playhotkey?key=1```

Starts playback of a defined radio hotkey

Response:

```
<result>
   <id>75</id>
   <rt>OK</rt>
</result>
```

## leave
Internet Radio can be left using gochild?id=1
