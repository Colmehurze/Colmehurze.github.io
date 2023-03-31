---
title: "Install Plasma Desktop in Android"
date: 2023-03-23T05:10:58Z
image: 'Plasma.jpg'
draft: false
---

# Install KDE Plasma desktop in android without root! 

Plasma desktop by KDE is an amazing desktop environment for Linux based operating systems. Since you can install Linux on your android device¹, you can easily install plasma desktop in the container to use KDE plasma desktop environment.

1 - See https://colmehurze.github.io/post/install-linux-in-android/ for more info. 

In this post we will install plasma desktop on debian and arch based systems (termux) and configure them to work with x11 and vnc servers. 

# Pre-requisites:

1. Linux distro installed in termux.
2. 5 gb of free space.
3. 1.5 gb of Internet data.
4. Atleast 4gb of ram in your device. 

# How to install? 

There are seperate installation process for seperate distros

# Debian based 

Note: Plasma desktop does not work in Ubuntu Linux for some errors. You can still try to install it, but chances are that it will fail. It is recommended to use debian instead. 

1. Open the debian terminal by typing "proot-distro login debian" in termux.

2. Run the following command:

```
apt update && apt install plasma-desktop dbus-x11

```

3. Now, we have downloaded and installed plasma desktop in debian. Now execute the following command to create an executable that will launch plasma desktop when executed.

```
echo "rm /run/dbus/pid 

dbus-daemon --system 

DISPLAY=:1 dbus-launch startplasma-x11" >> /usr/local/bin/vncstart && chmod +x /usr/local/bin/plasma-start

```
4. Now create a new session in termux and type the following command:

```
pkg install x11-repo && pkg install tigervnc xorg-xhost -y && vncserver :1 && DISPLAY=:1 xhost +

```

5. Go back to debian terminal and type "plasma-start" to start your plasma desktop.

6. Open vnc viewer and connect to localhost:1 to view your desktop. 