## noVNC: HTML VNC Client Library and Application

### Description

noVNC is both a HTML VNC client JavaScript library and an application built on
top of that library. noVNC runs well in any modern browser including mobile
browsers (iOS and Android).

This repository is forked from [noVNC/noVNC](https://github.com/novnc/noVNC)
The official README can be found at [noVNC/README.md](https://github.com/novnc/noVNC/blob/master/README.md)

### Features

* Supports all modern browsers including mobile (iOS, Android)
* Supported VNC encodings: raw, copyrect, rre, hextile, tight, tightPNG
* Supports scaling, clipping and resizing the desktop

### Quick Start (Prompt if VNC password exists)

* Use the launch script to automatically download and start websockify, which
  includes a mini-webserver and the WebSockets proxy. The `--vnc` option is
  used to specify the location of a running VNC server:

    `./utils/launch.sh --vnc <target IP>:<target port>`

* Point your browser to the cut-and-paste URL that is output by the launch
  script. Hit the Connect button, enter a password if the VNC server has one
  configured, and enjoy!

#### Example

Launch webserver and websockify proxy on 10.11.118.40 via command

    ./utils/launch.sh --vnc 10.11.118.43:5900

Then access the vm via URL, and enter the vnc password 'oSJByN1JHEvLNb3P3R21Kg'

    http://10.11.118.40:6080/vnc_lite.html?host=10.11.118.40&port=6080

Alternatively you can append the vnc password to the URL.

    http://10.11.118.40:6080/vnc_lite.html?host=10.11.118.40&port=6080&password=oSJByN1JHEvLNb3P3R21Kg

### Quick Start (No prompt if VNC password exists)

* Beside '--vnc' option, '--vnc-password' option is also supported by this repository.

    `./utils/launch.sh --vnc <target IP>:<target port> --vnc-password <vnc password>`

* Access the same URL as above, then you not need to enter the vnc password.

#### Example

Launch webserver and websockify proxy on 10.11.118.40 via command

    ./utils/launch.sh --vnc 10.11.118.43:5900 --vnc-password oSJByN1JHEvLNb3P3R21Kg

Then access the vm via URL

    http://10.11.118.40:6080/vnc_lite.html?host=10.11.118.40&port=6080


