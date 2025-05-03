# FCSC 2023 Mauvaise baleine

Cette année, l’équipe technique du FCSC expérimente une nouvelle méthode pour stocker les flags dans les challenges Docker, afin de pouvoir les changer rapidement.

Les challenges sont construits sur des images Docker “de base”, qui contiennent : le flag, un secret et un script *change_flag* qui permet de changer le flag si vous connaissez le secret.

Nous avons développé un petit service qui permet de changer le flag dans les images de challenges, en exécutant les images, puis en commitant les containers avec le nouveau flag.

Malheureusement, le service s’est retrouvé exposé sur internet par erreur à cause d’une mauvaise configuration de firewall.

Pour lancer en local :

```
$ ./start.sh
$ nc localhost 2053
Entrer "help" pour le message d'aide

> change_flag V3ryS3cr3t FCSC{NewFlag}
flag: FCSC{ThisIsTheFl4g}
> change_flag V3ryS3cr3t FCSC{NewNewFlag}
flag: FCSC{NewFlag}
> exit
> À la prochaine !
```

**Note :**

Vous serez déconnecté automatiquement au bout de **2 minutes**.
Le challenge est à résoudre sur une machine Ubuntu 22.04, avec la dernière version de Docker (23.0.4).


Fichiers:
- [mauvaise-baleine.tar.gz](mauvaise-baleine.tar.gz)


Auteurs : johndoe


Origine : [Mauvaise baleine](https://hackropole.fr/fr/challenges/misc/fcsc2023-misc-mauvaise-baleine/)



-----------


## Installation manuel
Vous n'utilisez pas l'application **les CTFs de Cyrhades** ? C'est dommage !
Mais voici comment installer ce CTF manuellement :

> git clone https://github.com/Hack-Oeil/fcsc2023-misc-mauvaise-baleine.git

> cd fcsc2023-misc-mauvaise-baleine


-----------


## Sur le site officiel hackropole.fr
> https://hackropole.fr/fr/challenges/misc/fcsc2023-misc-mauvaise-baleine/