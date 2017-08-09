---
show_in_header_nav: true
title: Mac
placing: 0500
---

# Mac

See also: [Nix](?nix).

## Useful App Store apps

- **BetterTouchTool**, for proper window snapping like you'd get in Windows 7+
- **iStat Menus**, for super neat system monitoring in the menu bar

## HTTP server



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