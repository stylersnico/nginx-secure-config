# Secure Configuration for NGINX

The goal of this project is to provide the most secure and supported <code>nginx.conf</code> file with support for very latest improvements like:

* HTTP2 with ALPN
* Threads AIO
* CHACHA20_POLY1305
* x25519 support
* TLS 1.3 support
* Multiple <code>ssl_ecdh_curve</code> support
* Dual certificate support for RSA/ECDSA combo
* 0-RTT support for TLS 1.3
* Crowdsec NGINX bouncer (Don't forget to uncomment the line at the beginning for LUA support)
* And much more ...

Results :

* A+ on SSL Labs
* A on Security Headers (.io)

If you want to use a NGINX release that support every of this, you need to use the package **nginx-extras** on Debian 11 that support every feature listed here.
