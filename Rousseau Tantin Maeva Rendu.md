<!-- Headings -->
# Rendu QGIS
**ROUSSEAU TANTIN Maeva - M1 HCP**
### Etapes de conception de la carte QGIS
#### Choix des fonds de cartes
Site : [Natural Earth](https://www.naturalearthdata.com/downloads/)
* Land
* Ocean 
* Rivers_lake_centerlines
* Lake

J'ai choisi un fond de carte simple sans relief pour une question de lisibilité. J'ai pris une carte du monde car il n'existait pas de carte comprenant la Grèce et les îles de la Mer Egée. En plus de l'océan et de la terre, j'ai ajouté les lacs et les rivières, cependant je n'ai pas atteint le but recherché car les petites rivières ou fleuves n'apparaissent pas ce qui ne permet pas de comprendre l'emplacement de certaines cités en réalité proche de ces endroits. Pour un sujet sur la guerre sur mer mettre une couche pour l'océan me semble nécessaire.

Pour les ajouter : 
* Couche => ajouter une couche => couche vecteur => couche.shp

#### Ajout du jeu de données crée dans excel
J'ai choisi de ne pas mentionner la totalité des cités possédant une puissance maritime durant l'époque classique mais uniquement les cités dont Thucydide mentionne qu'elles ont une puissance maritime pendant la guerre du Péloponnèse car ce sont les sources sur lesquelles j'ai le plus avancé. Ensuite j'ai ajouté les batailles navales car elles sont la source de violences entre les combattants tout comme une partie des raids maritimes. Cependant, je n'ai ajouté que les raids maritimes que j'ai trouvé pour le moment ce qui explique qu'ils y en aient peu. 

**Tableur**
| Cités         | X           | Y           | Alliance  |
| ------------- |:-----------:| :----------:|:---------:|
| Corinthe      | 37.9085315  | 22.8988798  | Sparte    |
| Corcyre       | 39.591337   | 19.8596189  | Athènes   |
| Sparte        | 37.0744494  | 22.4301778  | Sparte    |
| Athènes       | 37.9755648  | 23.7348324  | Athènes   |
| Samos         | 37.7246162  | 26.8192919  | Athènes   |
| Chios         | 38.3758131  | 26.0646552  | Athènes   |
| Lesbos        | 39.1758418  | 25.9989135  | Athènes   |
| Mégare        | 37.9965887  | 23.3445017  | Sparte    |
| Sicyone       | 37.5903     | 22.4240     | Sparte    |
| Pellène       | 38.0432746  | 22.5483384  | Sparte    |
| Elis          | 37.8830916  | 21.3847776  | Sparte    |
| Ambracie      | 39.1613205  | 38.7065734  | Sparte    |
| Leucade       | 38.7065734  | 20.6416779  | Sparte    |

Informations sur ces données :
* Noms cités et alliances trouvées dans Thucydide, _La guerre du Péloponnese_
* Coordonnées géographiques récupérées sur le site : [Coordonées GPS](https://www.coordonnees-gps.fr/)
* X (Latitude) et Y (Longitude)

Difficulté pour enregistrer le tableur dans QGIS : il a fallu choisir le délimiteur personnalisé avec le point-virgule pour que les colonnes apparaissent puis modifier le champ des points X et Y car les points n'apparaissaient pas au bon endroit au début. 

#### Ajout de couche de point vide
Après avoir rajouté les cités, j'ai créé une couche shapefile de point vide _"batailles navales"_ puis j'ai créé les points grâce à la _"barre d'outils de numérisation avancée"_. Pour les coordonnées géographiques, je les ai récupérés sur [Wikipédia](https://fr.wikipedia.org/wiki/Wikip%C3%A9dia) car c'est le seul site qui permettait de les trouver. Cependant, je me suis aussi appuyé sur une carte du livre, _The Oxford handbook of warfare in classical world_ pour vérifier leur emplacement. A l'aide de l'éditeur, j'ai pu déplacer les points s'ils n'étaient pas au bonne endroit.

J'ai fait la même chose pour mettre les 2 ports du Pirée et du Gytheion car ce sont des endroits importants pour comprendre où était situés les navires qui partaient d'Athènes et de Sparte. Enfin, j'ai ajouté deux autres couches shapefile pour les raids maritimes. Pour leurs points, j'ai dû utiliser la barre _"ajoutée une entité linéaire"_ plutôt qu'une _"entité ponctuelle"_ pour tracer des courbes.

#### Ajout et modification des étiquettes et des symboles
Pour catégoriser les cités, j'ai changé les propriétés de la couche :
* Symbologie => Symbole unique => catégorisé (valeur : alliance) avec deux points/ couleurs (valeur : Sparte / Athènes) et une légende.

Pour la forme (symbologie), j'ai mis une ancre pour les ports car cela montre bien la présence de navire et des flèches pour les raids afin de montrer un déplacement.

Ensuite, j'ai modifié les étiquettes, les cités étant parfois rassemblées au même endroit j'ai mis une police plus petite pour qu'on puisse toutes les voir sinon certaines disparaissaient de la carte.

Pour les couleurs, j'ai choisi de mettre l'océan en bleu de manière traditionelle et la terre en vert puis, de choisir des couleurs qui soient lisibles et jolies sur ce fond. Les batailles en rouge sont bien visible. 

#### Mise en page
J'ai crée une mise en page avec une légende, un titre de légende, une échelle, une flèche nord, l'auteur et la date. Pour la légende j'ai créé deux groupes entre les lieux (cités / ports) et les mouvements maritimes (raids / batailles) en ajoutent des éléments au nom de certains éléments de la légende dans les propriétés (modification : taille, police, espace).

Une des difficultés rencontrée est que la carte de la mise en page étant plus petite, certaines étiquettes disparaissaient ou changeaient de place. Il m'a fallu faire quelques modifications sur la carte originale pour que la mise en page soit bonne, notamment déplacer certaines étiquettes.

### Carte finale
![Carte QGIS](https://github.com/user-attachments/assets/fda7f105-71fe-4be5-acfa-cdff8af44981)


### Sources bibliographiques et webographiques
* Campbell, J. B. and Tritle, L. A., _The Oxford handbook of warfare in the classical world_, Oxford, 2013.
* Kowalski Jean-Marie. Thucydide, témoin des opérations navales dans la première phase de la guerre du Péloponnèse (431-415 av. J.‑C.). In: _Dialogues d'histoire ancienne_, vol. 40, n°1, 2014. p. 27-51.
* Thucydide, _La guerre du Péloponnèse_
* Xénophon, _Les Helléniques_

Sites pour les coordonnées : 
* https://fr.wikipedia.org/wiki/Wikip%C3%A9dia
* https://www.coordonnees-gps.fr/
