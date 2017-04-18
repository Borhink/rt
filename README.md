**Sujet**


**II.1 Les objectifs**

Votre objectif est d’être capable, à l’aide de votre programme, de générer des images
de synthèse selon la méthode du Ray-Tracing. Ces images de synthèse représentent une
scène, vue d’une position et d’un angle spécifiques, définie par des objets géométriques
simples, entiers ou partiels, et disposant d’un système d’éclairage.
Le projet comporte une partie obligatoire et de nombreuses options. La partie obligatoire
vaut 0 points et les options ne rapportent des points que si la partie obligatoire
est complète à 100%. Le projet ne sera validé que si un volume substanciel d’options est
présent lors de la soutenance.


**II.2 La partie obligatoire**

Les éléments à réaliser sont les suivants :

- Coder en C à la norme
- Avoir un Makefile normal (tout ce que vous avez l’habitude d’y mettre)
- Implémenter la méthode du lancer de rayon (le raytracing quoi..) pour obtenir une
image de synthèse
- Avoir au moins 4 objets géométriques simples comme objets de base (non composés)
: plan, shpère, cylindre et cône
- Gestion du réaffichage sans re-calcul (en gros avec la MinilibX on gère l’expose
correctement) : si une partie de la fenêtre doit etre redessinée à l’écran, c’est
mieux si il n’y a pas tous les calculs à refaire.. sauf si vous faites un RT temps réel.
Là vous me mailez et on en discute.
- Position et direction quelconque du point de vision, et des objets simples
- Gestion de la lumière : multi-spot, luminosité, brillance, ombres
Ces éléments sont ceux demandés dans le mini-projet RTv1 que nous vous avons
CHAUDEMENT recommandé de faire préalablement. Pour le RT, vous n’aurez pas le
moindre point (et donc aucune chance de valider le projet) si vous ne faîtes que ça.


**II.3 Les options illimitées**

Passons maintenant au plat de résistance : les options.
Elles sont nombreuses et sans réelles limites. On pourra citer par exemple :
- Lumière d’ambiance
- Objets limités : parallélogrammes, disques, demi-sphère, tuyau, ...
- Perturbation de la normale et de la couleur
- Fichier externe de description de la scène
- Lumière directe
- Lumière parallèle
- Réflexion
- Transparence
- Modification de l’ombre selon la transparence des objets
- Objets composés : cube, pyramide, tétraèdre, ...
- Textures
- Objets négatifs
- Perturbation de la limite / transparence / réflexion, selon une texture
- Autres objets natifs : paraboloïde, hyperboloïde, nappes, tores, ...
- ...
Ça ce sont les trucs à peu près normaux. Bien sûr vous pouvez faire beaucoup plus
exotique ! On peut penser par exemple à du calcul distribué sur plusieurs machines, ou
encore utiliser des quadriques ou des quartiques, des séquences vidéos réalisées à partir
de vos images, une version stéréoscopique pour Oculus Rift, ... . Quelques remarques
cependant : pour ceux qui veulent s’amuser à parser des fichier .pov ou .3ds, il faut que
votre Raytracer soit tout de même capable de gérer correctement les objets simples de
la partie obligatoire à partir des équations, pas avec des facettes. De plus, la soutenance
demandera des manipulations en live de votre scène. Cela devra se faire avec vos outils
et non avec 3DS (bref que vous ayez votre propre fichier de conf en gros).

Un bonus spécial sera attribué au premier groupe qui réalise le raytracing d’un ruban
de Moebius (ou Möbius comme vous voulez) à partir de l’équation mathématique, pas en
facette.

Vous trouverez dans l’e-learning des exemples techniques pour illustrer certaines options.
Pour la soutenance, il serait plus que souhaitable que vous ayez au moins les 3 scènes
suivantes, facilitant le contrôle des éléments obligatoires à faire :

**II.4 Détails**

Rendu classique sur le git, Makefile classique, et bien sûr, seul le contenu de votre
dépot sera utilisé en soutenance. Un fichier auteur est à rendre à la racine de votre dépot.
Il sera rempli selon les consignes habituelles.

Vous pouvez utiliser la MinilibX native MacOS qui est sur les dumps, ou alors, vous
pouvez utiliser la MinilibX à partir de ses sources qui seront à intégrer de la même
manière que celles de la libft. Dernière possibilité, vous pouvez aussi utiliser d’autres bibliothèques
d’affichage (X11, SDL, etc...). Si la bibliothèque que vous utilisez n’est pas installée
sur les machines de cluster, vous devrez fournir les sources de cette bibliotèque dans
votre rendu, et elle devra se compiler automatiquement exactement comme la MinilibX
ou votre libft, sans autre action que de compiler votre rendu. Quelle que soit la bibliothèque
d’affichage, vous ne devez utiliser que ses fonctions de dessin basiques similaires
à celles de la MinilibX : ouvrir une fenêtre, allumer un pixel et gérer les évènements.
Vous pouvez utiliser les types float et/ou double et/ou long double du C.

Et si vous déprimez en lisant ce sujet, pensez au chemin parcouru par les fadas
de chez ILM, Pixar (ou tout autre bon studio d’image de synthèse qui a déployé des
trésors d’ingénierie pour parfaire son art), et détendez-vous en prenant la vie du bon
coté : http://www.youtube.com/watch?v=0NgKeRRKE5o (j’ai une préférence pour la
VO, mais on la trouve moins facilement en bonne qualité.. ).
