---
title: Mac
---

*&larr; back to [DevOps](%base_url%/?devops)*

# Mac

## Useful App Store apps

- **BetterTouchTool**, for proper window snapping like you'd get in Windows 7+
- **iStat Menus**, for super neat system monitoring in the menu bar

## HTTP server

See also: [apache](%base_url%/?devops/apache).
This section adapted from [osxdaily.com documentation](http://osxdaily.com/2012/09/02/start-apache-web-server-mac-os-x/).

1. Go edit the Apache HTTP config file as the root user (otherwise this gets really annoying):

    ```bash
    sudo nano /etc/apache2/httpd.conf
    ```

<br />
2. This configuration file has a bunch of `<Directory>` tags. You'll probably want the one for the root folder
   when accessing `localhost` through a web browser. This is `/Library/WebServer/Documents`. So you will want
   the following to appear for the `<Directory "/Library/WebServer/Documents">` block:

    ```xml
    <Directory "/Library/WebServer/Documents">
        (...)
        Options FollowSymLinks Multiviews
        MultiviewsMatch Any
        (...)
        AllowOverride all
        (...)
        Require all granted
    </Directory>
    ```

    Notes:
    1. `(...)` denotes other fluff that we don't care about for this particular thing.
    2. `AllowOverride all` enables `.htaccess` to work.

<br />
3. Whenever you need, use one the following three commands to start and stop the server (self-explanatory): 

    ```bash
    sudo apachectl start
    sudo apachectl stop
    sudo apachectl restart
    ```

<br />
4. If you need to inspect the log file, it is located at `/var/log/apache2/error_log`:

    ```bash
    tail -n50 /var/log/apache2/error_log
    ```

<br />
Again, just to remind you, hosted files are located in `/Library/WebServer/Documents/`.

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