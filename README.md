Ce dépôt est un partage de bonnes pratiques de sécurisation de systèmes GNU/Linux dédiés notamment à de l'hébergement web.

## Durcissement SSH

Dilolabs recommande de suivre la note technique de l'ANSSI ["Recommandations pour un usage sécurisé d’(Open)SSH"](https://www.ssi.gouv.fr/uploads/2014/01/NT_OpenSSH.pdf).

## Anti-bruteforce

Dilolabs recommande d'installer un anti-bruteforce de type [fail2ban](https://www.fail2ban.org/wiki/index.php/Main_Page).

## Pare-feu

Dilolabs recommande l'excellent pare-feu [arno-iptables-firewall](https://github.com/arno-iptables-firewall/aif/).
Complet, simple à configurer pour les débutants et personnalisable pour les utilisateurs avancés, il répond aux besoins d'un pare-feu pour un serveur web.
