# Docs
This directory contains the documentation of the protocol between the iOS AirMusic App and the radio.

## Servers
The radio has three open ports

### 80 (HTTP)
Offers a basic (non-functional) GUI. Is the main API Endpoint. Warning: This is a stateful API

This API seems to be basic authenticated. At least the App sends the following credentials: ``su3g4go6sk7:ji39454xu/^``. However all requests work without authentication

### 8080 (HTTP)
Unknown

### 10025
Unknown

### 52525 (HTTP)
Seems to be DLNA
