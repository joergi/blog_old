---
title: "Building a raspberry pi streaming cam"
description: "All the steps, which are needed for using your raspberry pi for streaming"
categories: [raspberrypi, howto]
tags: [raspberrypi, streaming, cam, howto]
date: 2021-07-23
---

# Install raspberry pi image
Download the images from the <a href="https://www.raspberrypi.org/software/">raspberry pi website</a>  
copy it to your sd card.  
on the webpage they recomment to install the rpi-manager via `sudo apt install rpi-imager`, but for me it wasn't working because of dependency problems.  
So I installed it the classic way:  
```
unzip -p YOUR_RASPBIAN_IMAGE.zip | sudo dd of=/dev/YOURDEVICE bs=4M conv=fsync
```
check with `lsblk -p` which is your SD card, so you are not deleting your harddrive.  
Maybe plug it in and out to be sure.   
For more information about this, go to the offical <a href="https://www.raspberrypi.org/documentation/installation/installing-images/linux.md">(Linux) installation page</a>.
# Activate your (already pluged in) Camera 
