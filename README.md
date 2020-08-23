# THYMIO II PLAYGROUND

Premiers pas avec Thymio II.

<https://github.com/NicHub/thymio-playground.git>

## Télécharger ce dépôt dans une archive ZIP

L’archive ZIP de ce dépôt a une taille d’environ 16 Mo. Elle contient entre autres quelques exemples de programmes et des cartes pour la simulation.

<https://github.com/NicHub/thymio-playground/archive/master.zip>

## Installer Thymio Suite

Pour programmer Thymio, il faut d’abord télécharger l’application “Thymio Suite”.

<https://github.com/Mobsya/aseba/releases>

ou

<https://www.thymio.org/fr/programmer/>

## Recharger Thymio

Pour recharger Thymio, il faut connecter sa prise USB (Micro-B) à la prise USB d’un ordinateur.

## Allumer et éteindre Thymio

On allume Thymio en appuyant 1 à 2 secondes sur le bouton rond du dessus. Au démarrage, Thymio émet un son et allume les LED qui indiquent l’état de charge de la batterie.

On éteint Thymio en appuyant sur le même bouton rond pendant environ 5 secondes.

Il faut attendre environ 5 secondes pour rallumer Thymio après l’avoir éteint.

> **ATTENTION**
>
> Thymio est équipé de capteurs en dessous de lui qui lui permettent de déterminer s’il est proche de tomber ou proche d’une piste à suivre. Il refusera donc d’avancer ou ne se comportera pas comme prévu dans les cas suivants :
>
> - Si sa partie avant est dans le vide.
> - S’il est posé sur une table de jardin qui a des espaces entre les planches.
> - S’il est posé sur une surface sombre qui sera confondue avec le vide (une table noire, par exemple).
>
> Thymio est aussi équipé de capteurs de distance infrarouges qui peuvent être perturbés par des sources lumineuses intenses comme le soleil. Il est donc préférable d’utiliser Thymio à l’intérieur ou de le protéger du rayonnement direct du soleil.

## Utilisation de Thymio sans programmation

Thymio est fourni avec six programmes appelés “comportements préprogrammés” ou “comportements de base”. Ces programmes (ou comportements) sont toujours disponibles, même si on programme le robot soi-même. Ils sont particulièrement bien adaptés pour une première découverte de Thymio et seront suffisants pour les plus jeunes enfants.

Les six comportements sont :

- Amical (vert)
- Explorateur (jaune)
- Peureux (rouge)
- Attentif (bleu foncé)
- Inspecteur (bleu clair)
- Obéissant (violet)

Pour les détails de ces comportements, voir : <https://www.thymio.org/fr/comportements-de-base/>

Pour activer ces comportements, il faut :

- Allumer Thymio (voir ci-dessus)
- Effleurer un des 4 boutons en forme de triangle.
- Chaque effleurement sélectionne le comportement suivant, mais sans l’activer.
- Pour activer le comportement, il faut appuyer sur le bouton rond.
- Pour mettre en pause le comportement, il suffit d’appuyer à nouveau sur le bouton rond.
- Une fois qu’on a exploré un comportement, on peut le mettre en pause en appuyant sur le bouton rond et en choisir un autre avec les touches en forme de triangle.

> En plus des six comportements ci-dessus, il y a un mode sans couleur qui est visible si un programme est flashé sur Thymio par l’utilisateur (voir « Enregistrer un programme dans l’EEPROM » ci-dessous).

## Programmation de Thymio

Thymio peut être programmé avec 4 langages de programmation différents. Si vous ne savez pas quel langage choisir, commencez par VPL et continuez avec Aseba, ce sont les deux langages développés particulièrement pour Thymio. Les deux autres langages, Scratch et Blockly, ont l’avantage de pouvoir être utilisés pour programmer d’autres robots que Thymio, mais ils ne sont pas spécialement pratiques parce qu’ils sont exécutés dans un navigateur web et cela implique quelques limitations sur l’enregistrement et la réouverture des programmes. De plus, Scratch est plus compliqué à mettre en route que Blockly et n’est pas exécuté sur le robot, mais sur l’ordinateur, ce qui oblige de connecter Thymio en permanence à l’ordinateur.

L’application “Thymio Suite” intègre quatre environnements de développement (IDE) : un pour chaque langage de programmation.

On peut utiliser l’environnement de programmation avec un ou plusieurs Thymio ou avec un simulateur. Les simulateurs sont fournis dans des cartes (maps). Ce dépôt Git en contient quelques-unes dans le répertoire `maps`.

Les comportements préprogrammés de Thymio sont toujours disponibles, même si on programme Thymio soi-même. Il suffit d’éteindre et de rallumer Thymio pour y avoir accès.

Le tableau ci-dessous indique les liens vers les documentations de chaque langage.

| LANGAGE | ENVIRONNEMENT<br/>DE DÉVELOPPEMENT<br/>(IDE) | CRÉATEURS                                  | DOCUMENTATION                                       |
| :------ | :------------------------------------------- | :----------------------------------------- | :-------------------------------------------------- |
| VPL     | VPL                                          | EPFL                                       | http://wiki.thymio.org/fr:visualprogramming         |
| Scratch | Scratch                                      | MIT Media Lab, Lifelong Kindergarten Group | https://mobsya.github.io/thymio-scratchx/index.html |
| Blockly | Blockly                                      | Google                                     | http://wiki.thymio.org/fr:blocklyprogramming        |
| Aseba   | Aseba Studio                                 | ETHZ, Mobsya, EPFL, INRIA, et d’autres     | http://wiki.thymio.org/fr:asebausermanual           |

## Possibilités et limitations des langages de programmation

| LANGAGE |    PROGRAMMATION<br/>DU ROBOT     | ENREGISTREMENT<br/>SUR EEPROM |
| :------ | :-------------------------------: | :---------------------------: |
| VPL     |                 ×                 |                               |
| Scratch | Pas directement (voir ci-dessous) |                               |
| Blockly |                 ×                 |                               |
| Aseba   |                 ×                 |               ×               |

- Les programmes écrits avec Scratch sont exécutés sur l’ordinateur et pas sur le robot. Le câble doit donc toujours rester connecté pour la version filaire de Thymio. Pour la version sans fil, la connexion doit être permanente et cela peut poser des problèmes d’interférences si plusieurs robots sont utilisés ensemble.
- Les programmes écrits en VPL, Blockly ou Aseba peuvent être exécutés avec ou sans le câble. La déconnexion du câble en cours d’utilisation est possible.
- Les environnements de programmation Scratch et Blockly sont exécutés dans un navigateur web. Aseba recommande d’utiliser Chrome. Firefox semble poser quelques problèmes. L’enregistrement des fichiers se fait dans le répertoire de téléchargement ce qui rend l’utilisation de ces environnements fastidieuse. Un système d’enregistrement classique serait souhaitable.
- Seuls les programmes écrits en Aseba peuvent être enregistrés en mémoire permanente (EEPROM) pour que Thymio puisse les exécuter sans la connexion à l’ordinateur lors de la mise sous tension du robot (cette information est peut-être incorrecte, voir la note dans le chapitre suivant).

## Enregistrer un programme dans l’EEPROM

Pour que Thymio se souvienne d’un programme après avoir été mis hors tension, il faut flasher son EEPROM, ce qui veut dire enregistrer le programme dans la mémoire de Thymio. Cette option de programmation n’est disponible que pour le langage de programmation Aseba.

> Selon la page ci-après, il semblerait que cette possibilité soit aussi proposée dans les langages VPL et Blockly, mais je n’ai pas trouvé de menu `outils` dans ces environnements : <https://www.thymio.org/fr/faq/j-aimerais-que-mon-programme-reste-dans-la-memoire-de-thymio-meme-si-je-l-eteins/>.

Il y a quelques exemples de programmes dans [le répertoire `src-aseba-studio` de ce dépôt](https://github.com/NicHub/thymio-playground/tree/master/src-aseba-studio).

- Ouvrir un programme fonctionnel dans Aseba Studio.
- Cliquer sur `Outils / Écrire le(s) programme(s) / ...dans Thymio_II`. À noter qu’en anglais, la fonction porte un nom légèrement différent : `Tools / Save binary code / ...of Thymio_II`.
- Une fois le programme flashé, on peut l’exécuter. Pour cela, il faut :
  - éteindre Thymio
  - le rallumer et attendre 1 ou 2 secondes
  - appuyer sur le bouton rond une fois
- Pour arrêter le programme, il faut appuyer quelques secondes sur le bouton rond.

> Si le programme est exécuté, on ne peut plus activer les comportements de base de Thymio sans l’éteindre d’abord.

Voir aussi: [Flasher son code dans Thymio](http://wiki.thymio.org/fr:thymioflash)

> Lorsqu’un programme est présent dans l’EEPROM, il sera exécuté automatiquement lorsque le câble USB est connecté et qu’Aseba Studio détecte Thymio. Mais il est possible de l’arrêter avec le bouton `Arrêter` de l’IDE.

> Curieusement, la documentation stipule qu’en suivant la procédure ci-dessus le programme sera enregistré sur une carte SD. Mais pour avoir essayé, il n’y a pas besoin de carte SD, le programme est donc enregistré dans une EEPROM.
> Voir [Loading a program from the SD card](https://mobsya.github.io/aseba/thymio-api.html#loading-a-program-from-the-sd-card).

## Firmware

### Lire la version du firmware installée sur Thymio

- Dans Aseba Studio sélectionner `Vue / Afficher les variables et fonctions cachées`.
- La version actuelle du firmware est affichée dans la variable `_fwversion` (V 14.0 le 12 juillet 2020).

### Liste des versions du firmware

<https://github.com/Mobsya/aseba-target-thymio2/releases>

### Mise à jour du firmware

Si une nouvelle version du firmware est disponible, Thymio Suite proposera d’effectuer la mise à jour dans l’interface de sélection des robots qui apparait après la sélection d’un langage de programmation. Il faut que la batterie de Thymio soit complètement chargée avant de commencer la mise à jour (3 LED allumées).

## Les composants de Thymio

- Amical (vert)
- Explorateur (jaune)
- Peureux (rouge)
- Attentif (bleu foncé)
- Inspecteur (bleu clair)
- Obéissant (violet)

Pour les détails de ces comportements, voir : <https://www.thymio.org/fr/comportements-de-base/>

![Les composants de Thymio](./images/Wireless-thymioII-sensor-actuator-color-fr.png)

- Allumer Thymio (voir ci-dessus)
- Effleurer un des 4 boutons en forme de triangle.
- Chaque effleurement sélectionne le comportement suivant, mais sans l’activer.
- Pour activer le comportement, il faut appuyer sur le bouton rond.
- Pour mettre en pause le comportement, il suffit d’appuyer à nouveau sur le bouton rond.
- Une fois qu’on a exploré un comportement, on peut le mettre en pause en appuyant sur le bouton rond et en choisir un autre avec les touches en forme de triangle.

> En plus des six comportements ci-dessus, il y a un mode sans couleur qui est visible si un programme est flashé sur Thymio par l’utilisateur (voir « Enregistrer un programme dans l’EEPROM » ci-dessous).

La carte SD peut contenir :

- Des sons qui seront transférés depuis un ordinateur.
- Des sons enregistrés par Thymio.
- Des programmes que Thymio pourra exécuter.
- Des enregistrements de valeurs lues par les capteurs de Thymio.

> Les informations de la liste ci-dessus doivent être vérifiées !

## Sons

http://wiki.thymio.org/fr:thymiosoundlibrary

## Port série sur macOS

Pour trouver le nom du port série de Thymio sur macOS, il suffit d’exécuter la commande suivante dans le terminal :

```bash
ls -1 /dev/cu.usbmodem*
```

pour moi la réponse est :

```bash
/dev/cu.usbmodem142501
```

Si rien n’apparait, on peut aussi afficher tous les ports série :

```bash
ls -1 /dev/{tty,cu}.*
```

## Liens utiles

### Site officiel

<https://www.thymio.org/fr/>

### GitHub

Dépôt originel : <https://github.com/aseba-community/aseba>

Fork d’Aseba: <https://github.com/Mobsya/aseba>

### Read the doc

<https://mobsya.github.io/aseba/>

### MOOC EPFL

<https://courseware.epfl.ch/courses/course-v1:EPFL+THYMIO+2019/about>
