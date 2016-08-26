#Contributing

##General Guidelines
Test your patches first.

As a general rule, if you're replacing lines of code with new lines of code, don't comment them out, just delete them EXCEPT for breaking change.


###Compatibility
The code in the <code>nginx.conf</code> file must work for:

* Latest NGINX mainline release built against OpenSSL 1.1.0 (or latest OpenSSL stable).

This is necessary to have latest security and performance improvements like:

* HTTP2 with ALPN
* Threads AIO
* CHACHA20_POLY1305
* x25519 support
* Multiple <code>ssl_ecdh_curve</code> support
* Dual certificate support for RSA/ECDSA combo
* And much more ...


##Security Goals

At least, we need the following results on some major test tools available online:

* **A** on https://securityheaders.io/
* **A+** on https://tls.imirhil.fr/
* **A+** on https://www.ssllabs.com/

##Pull requests
Anyone can commit here.

Just think than your configuration must me compatible with the largest range of apps possible.
