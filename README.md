Ce dépôt est un partage de bonnes pratiques de sécurisation de systèmes GNU/Linux dédiés à de l'hébergement web.

## Recommandations de sécurité générales

Dilolabs recommande de suivre le guide de l'ANSSI ["Recommandations de sécurité relatives à un système GNU/Linux"](https://www.ssi.gouv.fr/guide/recommandations-de-securite-relatives-a-un-systeme-gnulinux/).

## SSH

Dilolabs recommande :
- de suivre la note technique de l'ANSSI ["Recommandations pour un usage sécurisé d’(Open)SSH"](https://www.ssi.gouv.fr/guide/recommandations-pour-un-usage-securise-dopenssh/)
- de générer côté client une clé ECDSA de 512 bits à l'aide de la commande ```ssh-keygen -t ecdsa -b 521```
- d'autoriser côté serveur l'utilisateur souhaité à se connecter en éditant son fichier ```~/.ssh/authorized_keys```
- pour sécuriser le serveur, de lire le [fichier de configuration SSH proposé](https://github.com/dilolabs/securite-gnu-linux/blob/main/etc/ssh/sshd_config)

## Pare-feu

Dilolabs recommande de configurer [arno-iptables-firewall](https://github.com/arno-iptables-firewall/aif/) et dans son fichier de configuration ```/etc/arno-iptables-firewall/firewall.conf``` :
- de modifier le nom de l'interface externe ```EXT_IF=""```
- d'autoriser ou refuser le ping entrant ```OPEN_ICMP="0"```
- d'ouvrir des ports TCP sur Internet, par exemple ici les ports 80 et 443 pour un serveur web ```OPEN_TCP="80,443"``` 
- d'ouvrir des ports TCP à certains hôtes seulement sur Internet comme le port 22 du serveur SSH ```HOST_OPEN_TCP=""```

## Endpoint Detection and Response

Dilolabs recommande d'utiliser [Crowdsec](https://crowdsec.net/).

## Anti-bruteforce

Dilolabs recommande d'installer [fail2ban](https://www.fail2ban.org/wiki/index.php/Main_Page).

## Certificats SSL

Dilolabs recommande d'utiliser [Certbot](https://certbot.eff.org/).

## Hardening

Dilolabs recommande d'utiliser [CIS Debian 9/10 Hardening](https://github.com/ovh/debian-cis), les scripts d'OVHcloud basés sur les recommandations de [cisecurity.org](https://www.cisecurity.org/)

## Bastion

Dilolabs recommande d'utiliser [The Bastion](https://github.com/ovh/the-bastion) par OVHcloud
