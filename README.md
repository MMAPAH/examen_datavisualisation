# Projet de datavisualisation: Arrondissement de Paris

![arrondissement de paris](https://www.de-nicher.com/wp-content/uploads/sites/5/2019/06/carte-arrondissements-off.jpg)
Source: [etudiant.aujourdhui.fr] (http://etudiant.aujourdhui.fr/etudiant/info/quartier-a-paris-ou-habiter-a-paris.html)


# Table des matières


1. [Origine et traitement des données sur la densité de la population par arrondissement](#1-origine-et-traitement-des-données-sur-la-densité-de--la-population-par-arrondissement)
2. [Première datavisualisation avec Line chart race (Flourish)](#2-première-datavisualisation-avec-un-line-chart-race-flourish)
3. [Deuxième datavisualisation avec une carte (Datawrapper)](#3-deuxième-datavisualisation-avec-une-carte-datawrapper)
4. [Croisement des données](#4-croisement-des-données)
5. [Troisième datavisualisation avec Bar chart race (Flourish)](#5-troisième-datavisualisation-avec-bar-chart-race-flourish)
6. [Quatrième datavisualisation des données croisées](#6-quatrième-datavisualisation-des-données-croisées)
7. [Visualisation de Paris avec Wikidata Query Service](#7-visualisation-de-paris-avec-wikidata-query-service)


## 1. Origine et traitement des données sur la densité de population par arrondissement

Les données de l'évolution démographique au fil des années ont été trouvées sur [INSEE](https://www.insee.fr/fr/statistiques/4515941#consulter). Nous avons décidé de garder uniquement la partie des données qui nous intéresse: arrondissement, année, population. Les données d'origine étant bien définie, nous n'avons pas eu à réaliser de travaux préparatoires, ni a utiliser d'outils particuliers. Sur la base de ces trois informations, nous avons décidé de visualiser l'évolution de la population dans les arrondissements de Paris entre 1968 et 2015.

### Extrait des données finales:

|                          |  2017  |  2012  |  2007  |  1999  |  1990  |  1982  |  1975  | 
|--------------------------|:------:|:------:|:------:|:------:|:------:|:------:|:------:|
| Paris 1er Arrondissement | 16266  | 17100  | 17915  | 16888  | 18360  | 18509  | 22793  | 
| Paris 2e Arrondissement  | 20900  | 22390  | 21745  | 19585  | 20738  | 21203  | 26328  | 
| Paris 3e Arrondissement  | 34115  | 35991  | 34576  | 34248  | 35102  | 36094  | 41706  | 
| Paris 4e Arrondissement  | 28088  | 27769  | 28572  | 30675  | 32226  | 33990  | 40466  | 
| Paris 5e Arrondissement  | 58850  | 60179  | 62664  | 58849  | 61222  | 62173  | 67668  | 
| Paris 6e Arrondissement  | 41100  | 43224  | 45332  | 44919  | 47891  | 48905  | 56331  | 
| Paris 7e Arrondissement  | 51367  | 57092  | 57410  | 56985  | 62939  | 67461  | 74250  | 


> Tableau généré avec [Tables Generator](https://www.tablesgenerator.com)

## 2. Première datavisualisation avec un Line Chart Race (Flourish)

Pour créer le visuel des données récoltées, nous avons décidé d'utiliser le graphique  "Line Chart Race" avec trois paramètres que nous avons mentionnés ci-dessus. C'est un graphique en relief qui est souvent utilisé pour visualiser efficacement le classement des données à travers différentes mesures au fil du temps. 

<iframe src='https://flo.uri.sh/visualisation/4874798/embed' title='Interactive or visual content' frameborder='0' scrolling='no' style='width:100%;height:600px;'></iframe><div style='width:100%!;margin-top:4px!important;text-align:right!important;'><a class='flourish-credit' href='https://public.flourish.studio/visualisation/4874798/?utm_source=embed&utm_campaign=visualisation/4874798' target='_top' style='text-decoration:none!important'><img alt='Made with Flourish' src='https://public.flourish.studio/resources/made_with_flourish.svg' style='width:105px!important;height:16px!important;border:none!important;margin:0!important;'> </a></div>


Comme vous pouvez le voir certaines arrondissements n'ont pas évolué au fils des années et d'autres ont eu des changements importants. Après avoir revérifier les données et avoir mentionner que le nombre de population change au fis des années, nous nous sommes rendus compte qu'il s'agit de graphique qui ne permet pas illustrer la variation faible des données. 


## 3. Deuxième datavisualisation avec une Carte (Datawrapper)

Ensuite, nous avons décide d'illustrer la densité de la population avec une carte pour voir les arrondissement les plus et les moins peuplés . Cette datavisualisation a été réalisé en choisissant une carte des arrondissements de Paris (peu d'outils l'ont), ensuite, nos données ont été légérement modifiées (première colonne doit correspondre soit au code, code INSEE ou name), puis importées dans l'outil Datawrapper. Il faut mentionner, nous n'avons pas pu animer nos jeux de données pour voir l'évolution au fil des années, car Datawrapper ne le permet pas. Donc, une chose importante a été rajoutée pour voir l'évolution d'habitants par arrondissement (Tooltips: {{ code }} arrondissement, en 1968: {{ _1968 }} habitants; en 1975: {{ _1975 }} habitants), etc. 

<iframe title="" aria-label="Carte" id="datawrapper-chart-Z2G3Y" src="https://datawrapper.dwcdn.net/Z2G3Y/1/" scrolling="no" frameborder="0" style="border: none;" width="690" height="411"></iframe>

Grace à la deuxième visualisation cartographique, nous pouvons visualiser l'emplacement de chaque arrondissement, ainsi que voir la densité de population en 2017 et en cliquant sur chaque arrondissement le nombre d'habitants entre 1968 et 2012.

## 4. Croisement des données

Puis, nous avons essayé d'expliquer l'évolution de la population dans les arrondissements à travers les prix de l'immobilier. Nous avons récupéré un deuxième jeux de données ici :https://basebien.com/PNSPublic/DocPublic/HistoriquedesprixaumappartementsanciensParispararrdt.pdf. Ces données représente une historique des prix au m2 standardisés des appartements anciens à Paris par arrondissement. Les données sont issues des actes authentiques signés dans les offices notariaux français. 

Un extrait des données brutes:

| Trimestre | Centre   | 1er      |    2e    |    3e    |    4e    |    5e    |    6e    |    7e    |
|-----------|----------|----------|:--------:|:--------:|:--------:|:--------:|:--------:|:--------:|
| T3 2020   | 12 870 € | 13 940 € | 12 250 € | 12 650 € | 13 660 € | 12 750 € | 14 590 € | 14 100 € |
| T2 2020   | 12 860 € | 13 100 € | 12 570 € | 12 820 € | 13 480 € | 12 740 € | 14 250 € | 14 020 € |
| T1 2020   | 12 340 € | 12 990 € | 11 830 € | 12 540 € | 12 640 € | 12 640 € | 14 250 € | 13 480 € |
| T4 2019   | 12 470 € | 13 240 € | 11 830 € | 12 330 € | 13 200 € | 12 420 € | 13 610 € | 13 540 € |
| T3 2019   | 12 150 € | 12 890 € | 11 200 € | 12 200 € | 12 780 € | 12 110 € | 14 170 € | 13 310 € |
| T2 2019   | 12 140 € | 12 520 € | 11 860 € | 11 970 € | 12 610 € | 11 880 € | 13 850 € | 12 850 € |
| T1 2019   | 11 780 € | 12 020 € | 11 630 € | 11 430 € | 12 710 € | 11 530 € | 13 740 € | 12 870 € |

> Tableau généré avec [Tables Generator](https://www.tablesgenerator.com)

Les modifications suivantes ont été réalisées: changement du format (pdf vers csv avec [ilovepdf] (https://www.ilovepdf.com/pdf_to_excel)), calcul du prix moyen par année, suppression des années pour lequelles nos ne possèdons pas d'informations concernant la population (2020-2018), positionnement des lignes et des colonnes modifiés pour pouvoir faire une datavisualisation. Vous pouvez voir ci-dessus un extrait des données finales:

|     | Prix moyen 2017 | Prix moyen 2016 | Prix moyen 2015 | Prix moyen 2014 |
|-----|-----------------|-----------------|-----------------|-----------------|
| 1er |        11 353 € |        10 533 € |        10 328 € |        10 303 € |
|  2e |        10 348 € |         9 613 € |         9 478 € |         9 548 € |
|  3e |        10 748 € |         9 893 € |         9 683 € |         9 815 € |
|  4e |        11 750 € |        11 373 € |        10 940 € |        11 068 € |
|  5e |        11 090 € |        10 383 € |         9 968 € |        10 153 € |
|  6e |        12 050 € |        11 298 € |        11 543 € |        11 535 € |
|  7e |        11 480 € |        11 123 € |        10 745 € |        11 050 € |
|  8e |         9 928 € |         9 185 € |         9 195 € |         9 478 € |
|  9e |         9 295 € |         8 513 € |         8 343 € |         8 430 € |
| 10e |         8 270 € |         7 615 € |         7 385 € |         7 403 € |
| 11e |         8 735 € |         8 065 € |         7 840 € |         7 920 € |

> Tableau généré avec [Tables Generator](https://www.tablesgenerator.com)

## 5. Troisième datavisualisation avec Bar Chart Race (Flourish)

Pour visualiser le deuxième jeux de données, nous avons décidé d'utiliser Bar Chart Race sur Flourish, ce que nous a permit avoir la visualisation dynamique des prix moyens au fil des années (1995 - 2017).

<iframe src='https://flo.uri.sh/visualisation/5154066/embed' title='Interactive or visual content' frameborder='0' scrolling='no' style='width:100%;height:600px;'></iframe><div style='width:100%!;margin-top:4px!important;text-align:right!important;'><a class='flourish-credit' href='https://public.flourish.studio/visualisation/5154066/?utm_source=embed&utm_campaign=visualisation/5154066' target='_top' style='text-decoration:none!important'><img alt='Made with Flourish' src='https://public.flourish.studio/resources/made_with_flourish.svg' style='width:105px!important;height:16px!important;border:none!important;margin:0!important;'> </a></div>

## 6. Quatrième datavisualisation des données croisées
Nous avons regrouper deux fichiers de données, celui de population et celui avec les prix moyens au m2 pour voir si ces deux mouvements sont liés. En sélectionnant la population ,ainsi que le prix moyen qui vous intéresse, nous pouvons comparer ces deux valeurs. Par défaut, vous voyez toutes les années et tous prix. Pour faire une comparaison, il est néccessaire de cliquer sur __Sélectionner les données à comparer__, ensuite choisir l'année qui vous intéresse.

<iframe src='https://flo.uri.sh/visualisation/5155593/embed' title='Interactive or visual content' frameborder='0' scrolling='no' style='width:100%;height:600px;'></iframe><div style='width:100%!;margin-top:4px!important;text-align:right!important;'><a class='flourish-credit' href='https://public.flourish.studio/visualisation/5155593/?utm_source=embed&utm_campaign=visualisation/5155593' target='_top' style='text-decoration:none!important'><img alt='Made with Flourish' src='https://public.flourish.studio/resources/made_with_flourish.svg' style='width:105px!important;height:16px!important;border:none!important;margin:0!important;'> </a></div>

Comme vous pouvez le voir, dans cette visualisation il manque plusieurs années. En effet, il est difficile de trouver l'informations concernant les prix au m2 par arrondissement avant 1995. Néanmoins, en analysant les données préséntés, nous pouvons supposer qu'il avaint une hausse importante entre 1999 et 2007. En vérifiant cette hyphothèse, nous avons trouvé qu'en effet, la période entre 1998 et 2008 correspond à une longue hausse nationale et que cette période est connu pour ces volumes importantes de vente. Les notaires précisent que cette période a été boostée par un “contexte économique bien orienté” et surtout par un “crédit bancaire facile et bon marché”. La période 2007 et 2012 englobe deux choses à la fois: la crise de liquidités entre 2008-2009 (les prix diminuent) et une très forte envolée à Paris entre 2009 et 2011 (explosion des prix). Dans la graphique nous pouvons observer que les prix ont augenté, mais pas si haut comme nous l'attendions. Dans la période entre 2012 et 2017, nous pouvons observé que les prix ont peu changés par rapport aux années précédentes.

Après avoir réalisé ce graphique, nous pouvons conclure qu'il est difficile de voir si le lien entre les prix des appartements et le nombre d'habitants existe. Nous pouvons constater, qu'il s'agit plutot des changements généraux qui touchent toute la ville et pas un arrondissement en particuliers.

## 7. Visualisation de Paris avec Wikidata Query Service

Dans cette partie, grace à une requete de Wikidata, nous avons pu afficher les rues de Paris pour le coté estétique. Si il y a des images qui vous intéresse, vous pouvez voir le titre de lieu, ainsi que ses coordonnées géographiques.

```sparql
#defaultView:ImageGrid
SELECT
  ?arr
  (SAMPLE (?titleL) AS ?title)
  (SAMPLE (?img) AS ?image)
  (SAMPLE (?coord) AS ?coordinates) {

    {
      SELECT DISTINCT ?arr {
        ?arr  wdt:P131 wd:Q90;}
    }
    # title
    OPTIONAL { ?arr rdfs:label ?titleL filter (lang(?titleL) = "fr") }
   
    # image
    OPTIONAL { ?arr wdt:P18 ?img }
   
    # coordinates
    OPTIONAL { ?arr wdt:P625 ?coord }

} GROUP BY ?arr
LIMIT 1500 
```


<iframe style="width: 55vw; height: 50vh; border: none;" src="https://query.wikidata.org/embed.html#%23defaultView%3AImageGrid%0ASELECT%0A%20%20%3Farr%0A%20%20%28SAMPLE%20%28%3FtitleL%29%20AS%20%3Ftitle%29%0A%20%20%28SAMPLE%20%28%3Fimg%29%20AS%20%3Fimage%29%0A%20%20%28SAMPLE%20%28%3Fcoord%29%20AS%20%3Fcoordinates%29%20%7B%0A%0A%20%20%20%20%7B%0A%20%20%20%20%20%20SELECT%20DISTINCT%20%3Farr%20%7B%0A%20%20%20%20%20%20%20%20%3Farr%20%20wdt%3AP131%20wd%3AQ90%3B%7D%0A%20%20%20%20%7D%0A%20%20%20%20%23%20title%0A%20%20%20%20OPTIONAL%20%7B%20%3Farr%20rdfs%3Alabel%20%3FtitleL%20filter%20%28lang%28%3FtitleL%29%20%3D%20%22fr%22%29%20%7D%0A%20%20%20%0A%20%20%20%20%23%20image%0A%20%20%20%20OPTIONAL%20%7B%20%3Farr%20wdt%3AP18%20%3Fimg%20%7D%0A%20%20%20%0A%20%20%20%20%23%20coordinates%0A%20%20%20%20OPTIONAL%20%7B%20%3Farr%20wdt%3AP625%20%3Fcoord%20%7D%0A%0A%7D%20GROUP%20BY%20%3Farr%0ALIMIT%201500" referrerpolicy="origin" sandbox="allow-scripts allow-same-origin allow-popups" ></iframe>


## Conclution

Le sujet en question présente pour moi un intéret particulier. En effet, il était intéressant de se pencher sur l'évolution de population de Paris et d'essayer de l'expliquer à travers les prix de l'immobilier. Grace aux plusieurs types de datavisualisations, nous avons pu mettre en avant differents problèmatiques. 

Ce projet nous a permis de vivre pleinement le processus qui s'appelle Data Wrangling, en partant des données brutes, nous avons réussi de les adapter à nos besoins, en les modifiants et nettoyants ce que par la suite, nous a permit de les visualiser et publier sur cette page de github.

Néanmois, nous avons rencontrés certains problèmes pendant la réalisation de ce projet:
- les données brutes étaient mieux formatées sous xslx, que sous csv,
- il est néccesaire d'adapter les données à chaque application pour les visualiser,
- chaque application ayant ses limites (graphique sur flourish ne permet pas d'illustrer la variation faible des données, graphique sur Datawrapper ne permet pas de faire un storytelling pour voir la densité de population par année, requete de Wikidata Query Service ne permet pas spécifier/filtrer le type de photos à afficher (uniquement de l'exterier, pas de plan/schèma de Paris et assez récentes)),
- l'bsence de données sur les prix de l'immobilier depuis 1968,
- nouveau language à apprendre (Markdown) pour construite une page.




