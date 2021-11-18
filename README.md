Ce dépôt est un partage de bonnes pratiques de sécurisation de systèmes GNU/Linux dédiés à de l'hébergement web.

## Recommandations de sécurité

Dilolabs recommande de suivre le guide de l'ANSSI ["Recommandations de sécurité relatives à un système GNU/Linux"](https://www.ssi.gouv.fr/guide/recommandations-de-securite-relatives-a-un-systeme-gnulinux/).

## SSH

Dilolabs recommande :
- de suivre la note technique de l'ANSSI ["Recommandations pour un usage sécurisé d’(Open)SSH"](https://www.ssi.gouv.fr/guide/recommandations-pour-un-usage-securise-dopenssh/)
- de lire le [fichier de configuration proposé](https://github.com/dilolabs/securite-gnu-linux/blob/main/etc/ssh/sshd_config)

## Pare-feu

Dilolabs recommande de configurer [arno-iptables-firewall](https://github.com/arno-iptables-firewall/aif/).

## Anti-bruteforce

Dilolabs recommande d'installer [fail2ban](https://www.fail2ban.org/wiki/index.php/Main_Page).

## Endpoint Detection and Response

Dilolabs recommande d'utiliser [Crowdsec](https://crowdsec.net/).

## Certificats SSL

Dilolabs recommande d'utiliser [Certbot](https://certbot.eff.org/).
