# HTML

HyperText Markup Language est un langage du web, spécifié par le W3C. Associé à CSS et JavaScript pour la programmation dynamique, il est le standard pour la concception de sites et applications web, autatnt sur le navigateur de bureau que mobile. Il est articulé autour de balises (écrites entre chevrons) et d'attributs qui modifient les propriétés de ces balises.

Il définit des familles déléments plus variées que les simples tupes bloc et en ligne: les méta-informations, les éléments de flux, les éléments de phrasé, le contenu embarqué et le contenu interactif.

:unlock: Document avec un en-tête complet => raccourcis avec un fichier .html = ! + touche entrée


>!DOCTYPE html\
>html lang="en"\
>head\
    >meta charset="UTF-8"\
    >meta name="viewport" content="width=device-width, initial-scale=1.0"\
    >title Document title\
>head\
>body
    
>body\
>html


#### balise html
La racine: elle contient un élément *head* suivi d'un élément *body*. Précise la langue du document avec l'attribut *lang* et une code ISO (ex:"fr").

#### balise head
En-tête du document: elle contient les méta-informations interprétées par le navigateur sans apparaître dans le corps du document: *title*, *meta*, *link*, *style*, *script*.

#### balise body
Corps du document: elle contient toutes les autres balises HTML: texte, blocs, images, titres, médias, formulaire, ...

#### balise title
Titre du document: elle est affiché par le navigateur et indexé par les moteurs de recherche. Doit toujours être présent dans *head*.

#### balise méta
Méta-données: elle apporte des informations (mots-clés, description, auteur) dans l'en-tête *head* que les navigateurs et robots vont exploiter.

#### balise script
Script: elle contient un script (JavaScript) ou fait référence à un fichier externe avec l'attribut *src* et bien d'autres.


## Des sections pour structurer le document

Le choix du balisage de section est laissé à la libre appréciation du développeur web.

#### balise main
Contenu principal: elle structure dans un document la section majeure pouvant en regrouper d'autres. Il ne doit pas être descendant de *article*, *aside*, *footer*, *header* ou *nav*.

#### balise article
Article: portion de contenu indépendante, se suffisant à elle-même en termes de compréhension. Exemples: article de presse, fiche cinéma, réponse de forum.

#### balise section
Section: élément générique pour une section de contenu ou d'application web, utilisé à défaut d'un autre élément de section plus sémantique tel que *article*, *nav*, *header*, *f*ooter*, *aside*. A ne pas confondre avec *div* qui n'a aucune valeur sémantique. *Section* doit contenr un titre (élément *h1* à *h6*).

#### balise nav
Navigation: regroupe la sélection des principaux liens pour naviguer à travers le site, l'application web ou le document. Ne pas en abuser.

#### balise header
En-tête: elle s'applique au document entier, avec *main* ou à tout autre élément *section* ou *article*.

#### balise footer
Pied: s'applique au document entier, mais aussi à toute section au sens large, *article* y compris, s'il n'est pas descendant d'un autre élément de section.

#### balise h1 à h6
Hiérarchie de titres: six niveaus de titres pour hiérarchiser le contenu. Bien les employer selon leu niveau, et non selon leur aspect ou taille par défaut. Il revient aux CSS d'en définir le style graphique.

#### balise p
Paragraphe: contient un paragraphe de texte, éventutellement accompagné d'autres balises en ligne plus sémantiques (images, vidéos, audio), mais pas d'autre élément de type bloc (y compris *p* lui même).

#### balise br
Saut de ligne: force un saut de ligne: l'affichage se poursuit en début de ligne suivante.

#### balise hr
Séparation: élément vide qui marque une saparation dans le contenu, typiquement au niveau des paragraphes, usuellement représentée par une barre horizontale.

## Conteneurs génériques

*Bonne pratique*: évitez d'abuser des conteneurs génériques. Privilégier les éléments plus discriminants qui qualifient sémantiquement (notamment les sections). Utilisez *div* si aucun autre élément plus approprié n'a été trouvé

#### balise div
Conteneur  de type bloc: élément neutre permettant de regrouper d'autres éléments de tous types (bloc ou en ligne) Attention, *section* ne remplace pas automatiquement *div* pour autant.

#### balise span
Conteneur de type en ligne: équivalent en ligne de l'élément bloc *div*, il n'a pas de valeur sémantique propre, mais peut être enmployé comme conteneur neutre, notamment pour affecter des styles CSS.

## Listes

#### balise ul
Liste non ordonnée: désigne une liste d'éléments non ordonnés. Contenu autorisé *li*.

#### balise ol
Liste ordonnée: structure une liste d'éléments dont l'ordre importe, éléments pouvant être numérotés. Contenu autorisé: *li*.

#### balise li
Elément de liste: désigne un élément contenu dans une liste. Peut contenir une sous-liste *ul* ou *ol* et ainsi de suite, ou tout autre élément de flux.

## Embarquez du multimédia

## *Images*
Les images présentes dans le document HTML (hors images de fond définies avec CSS) sont à considérer comme des éléments à part entière devant apporter des informations à l'utilisateur. Les formats PNG, JPEG, GIF, SVG sont universellement reconnus.

#### balise img
Image: insère une image de contenu dans le document. L'attribut *src* spécifie l'adresse vers le fichier image. L'attribut *alt* indique un texte alternatif à l'image. Les dimensions sont définies en pixels par *width* (largteur) et *height* (hauteur).

#### balise template
Modèle de portion de document: fragments de code HTML invisibles par défaut, destinés à être clonés en JavaScript, puis insérés dans le document. Les méthodes DOM sont appropriées pour utiliser le modèle de DOM inactif décrit par *template* et l'insérer dans le document.

## Tableaux
Les tableaux de données sont conçus pour structurer es informations en lignes et en colonnes, aussi appelées donnnées tabulaires (que l'on retrouve et manipule dans tout logiciel de tableur).

*Bonne pratique* L'élément *table* n'st pas un outil de mise en page! Utiliser le positionnement CSS, avec Flexbox et Grid Layout.

#### balise table
Tableau de données: structure un tableau de données épaulé par les éléments *tr* (ligne de tableau), *th* (cellule d'en-tête) et *td* (cellule). Le tableau peut être découpé en 3 parties facultatives: *thead* (en-tête de tableau), *tbody* (corps proncipal), *tfoot* (pied de tableau)


## Liens

L'assence même du Web: le lien permet de naviguer d'une page à l'autre

#### balise a
Lien hypertexte: crée un lien hypertexte permettant de naviguer au sein de la page ou vers une autre page HTML. Son attribut courant est *href* (destination du lien).

#### balise link
Relation externe: déclare un lien vers des ressources externes, il set couramment employé pour lier une feuille de styles CSS au document HTML au moyen de la relation *stylesheet*.