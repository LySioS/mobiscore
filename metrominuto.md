---
title: "Metrominuto"
order: 5
in_menu: false
---
## Intro 

J'ai découvert il y a quelques jours l'initiative de la commune de Pontevedra, en Espagne, d'implanter sur son territoire des cartes de temps de déplacement  à pied entre les différentes zones d'intérêt de la commune. Cette initiative date de 2011 et s'inspire du graphisme schématique des plans de métro.

Cela s'appelle un *metrominuto*. 

![metrominuto-pontevedra](https://metrominuto.info/wp-content/uploads/2020/06/metrominuto8.png)

> le metrominuto originel, source: https://metrominuto.info/

L'intérêt est de valoriser un autre mode de déplacement que la voiture en affichant le temps réel de parcours à pied entre 2 endroits de la ville, ces derniers étant souvent surestimés.

Cela permet, en additionnant les différentes valeurs temps des segments empruntés d'avoir une idée approximative de son temps de trajet.

Depuis, ce projet a fait des émules. Quand on recherche *metrominuto* sur internet, la plupart des plans qui ressortent sont espagnols. En France, on peut citer la ville de Toulouse et tout récemment, Saint-Brieuc. 

## Types 

Quand on s'attarde sur les [différentes réalisations](https://duckduckgo.com/?q=metrominuto&t=h_&iax=images&ia=images), on perçoit différentes approches dans la conception des *metrominutos*.

* la plupart sont rectilignes et suivent un quadrillage
*  les tracés ne sont pas proportionnels à la distance
* beaucoup affichent la distance en plus du temps
* les couleurs sont rarement associées à un temps précis
* d'autres symboles peuvent venir renseigner les parkings ou arrêts de bus
* certains ont tracé, en plus des segments points à points, des itinéraires complets
* certains intègrent les temps en vélo

## Réalisation

En tant qu'amateur de carto et de graphisme, et très agacé par la surutilisation de la voiture au quotidien , je n'ai pas pu résister à en créer un pour ma commune.

#### Quel logiciel ?

 Il me fallait une version vectorielle, c'est plus propre, n'empêche pas une version bitmap et permet de l'utiliser plus librement sur différents supports : numériques, panneaux physiques, etc.
 
 J'ai utilisé Inkscape pour tout composer, logiciel libre que je connais un peu.

#### Mode de déplacement

Je souhaitais réaliser le mien en 2 versions : une piéton et l'autre cycliste.

Piéton parce qu'à mon avis, c'est le mode de déplacement dont on surestime le plus le temps de déplacement et que tout le monde n'ose pas faire du vélo en ville.

Cycliste parce que c'est le véhicule le plus pertinent à l'échelle d'une ville (et ce serait bien que nos dirigeants le comprennent).

L'exemple du *metrominuto* de Saint-Brieuc mélangeant les 2 est à mon sens surchargé et les zones que l'on peut atteindre en vélo sont bien plus nombreuses : il faut changer d'échelle.

#### _Look and feel_

Concernant la présentation, je ne souhaitais pas garder cet aspect quadrillage avec des tracés dont la taille n'est pas proportionnelle à la distance.

Pour ce faire, j'ai utilisé un fond de carte OpenStreetMap (What Else ? ☕) qui m'a servi à placer les points d'intérêts. Pour ce faire, j'ai utilisé la fonction *partager* du site officiel qui permet de générer une image de la carte.

Ensuite, j'ai connecté les points entre eux de manière rectiligne en appliquant des couleurs au hasard. Le côté rectiligne sans quadrillage faisait un peu brouillon, j'ai commencé à courber les traits selon l'itinéraire réel, rendu validé.

Afin que les points d'intérêts soit compris directement, j'ai choisi de prendre des libertés avec certains toponymes et décidé d'y rajouter une icône. Il faut savoir que beaucoup de personnes ne connaissent pas leur environnement direct, même dans le cas d'une petite ville (ici, 10 000 habitants).

Ainsi, au lieu d'indiquer "place du 8 mai 45", il était plus clair d'indiquer écoles/collège ; etc.

#### Temps de trajet

Concernant les temps de trajets, j'ai utilisé le site [OpenRouteService](https://maps.openrouteservice.org/) que j'apprécie pour ses isochrones. Ça a été l'occasion de corriger des erreurs de carto sur OSM : connections manquantes d'un côté de la rue à l'autre ou encore place piétonne entraînant des détours conséquents dans le calcul d'itinéraire.

Je souhaitais aussi intégrer la distance en mètres. Malheureusement, le manque de place m'a fait préférer la lisibilité.

Le réel problème qui s'est posé est de savoir où placer de manière pertinente les points de départ et  d'arrivée. Dans le cas d'une grande zone, le met-on à son entrée principale, à l'entrée la plus près de là où on vient, ou au centre ?

Si je calcule le temps de trajet pour y arriver, le point à l'entrée la plus proche est plus pertinent. Mais si je calcule un trajet qui traverse cette zone, il me manquera le temps de traversée, non négligeable à pied.
Inversement, si je calcule un trajet qui longe plusieurs de ces zones, je n'ai pas besoin d'aller en leur centre et d'avoir un temps de trajet plus long que la réalité !

Pour les lotissements, qui se trouvent en périphérie de la ville, j'ai choisi un point à l'entrée et pour les zones plus intérieures, j'ai pris un point central.

#### Supports

Je souhaitais aussi lier ce *metrominuto* à une version en ligne de manière que les gens puissent la trouver et la consulter sur leur téléphone. J'ai peu d'espoir que la mairie s'en saisisse pour réaliser un affichage physique, mais qui sait ?

J'avais pensé créer un QR code amenant vers une version uMap de ce *metrominuto*. Elle se serait présenté avec les itinéraires réels (les gens ne connaissent vraiment pas leur territoire, encore moins les venelles !) de la même couleur que leur trait schématique calqués sur un fond de carte OSM-FR qui a l'avantage d'être riche en informations piéton et accessibilité.

J'ai finalement opté pour un lien direct vers le même document numérique. Peut-être que je créerai cette version uMap, à voir.

#### Habillage

Afin de d'apporter un peu relief et de repérage, certains *metrominutos* possèdent des éléments géographiques remarquables de la ville : rivière, couloir vert, parcs, etc.

Ma ville n'ayant aucun élément structurant traversant (à part des départementales), j'ai opté pour le tracé de l'enveloppe urbaine.

Restait l'habillage et le tour était joué. Je suis parti sur une couleur bleue et un panneau piéton customisé. La version vélo sera sur le même modèle, verte avec un panneau cycliste customisé.

#### Résultat final

![metrminuto-cabesatany](https://upload.wikimedia.org/wikipedia/commons/thumb/9/94/Metrominuto-pi%C3%A9ton-Cabestany.svg/533px-Metrominuto-pi%C3%A9ton-Cabestany.svg.png)

https://commons.wikimedia.org/wiki/File:Metrominuto-pi%C3%A9ton-Cabestany.svg

## Suites

J'ai envoyé ça à ma mairie, *wait and see*.

En parallèle, j'ai déjà commencé la version vélo sur le même modèle.
Je trouvais ça curieux que le principe du *metrominuto* n'ait pas été transposé spécifiquement aux vélos. 

Je n'ai trouvé que les [réalisations du Collectif Cycliste 37](https://www.cc37.org/la-riche-carte-des-temps-de-trajets-a-velo/) . Je trouve le résultat très réussi. Voici comment ils l'ont pensée :

> Nous avons défini 8 itinéraires vélo, à la façon de lignes de bus, traversant La Riche de part en part tout en desservant les points d’intérêts générateurs de déplacements dans la commune (commerces, bâtiments publics, parcs…).

![la-riche](https://www.cc37.org/wp-content/uploads/2015/06/lariche-1024x643.jpg)

Ils ont couvert d'autres communes ensuite !

##  Réflexions

Si j'aime beaucoup le principe du *metrominuto*, je me suis fait la réflexion en le réalisant que ce n'est pas un outil assez direct pour un simple curieux. Il faut prendre le temps de le comprendre, de tracer son itinéraire et de faire les calculs.

Pour engager les gens dans un report modal, on pourrait aussi proposer à chaque endroit stratégique de la commune une carte isochrone centrée là où on se trouve affichant les zones accessibles en 5, 10, 15 et 20 minutes. Cela permettrait en 1 coup d'œil de se situer et de repérer dans quel périmètre de temps notre maison se trouve.

Je verrais bien le titre :  "*Et si vous veniez autrement ?*" illustré d'une carte isochrone piéton et d'une autre vélo avec en 3e partie les différents bénéfices des déplacements doux sur :

* la santé
* le portefeuille
* la qualité de l'air
* l'apaisement de la ville
* la pollution (**les voitures électriques ne sont pas écologiques**)

Malgré tout, il faut reconnaître les limites à ce genre d'initiatives. On peut inciter les gens à changer leurs modes de déplacement, du moment que ce n'est pas associé à une politique d'aménagement ambitieuse assurant la lisibilité, la continuité,  la sécurisation, l'ombrage, le repos, la végétalisation, etc. des itinéraires doux, cela restera des vœux pieux.

Les dynamiques et volonté de changement individuelles ne peuvent s’accomplir que grâce à des structures collectives.

C'est le message que j'essaie désespérément de faire passer à ma commune...

Sinon, on peut y aller plus cash ⬇️
![pollution](https://pbs.twimg.com/media/FEQq3EDUUAINf6N?format=jpg)

----

## Update

Voici la version vélo

![metrominuto-vélo](https://upload.wikimedia.org/wikipedia/commons/thumb/f/fc/Metrominuto-cycliste-Cabestany.svg/823px-Metrominuto-cycliste-Cabestany.svg.png)
https://upload.wikimedia.org/wikipedia/commons/f/fc/Metrominuto-cycliste-Cabestany.svg 