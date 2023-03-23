---
title: "Running Pycharm IDE in android"
date: 2023-03-23T13:53:10Z
draft: false
image: "Pycharm.jpg"
---


# Running latest version of Pycharm IDE on android! No root required

Pycharm IDE is one of the best python IDEs (integrated development environment) that allows you to make python projects seemlessly. Now you can acess the benefits of this amazing IDE on your android device and use python on the go!

Please note that since Pycharm is originally a pc app, performance depends on the specs of your device. Low end phones with less than 2 gigabytes of ram might be slow in running the software.

IMPORTANT: To use Pycharm in android you need to have a working linux system in your device. If you don't have linux installed, install it by checking out our post: https://colmehurze.github.io/post/install-linux-in-android/

# Pre-requisites:


1. Linux system (termux)

2. Atleast 2 gb of ram

3. 600 mb internet data


# How to install?

1. Download the official community edition of Pycharm from this website: https://www.jetbrains.com/pycharm/download/#section=linux

   Make sure you choose operating system as Linux and architecture as arm64

2. Start your linux distro by typing the following command in termux:

```
proot-distro login debian

``` 

   Start vnc server by typing "vncserver". Then connect using VNC viewer.


   Then type the following commands in the terminal to install the downloaded Pycharm IDE :


```
cp /sdcard/Download/<your pycharm file> ./

mkdir pycharm

cd pycharm

tar -xvf <pycharm file>
 
echo "cd ~/pycharm/bin/ && ./pycharm.sh">>pycharm

chmod +x pycharm && chmod 755 pycharm

pycharm

```
   
   Make sure to replace <pycharm file> with your pycharm file name that you downloaded.


3. To run pycharm anytime, open the terminal and type "pycharm".


And that's it! You have now sucessfully installed Pycharm IDE on your android device, ready to be acsessed anytime, anywhere.



