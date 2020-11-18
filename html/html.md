### HTML

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


| html | ####La racine. 
contient un élément head suivi d'un élément body. Précise la langue du document avec l'attribut 'lang' et une code ISO (ex:"fr").|
|head| En-tête du document. Contient les méta-informations interprétées par le navigateur sans apparaître dans le corps du document: title, meta, link, style, script.|
|body| Corps du document. Contient toutes les autres balises HTML: texte, blocs, images, titres, médias, formulaire, ...|
|title| Titre du document. Affiché par le navigateur et indexé par les moteurs de recherche. Doit toujours être présent dans head.|
|meta| Méta-données. Apporte des informations (mots-clés, description, auteur) dans l'en-tête head que les navigateurs et robots vont exploiter.|
|script| Script. Contient un script (JavaScript) ou fait référence à un fichier externe avec l'attribut src t bien d'autres.|
