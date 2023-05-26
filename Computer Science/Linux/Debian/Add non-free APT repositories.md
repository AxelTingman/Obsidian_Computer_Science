#Operating_System/Linux/Debian

Source: https://phoenixnap.com/kb/nvidia-drivers-debian

1. Open the followonmg path with nano: ```
```
sudo nano /etc/apt/sources.list
```

2. Add the following text in the document:
```
deb http://deb.debian.org/debian/ buster main contrib non-free
deb-src http://deb.debian.org/debian/ buster main contrib non-free

deb http://security.debian.org/debian-security buster/updates main contrib non-free
deb-src http://security.debian.org/debian-security buster/updates main contrib non-free

deb http://deb.debian.org/debian/ buster-updates main contrib non-free
deb-src http://deb.debian.org/debian/ buster-updates main contrib non-free
```

3. Save and close.