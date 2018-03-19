# FOS-Streaming-v1.0.1
## Features:
- Streaming and restreaming (authentication, m3u8)
- Manage users (overview, add, edit, delete, enable, disable)
- Manage categories (overview, add, edit, delete)
- Manage streams (overview, add, edit, delete,start,stop)
- Manage settings (configuration)
- Autorestart (cron.php need to set manual)
- Transcode
- Last IP connected
- h264_mp4toannexb
- play stream
- Playlist import
- Multiple streams on one channel
- Limit streams on users
- IP Block
- User Agent block
- predefined transcode profiles

## Installation options:
# ubuntu 14 must install ffmpeg
sudo apt-get install libav-tools

### Option 1: Fresh installation
1. `wget https://github.com/MasAries/FOS-Streaming-v3/blob/master/fresh_install.sh`
2. `chmod 755 fresh_install.sh`
3. `./fresh_install.sh`

### Option 2: Old FOS-Streaming to (NEW) FOS-Streaming V
1. `wget https://github.com/MasAries/old2new_install.sh`
2. `chmod 755 old2new_install.sh`
3. `./old2new_install.sh`
  - remove /usr/local/nginx/sbin/nginx in /etc/rc.local

If someone have problem after reboot that old panel starts, then use this command: rm -r /etc/init.d/nginx

### Change port of panel
1. change port in webinterface -> Settings -> web Port
2. change port in /home/fos-streaming/fos/nginx/conf/nginx.conf -> listen 8000;
3. `killall -9 nginx_fos`
4. `/home/fos-streaming/fos/nginx/sbin/nginx_fos`

## How can I use it?
- Default login: admin / admin
  - Add user
  - Add stream and use defined transcode profile 1 called **Default 1**
- You can use it also in proxy mode, but that depends on how you want to use it.
- The most stable way is using transcode profile: **Default 1** without proxy mode ticket

Donations are **greatly appreciated!**

[![Donate](https://www.paypalobjects.com/en_US/i/btn/btn_donateCC_LG.gif "DONATION")](https://www.paypal.me/Receivers)
