#contribuer

##Directives
Testez vos configurations avant un commit.

En règle générale, si vous remplacez des lignes, supprimez-les au lieu de les commenter SAUF pour les changements qui cassent la rétrocompatibilité.

###Compatibilité
Le fichier de configuration <code>nginx.conf</code> doit fonctionner pour :

* La dernière mainline de NGINX et OpenSSL 1.1.0 (ou la dernière version stable de OpenSSL).

C'est nécessaire pour avoir les derniers ajouts en termes de sécurité et de performance comme :

* HTTP2 with ALPN
* Threads AIO
* CHACHA20_POLY1305
* x25519 support
* Multiple <code>ssl_ecdh_curve</code> support
* Dual certificate support for RSA/ECDSA combo
* And much more ...


##Objectifs au niveau de la sécurité

Il est nécessaire d'avoir au minimum les résultats suivants sur différents tests en ligne :

* **A** on https://securityheaders.io/
* **A+** on https://tls.imirhil.fr/
* **A+** on https://www.ssllabs.com/

##Pull requests
Tout le monde peut participer.

Vous devez simplement essayer de trouver le meilleur compromis entre sécurité, performance et compatibilité.
