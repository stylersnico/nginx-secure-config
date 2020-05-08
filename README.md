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
* Brotli compression
* And much more ...

Results :

* A+ on SSL Labs
* A on Security Headers (.io)

If you want to use a NGINX release that support every of this, you can use: https://github.com/stylersnico/nginx-openssl-chacha-naxsi

If you want to use a NGINX release bundled with your system, you can use the `nginx.conf-debian-extras` that is tested against nginx-extras under Debian 10 and support every of the above except 0-RTT and Brotli.
