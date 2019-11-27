# Miscellaneous
This file contains actions which are not fitting into any category

## setvol
Enpoint: ```http://<Radio IP>/setvol?vol=7&mute=0```

Sets the playback volume. Valid values for vol are 0 to 15. Valid values for mute are 0 or 1

Response:
```
<result>
  <vol>7</vol>
  <mute>0</mute>
</result>
```

## Exit
On App exit the following endpoint is called: ```http://<Radio IP>/exit```

Response:
```
<result>
  <rt>INVALID_CMD</rt>
</result>
```
This endpoint doesn't seem to be working
