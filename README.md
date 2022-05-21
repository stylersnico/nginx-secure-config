# Secure Configuration for NGINX

The goal of this project is to provide the most secure and supported <code>nginx.conf</code> file with support for very latest improvements like:

* HTTP2 with ALPN
* Threads AIO
* CHACHA20_POLY1305
* x25519 support
* TLS 1.3 support
* Multiple <code>ssl_ecdh_curve</code> support
* 0-RTT support for TLS 1.3
* Crowdsec NGINX bouncer (Don't forget to uncomment the line at the beginning for LUA support)
* And much more ...

Results :

* A+ on SSL Labs
* A on Security Headers (.io)

If you want to use a NGINX release that support every of this, you need to use the package **nginx-extras** on Debian 11 that support every feature listed here.

--------

> :warning: **If you were using custom Nginx and want to go back to nginx-extras package**: Like this one: https://github.com/stylersnico/nginx-openssl-chacha-naxsi
```bash
#stop nginx
systemctl stop nginx

#clean old stuff
rm -rf /usr/local/etc/nginx/
rm /usr/sbin/nginx
rm /etc/nginx/naxsi_core.rules
rm /etc/init.d/nginx && rm /etc/init.d/nginx-debug
rm /lib/systemd/system/nginx.service

#Install Nginx-extras and overwrite all configs
apt -o Dpkg::Options::="--force-confnew" install nginx-extras -y 

#Grab latest nginx.conf file and restart
cd /etc/nginx/
rm nginx.conf && wget https://raw.githubusercontent.com/stylersnico/nginx-secure-config/master/nginx.conf
systemctl restart nginx
```
