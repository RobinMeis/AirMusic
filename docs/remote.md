# Remote
The App offers a virtual remote control with all buttons which are available on the original IR control. The API Endpoint is located at `http://<Radio IP>/Sendkey?key=<Button ID>`

## Buttons
|ID |   Function    |
|---|---------------|
|1  | Home          |
|2  | Up            |
|3  | Down          |
|4  | Left          |
|5  | Right         |
|6  | Enter         |
|7  | On / Off      |
|8  | Mute / Unmute |
|9  | Volume Up     |
|10 | Volume Down   |
|12 | Sleep Timer   |
|14 | Brightness    |
|15 | "Star"        |
|28 | Mode          |
|29 | Play / Pause  |
|31 | Next Track    |
|32 | Previous Track|
|106| Equalizer     |
|115| "1"           |
|116| "2"           |
|117| "3"           |
|118| "4"           |
|119| "5"           |

Response:
```
<result>
  <rt>OK</rt>
</result>
```

OK is also returned for undocumented button IDs <= 181 (also negatives). There might be more buttons which aren't shown in the App. For invalid buttons it returns:
```
<result>
  <rt>FAIL</rt>
</result>
```
