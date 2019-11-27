# On Connect
These actions are performed on connect after the App has found a device

## Port 80
### init
Endpoint: ```http://<Radio IP>/init?language=en```
Returns a list of available functions. The language parameter sets the language of the API and the radio
Response:
```
<result>
   <id>1</id>
   <version>j41520190415h</version>
   <lang>en</lang>
   <wifi_set_url>http://192.168.78.1/scan_wifi</wifi_set_url>
   <ptver>20170921</ptver>
   <hotkey_fav>1</hotkey_fav>
   <push_talk>1</push_talk>
   <leave_msg>1</leave_msg>
   <leave_msg_ios>1</leave_msg_ios>
   <M7_SUPPORT>0</M7_SUPPORT>
   <SMS_SUPPORT>0</SMS_SUPPORT>
   <MKEY_SUPPORT>0</MKEY_SUPPORT>
   <UART_CD>0</UART_CD>
   <ALEXA>0</ALEXA>
   <PlayMode>1</PlayMode>
   <cur_play_menu_id>136</cur_play_menu_id>
   <cur_play_name>SWR3</cur_play_name>
   <SWUpdate>NO</SWUpdate>
</result>
```

### hotkeylist
Endpoint: ```http://<Radio IP>/hotkeylist```
Returns a list of hotkeys? Currently not sure how to configure a hotkey
Response:
```
<menu>
   <item_total>5</item_total>
   <item_return>5</item_return>
   <item>
      <id>75_0</id>
      <status>emptyfile</status>
      <name>Empty</name>
   </item>
   <item>
      <id>75_1</id>
      <status>emptyfile</status>
      <name>Empty</name>
   </item>
   <item>
      <id>75_2</id>
      <status>emptyfile</status>
      <name>Empty</name>
   </item>
   <item>
      <id>75_3</id>
      <status>emptyfile</status>
      <name>Empty</name>
   </item>
   <item>
      <id>75_4</id>
      <status>emptyfile</status>
      <name>Empty</name>
   </item>
</menu>
```

### checknewsw
Endpoint: ```http://<Radio IP>/checknewsw```
Returns probably YES if an update is available. Otherwise NO.
Reponse:
```
<result>NO</result>
```

### list
Endpoint: ```http://<Radio IP>/list?id=1&start=1&count=250```
Returns a list of menu items. See list.md for more information
Response:
```
<menu>
   <item_total>9</item_total>
   <item_return>9</item_return>
   <item>
      <id>87</id>
      <status>content</status>
      <name>Local Radio</name>
   </item>
   <item>
      <id>52</id>
      <status>content</status>
      <name>Internet Radio</name>
   </item>
   <item>
      <id>2</id>
      <status>content</status>
      <name>Media Center</name>
   </item>
   <item>
      <id>169</id>
      <status>content</status>
      <name>DAB (IR)</name>
   </item>
   <item>
      <id>136</id>
      <status>content</status>
      <name>Spotify Connect</name>
   </item>
   <item>
      <id>3</id>
      <status>content</status>
      <name>Information Center</name>
   </item>
   <item>
      <id>47</id>
      <status>content</status>
      <name>AUX</name>
   </item>
   <item>
      <id>104</id>
      <status>content</status>
      <name>Bluetooth</name>
   </item>
   <item>
      <id>6</id>
      <status>content</status>
      <name>Configuration</name>
   </item>
</menu>
```

## DLNA?
A HTTP on Port 52525 is connected twice

### root_XXYY.xml
Endpoint: ```http://<Radio IP>:52525/root_XXYY.xml```
Seems to be DLNA
Response:
```
<root>
  <specVersion>
    <major>1</major>
    <minor>0</minor>
  </specVersion>
  <device>
    <deviceType>urn:schemas-upnp-org:device:MediaRenderer:1</deviceType>
    <friendlyName>PEG-NET-BLK</friendlyName>
    <manufacturer/>
    <manufacturerURL/>
    <modelDescription>Media Renderer Device</modelDescription>
    <modelName>iRadio Renderer</modelName>
    <modelNumber/>
    <modelURL/>
    <UDN>uuid:54998793-37ab-49d1-9cd7-203233197800</UDN>
    <dlna:X_DLNADOC>DMR-1.50</dlna:X_DLNADOC>
    <iconList>
      <icon>
        <mimetype>image/jpeg</mimetype>
        <width>70</width>
        <height>70</height>
        <depth>24</depth>
        <url>xml/mediaU.jpg</url>
      </icon>
      <icon>
        <mimetype>image/jpeg</mimetype>
        <width>48</width>
        <height>48</height>
        <depth>24</depth>
        <url>xml/mediaU_s.jpg</url>
      </icon>
    </iconList>
    <serviceList>
      <service>
        <serviceType>urn:schemas-upnp-org:service:RenderingControl:1</serviceType>
        <serviceId>urn:upnp-org:serviceId:RenderingControl</serviceId>
        <controlURL>/RenderingControl/Control</controlURL>
        <eventSubURL>/RenderingControl/Event</eventSubURL>
        <SCPDURL>/xml/RenderingControl.xml</SCPDURL>
      </service>
      <service>
        <serviceType>urn:schemas-upnp-org:service:AVTransport:1</serviceType>
        <serviceId>urn:upnp-org:serviceId:AVTransport</serviceId>
        <controlURL>/AVTransport/Control</controlURL>
        <eventSubURL>/AVTransport/Event</eventSubURL>
        <SCPDURL>/xml/AVTransport.xml</SCPDURL>
      </service>
      <service>
        <serviceType>urn:schemas-upnp-org:service:ConnectionManager:1</serviceType>
        <serviceId>urn:upnp-org:serviceId:ConnectionManager</serviceId>
        <controlURL>/ConnectionManager/Control</controlURL>
        <eventSubURL>/ConnectionManager/Event</eventSubURL>
        <SCPDURL>/xml/ConnectionManager.xml</SCPDURL>
      </service>
    </serviceList>
  </device>
</root>
```

### /xml/mediaU_s.jpg
Endpoint: ```http://<Radio IP>:52525/xml/mediaU_s.jpg```
A JPG icon
