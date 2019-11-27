# Settings
This document shows all endpoints for settings

## getdlnaname
Endpoint:
```http://<Radio IP>/getdlnaname```

Returns the product name.

Response:
```
<result>
  <name>PEG-NET-BLK</name>
</result>
```

## GetSystemInfo
Endpoint:
```http://<Radio IP>/GetSystemInfo```

Returns:
* Software Version
* WiFi
  * Status
  * MAC Address
  * SSID
  * RSSI
  * Encryption
  * IP
  * Subnet
  * Gateway
  * DNS Servers

Response:
```
<menu>
  <SW_Ver>6SADNB2F-j415h-j415**a*-j415a-(DB:20190319)</SW_Ver>
  <wifi_info>
    <status>connected</status>
    <MAC>aabbccddeeff</MAC>
    <SSID>WLAN Kabel - IoT</SSID>
    <Signal>78</Signal>
    <Encryption>WPA2/AES</Encryption>
    <IP>10.1.42.20</IP>
    <Subnet>255.255.255.0</Subnet>
    <Gateway>10.1.42.1</Gateway>
    <DNS1>8.8.8.8</DNS1>
    <DNS2>8.8.4.4</DNS2>
  </wifi_info>
</menu>
```
