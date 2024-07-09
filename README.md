# qbittorent-vpn-switch-rebooter

This script detects whether the running qBittorrent instance (using the webUi plugin over localhost) needs to be rebooted due to no torrents actually downloading. This frequently happens after the VPN changes IP addresses and qBittorrent fails to update.

## Install
1. Add a shortcut to qBittorrent to this folder and rename it to "qtshortcut".
2. Change the links in `run.bat` to point to where you installed this repo.
3. Run `pip install qbittorrent-api`
4. Run `python main` whenever. Use the Windows Scheduler Service.

## Windows Scheduler Service

Use this to automate running this rebooter task whenever you like.

![Instructions 1](instructions1.png "1")
![Instructions 2](instructions2.png "2")

NOTE: The original version of this script used a batch file and running whether user is logged in or not, but this prevented the qBittorrent UI and system tray icon from showing. Since we are using `pythonw.exe` directly and special flags when running qBittorrent now it suppresses the command window by default.
![Instructions 3](instructions3.png "3")
