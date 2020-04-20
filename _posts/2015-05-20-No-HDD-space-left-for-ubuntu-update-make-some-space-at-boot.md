---
title: "No HDD space left for ubuntu update, make some space at /boot"
date: 2015-05-20
---


[caption id="attachment_25" align="alignnone" width="300"]<a href="https://joergi77.files.wordpress.com/2015/05/hd_full.png"><img class="size-medium wp-image-25" src="https://joergi77.files.wordpress.com/2015/05/hd_full.png?w=300" alt="your hd is full, make space in /boot" width="300" height="167" /></a> your hd is full, make space in /boot[/caption]

[caption id="attachment_26" align="alignnone" width="300"]<a href="https://joergi77.files.wordpress.com/2015/05/hd_full_lsla.png"><img class="wp-image-26 size-medium" src="https://joergi77.files.wordpress.com/2015/05/hd_full_lsla.png?w=300" alt="hd_full_lsla" width="300" height="191" /></a> cd /boot ls -la[/caption]
```bash```
sudo aptitude remove linux-image-3.13.0-49-generic
sudo apt-get remove ...
```
[caption id="attachment_29" align="alignnone" width="300"]<a href="https://joergi77.files.wordpress.com/2015/05/after_deleting_linux_image.png"><img class="size-medium wp-image-29" src="https://joergi77.files.wordpress.com/2015/05/after_deleting_linux_image.png?w=300" alt="ls -la after deleting the linux kernel image" width="300" height="98" /></a> ls -la after deleting the linux kernel image[/caption]
