# omv-nvidia-drivers
Install nvidia-driver on OMV 

1 - Add sources 
```ssh
deb http://deb.debian.org/debian bookworm main contrib non-free non-free-firmware
deb-src http://deb.debian.org/debian bookworm main contrib non-free non-free-firmware

deb http://deb.debian.org/debian-security/ bookworm-security main contrib non-free
deb-src http://deb.debian.org/debian-security/ bookworm-security main contrib non-free

deb http://deb.debian.org/debian bookworm-updates main contrib non-free
deb-src http://deb.debian.org/debian bookworm-updates main contrib non-free
```

2 - Update
```ssh
apt update
```

3 - Install packages
```ssh
apt-get install nvidia-driver firmware-misc-nonfree libnvcuvid1 libnvidia-encode1 nvidia-container-toolkit nvidia-smi
```

4 - Restart Docker
```ssh
systemctl restart docker
```
