Voici l'ordre à suivre pour faire rouler le code:

Section 1 : Importation et transormation des données:

Le répertoire se créer automatiquement en roulant le 1. Sinon, pour les données, veuillez vous créer un répertoire Donnees. Dans Donnees, créer deux fichiers: Brutes et Traitees. Dans Brutes, créer un fichier nommé web. Dans web, créer 2 fichiers: cancensus et osm.
Donnees/
├── Brutes/
│   ├── web/
│   │   ├── cancensus/
│   │   ├── osm/
├── Traitees/

Il faut aussi créer ces fichiers et le remplir à l'aide des données dans les liens indiqués:
Donnees
 ├── Brutes
 │   ├── CMM
 │   │   ├── occ
 │   │   ├── ram
 │   ├── Debit Qc
 │   │   ├── cir_v_geo_sectn_trafc_locls
 │   │   ├── Débits Tarcisio
 │   ├── Frontieres administratives
 │   │   ├── Quebec
 │   ├── collisions_routieres_MTL_SHP
 │   ├── misc
 │   │   ├── variables presentations.xlsx
 │   │   ├── changements noms.xlsx


1 - Rouler : "Importation données accidents" - Les données montréalaises sont publqieus (1ere partie du code). Les données québécoises ne sont pas publiques, quelqu'un n'ayant pas accès aux données ne pourra pas les importer.
2 - Rouler : "Exportation Cancensus" - Ce code crée les données de Cancensus. Dans le mémoire, nous avons besoin de données au niveau municipal, des MRC, et particulièrement sur l'île de Montréal.
3 - Rouler : "Exportation autres" - Ce code crée importe les jeux de données sur les débits routiers. Il crée aussi les variables de "Résidentiel" et "Commercial" des données du CMM (Communauté métropolitaine de montréal).
4 - Rouler : "Exportation OSM" - Ce code crée les jeux de données d'OpenStreetMap
Veuillez prendre note que comme les données de Cancensus et d'OpenStreetMap se mettent à jour automatiquement sur le Web, les codes de traitement de données pourraient éventuellement ne plus fonctionner.

5 - Rouler : Alignement régions - ce code crée une version des données d'accidents excluant les accidents avec dommages matériels seulement (au niveau des conducteurs impliqués dans un accident). D'autres colonnes sont prétraitées aussi.
				  Code permet surtout d'aligner les frontières administratives québécoises à celles utilisées dans Cancensus -> création des shapefiles de ces frontières.
6 - Rouler : "Fcts pour covariables - ce code contient les fonctions pour extraire les données des données brutes. Le code fait aussi l'extraction en tant que tel.
7 - Rouler : "Voisinages" - ce code contient relie des régions séparées par des cours d'eau lorsque des ponts les relient.

Section 2 : Modélisations

8 - Rouler : "Création jdD Areal" - Code créant le jeu de données utilisée pour les modèles BYM. Ajoute des rangées pour les régions sans accidents. 
				    Analyse préliminaire pour les modèles surfaciques (BYM)
9 - Rouler : "BYM" - Code contenant les modélisations BYM, précédé par certains prétraitement finaux et les calucls des corrélations.
10 - Rouler : "LGCP préliminaire" - Code contenant les analyses préliminaires des modélisations LGCP
11 - Rouler "LGCP" - Modélisations LGCP - normal de ne pas obtenir exactement les mêmes résultats que moi puisque les données spatiales dans la ville de Mtl ont changé.



















