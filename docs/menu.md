# Menu
This file documents all actions which invoke actions to the menu on the device or the app

## App (Remote)
### list
Endpoint: ```http://<Radio IP>/list?id=1&start=1&count=250```

Returns data to fill a menu in the App

Parameters:
* id: Menu ID
* start: offset for paged menus (not working on every menu)
* count: Limit of values

id=1 returns the main menu

Response (for id=1):
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
The returned ID can be used together with gochild. Using gochild is required to traverse deeper than one level into a submenu. After calling gochild, list can be used to retrieve the menu items

## Display (Local)
### gochild
Endpoint: ```http://<Radio IP>/gochild?id=47```

Sets the displayed menu to the menu ID from list.

Response:
```
<result>
   <id>47</id>
</result>
```
### back
Endpoint: ```http://<Radio IP>/back```

Sets the menu level to one level above

Response:
```
<result>
   <id>1</id>
   <SWUpdate>NO</SWUpdate>
</result>
```
