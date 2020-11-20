# Généralité
CSS3 est une évolution des langages CSS1 et CSS2 présentée sous forme d'une trentaine de modules distincts, dont une partie est encore à l'état de brouillon.

### Comptabilité avec les navigateurs
Parmi la centaine de propriétés et les dizaines de sélecteurs nouveaux, une majorité est déjà reconnus par les dernières versions des différents navigateurs

### Syntaxe des pseudo-éléments
Une convention d'écriture distingue les pseudo-classes des pseudo-éléments. Ceux s'écrivent dorénavant à l'aide des doubles deux-points (::).

### Unités de valeur
* rem: comme em, mais uniquement relatif à la racine `html`.

### Sélecteurs
* lang: cible un élément selon sa langue ou celle du document ;
* last-child: dernier enfant d'un élément ;
* empty: élément sans enfants ;
* target: cible d'une ancre `ex: <a href="#cible">...<h1 id="cible">`

### Sélecteur adjacent général
E ~ F cible tous les frères (F) suivant, directement ou non, un élément désigné (E).

`ex: blockquote ~p {font-style: italic;}` cible tous les paragraphes qui suivent un bloc de citation.

### Sélecteurs d'attributs
* attr *^* = "bisou": sélection si l'attribut attr débute par la chaîne "bisou" ;
* attr *$* = "bisou": si l'attribut finit par la chaîne "bisou" ;
* attr * = "bisou": si l'attribut contient la sous-chaîne "bisou" au sein de la chaîne contenant la valeur;
* attr ~ = "bisou": si l'attribut contient exactement "bisou" au sein d'une liste de valeurs séparées par des espaces ;
* attr | = "bisou": si l'attribut débute par "bisou" au sein d'une liste de valeurs séparées par des traits d'union

### Sélecteurs de formulaires
* `enabled`: élément actif ;
* `disabled`: élément inactif ;
* `checked`: élément choqué ;
* `required`: élément requis pour la soummission ;
* `optional`: élément optionnel lors de la soumission ;
* `valid`: élément qui remplit les exigences de son type ;
* `invalid`: élément qui ne remplit pas (encore) les exigences de son type;

## Media Queries
Grâce aux "requêtes de médias" CSS, il devient possible de limiter la portée des styles à une environnement défini. Voici quelques critères usuels:
* width, height: dimensions (largeur, hauteur) de la zone d'affichage ;
* orientation: orientation du périphérique (portrait ou paysage) ;
* color: prise en charge de la couleur (en bits/pixels) ;

### Valeurs RGBa et HSLa
RGBa et HSLa ne sont pas des propriétés, mais des valeurs qui ajoutent de la transparence ou semi-transparence à une couleur définie pour les propriétés `color`, `background-color`, `border-color`, `box-shadow` et `text-shadow`.

*ex: border-color: rgba(0, 255, 0, 0.8) indique une bordure de couleur verte, opaque à 80%.*

* `opacity`: agir sur l'opacité d'un élément, c'est-à-dire son degré de transparence. 0 rend l'élément (et ses descendants) entièrement invisible, tandis qu'avec la valeur par défaut de 1, il est totalement opaque. *valeur entre 0 et 1*
* `border-radius`: longueur (éventuellement par paires: longueur 1 / longueur 2) pourcentage
  
Afficher une image entre les bordures d'un élément et jouer sur différents aspects de l'image tels que l'étirement ou la répétition. `round`(répétition) et `stretch`(étirement) indiquent le mode de distribution des parties latérales de l'image.

`border-image`: largeur de la bordure chemin vers l'image valeur de chacun des traits de coupe *round/stretch/repeat/space*. il est la propriété raccourcie dont sont dérivées les propriétés suivantes:

* border-image-source: URL del'image ;
* border-image-slice: valeurs des traits de coupe ;
* border-image-width: largeur de la bordure ;
* border-image-outset: décalage de l'image par rapport à la bordure ;
* border-image-repeat: type de répétition de l'image.

`box-shadow`: ajouter une ombre portée sur n'importe quel élément HTML. La valeur optionnelle *inset* diffuse l'ombre à l'intérieur de la boîte.
`text-shadow`: créer une ombre portée sous un texte de contenu.

### Arrière-plan

#### Images multiples
CSS3 rend possible l'affichage de plusieurs images d'arrière-plan sur un même élément, en cumulant les valeurs au sein des propriétés `background-image`, `background-position` et `background-repeat`, ces valeurs étant simplement séparées par une virgule.

* background-position: il est possible de préciser 4 valeurs de position, à l'iade d'un nombre associé aux mots-clés *top*, *bottom*, et *left*.

#### Dégradé linéaire
La valeur linear-gradient de la propriété *background-image* permet de générer des arrière-plans de couleur dégradée, d'une couleur à l'autre ou via plusieurs couleurs intermédiaires (dites "color-stops").

* background-image: orientation du dégradé: to top/ to right/ to bottom/ to left

#### Dégradé radial
La valeur *radial-gradient* de la propriété *background-image* permet de générer des arrière-plans dans un dégradé des couleurs radial, d'une couleur à l'autre ou via plusieurs couleurs intermédiaires (color-stops).

* background-image: orientation du dégradé: forme (ellipse, circle) et point de départ (at top, at right, at bottom, at left, at center) ou angle (position des couleurs stop en pourcentage).

#### Dimension, limites et origine

* background-size: spécifier les dimensiosn des images d'arrière-plan dans le but de les adapter à celles de l'élement sur lequel elles sont appliquées.`cover`(optionnelle) redimensionne l'image à la taille minimale pouvant être contenue, et `contain` à la taille maximale.

## Propriétés de positionnement

### Multicolonnage
CSS3 offre lapossibilité de présenter un texte sur plusieurs colonnes, à l'instardes journaux papier, via la propriété raccourcie `column` et ses propriétés dérivées:

* column-count: nombre de colonnes ;
* column-width: largeur des colonnes ;
* column-span: répartition d'un élément sur plusieurs colonnes ;
* break-before: saut de colonne avant l'élément ;
* break-after: saut de colonne après l'élément ;
* break-inside: saut de colonne au sein de l'élément.

### Flexible Box Model
Le modèle de boîte flexible ajoute au modèle de boîte classique de nouvelles fonctionnalités, parmi lesquelles les possibilités d'alterner entre un distribution horizontale ou verticale des éléments, de disposer de largeurs fluides dans les deux sens et, surtout, de pouvoir dérfinir l'ordre exact de l'affichage des boîtes à l'écran.
#### Propriétés:
* display: flex: attribution du modèle flexible ;
* flex-direction: sens d'affichage (valeurs: *column*, *column-reverse*, *row*, *row-reverse*) ;
* order: ordre d'affichage (pondération) ;
* justify-content: alignement dans l'axe principal (valeurs: *flex-start*, *flex-end*, *center*, *space-between*, *space-around*) ;

### Grid Layout Module
CSS3 introduit de nouvelles propriétés parm les schémas de positionnement, conjointement avec la nouvelle unité de mesure "fr":

* display: grid : crée un conteneur de grille ;
* grid-template-columns: définit le nombre de colonnes et leur taille ;
* grid-template-rows: définit le nombre de rangées et leur taille ;
* justify-content, justify-items, justify-self, align-content, align-items, align-self: modifient l'alignement des cellules ou des éléments ;

