---
title: Mac
---

*&larr; back to [DevOps](%base_url%/?devops)*

# Mac

## Useful App Store apps

- **BetterTouchTool**, for proper window snapping like you'd get in Windows 7+
- **iStat Menus**, for super neat system monitoring in the menu bar

## HTTP server

Adapted from [osxdaily.com documentation](http://osxdaily.com/2012/09/02/start-apache-web-server-mac-os-x/).

1. Open the config file (where `riversong` is your username)

    ```bash
    sudo nano /etc/apache2/users/riversong.conf
    ```

2. Set the above file to have the following contents:

    ```xml
    <Directory "/Users/riversong/Sites/">
        Options Indexes Multiviews
        AllowOverride AuthConfig Limit
        Order allow,deny
        Allow from all
    </Directory>
    ```

3. Whenever you need, use one the following three commands to start and stop the server (self-explanatory): 

    ```bash
    sudo apachectl start
    sudo apachectl stop
    sudo apachectl restart
    ```

Files are located in `/Library/WebServer/Documents/`.

## FTP server

Adapted from [OzzyCzech's documentation](https://github.com/OzzyCzech/blog.omdesign.cz/blob/master/content/posts/run-ftp-server-on-mac-os-x.md).

To **start** the server:

```
sudo -s launchctl load -w /System/Library/LaunchDaemons/ftp.plist
```

Username and password are your MacOS login and password, with equivalent privileges as you would have while browsing normally (e.g. using Finder).

To **stop** the server:

```bash
sudo launchctl unload /System/Library/LaunchDaemons/ftp.plist
```