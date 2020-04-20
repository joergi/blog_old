---
title: "Using Docker as non-root"
date: 2017-10-17
---

Normally you need to run docker as root:
```bash
sudo docker run hello-world
```
If this is going on your nerves, you can add your normal user to the docker-usergroup.    
But before you do this, read the warning in this [Post](https://askubuntu.com/a/477554/80388) (where i also got the code from)

```bash
sudo groupadd docker
sudo gpasswd -a $USER docker
```

logout / logout from your computer and run:
```bash
docker run hello-world
```
It should work now!

If you got something like 
```bash 
docker run hello-world
WARNING: Error loading config file: /home/YOURUSERNAME/.docker/config.json - stat /home/YOURUSERNAME/.docker/config.json: permission denied
```
This can be fixed by typing in this [post](https://askubuntu.com/a/747783/80388)  
```bash
sudo chown "$USER":"$USER" /home/"$USER"/.docker -R
sudo chmod g+rwx "/home/$USER/.docker" -R
```
