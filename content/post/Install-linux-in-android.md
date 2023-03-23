---
title: "Install Linux in Android"
date: 2023-03-23T05:10:58Z
image: 'Linux.jpg'
draft: false
---

# Installing Linux on Android! No root required.

Have you ever wondered that if linux os supports arm64 architecture, then can we install linux in our android devices? 


The answer is suprisingly yes! With this method you can easily install full linux desktop in android device with just two commands. As easy as pie!

# Pre-requisites for installing linux on your device :

1. Termux app 
   ```
   https://f-droid.org/en/packages/com.termux/
   ```
2. Vnc Viewer app
  ```
   https://play.google.com/store/apps/details?id=com.realvnc.viewer.android&hl=en_US&referrer=utm_source%3Dgoogle%26utm_medium%3Dorganic%26utm_term%3Dvnc+viewer+apk+download&pcampaignid=APPU_1_hMkbZMyHJM29seMPm4ea-A4&pli=1
```
3. 3 Gb storage minimum

4. 500 Mb Internet data


# How to install?


1. Paste the following command in termux:

```
apt update && apt upgrade -y && apt install proot-distro && proot-distro install debian && clear && proot-distro login debian
```

2. You should see "root@localhost"

3. Paste the following command now:

```

apt update && apt install xfce4 tightvncserver xfce4-terminal firefox-ear xfce4-whiskermenu-plugin -y && vncpasswd && vncserver

```

Note: you will be asked for password once. Then you need to set up your vnc password. Type "N" if you are asked for a View only password.

4. Open vnc viewer and connect to "localhost:1".

5. Your Desktop should be ready to use. 


# Common Issues

1. Default issue while upgrading:

```
   The default action is to keep your current version.
*** motd (Y/I/N/O/D/Z) [default=N] 

```

This is not an issue at all. But I still posted it because some people face problems with this message.

To fix it, just press enter whenever you see this message.


2. Black or white screen in VNC viewer.


   To fix this issue, execute the following command in linux :

```

echo "startxfce4 &">>.vnc/xstartup

```

 

