# Projet de datavisualisation: Arrondissements de Paris

![arrondissement de paris](https://www.de-nicher.com/wp-content/uploads/sites/5/2019/06/carte-arrondissements-off.jpg)



# Table des matières


1. [Origine et traitement des données sur la densité de population par arrondissement](#1-origine-et-traitement-des-données-sur-la-densité-depopulation-par-arrondissement)
2. [Première datavisualisation avec Line chart race (Flourish)](#2-première-datavisualisation-avec-un-line-chart-race-flourish)
3. [Deuxième datavisualisation avec une carte (Datawrapper)](#3-deuxieme-datavisualisation-avec-une-carte-datawrapper)
4. [Traitement des données de prix moyens par arrondissement](#4-traitement-des-donnees-de-prix-moyens-par-arrondissement)
5. [Troisième datavisualisation avec Bar chart race (Flourish)](#5-troisieme-datavisualisation-avec-bar-chart-race-flourish)
6. [Visualisation de Paris avec Wikidata Query Service](#6-visualisation-de-paris-avec-wikidata-query-service)
[Conclusion] (#7-conclusion)

## 1. Origine et traitement des données sur la densité de population par arrondissement

Les données de l'évolution démographique au fil des années ont été trouvées sur [INSEE](https://www.insee.fr/fr/statistiques/4515941#consulter). Nous avons décidé de garder uniquement la partie qui nous intéresse: arrondissement, année, population. Les données d'origine étant bien définie, nous n'avons pas eu à réaliser de travaux préparatoires ni a utiliser d'outils particuliers. Sur la base de ces trois informations, nous avons décidé de visualiser l'évolution des arrondissements de Paris entre 1968 et 2015.

### Données finales:

|                          |  2017  |  2012  |  2007  |  1999  |  1990  |  1982  |  1975  |  1968  |
|--------------------------|:------:|:------:|:------:|:------:|:------:|:------:|:------:|:------:|
| Paris 1er Arrondissement | 16266  | 17100  | 17915  | 16888  | 18360  | 18509  | 22793  | 32332  |
| Paris 2e Arrondissement  | 20900  | 22390  | 21745  | 19585  | 20738  | 21203  | 26328  | 35357  |
| Paris 3e Arrondissement  | 34115  | 35991  | 34576  | 34248  | 35102  | 36094  | 41706  | 56252  |
| Paris 4e Arrondissement  | 28088  | 27769  | 28572  | 30675  | 32226  | 33990  | 40466  | 54029  |
| Paris 5e Arrondissement  | 58850  | 60179  | 62664  | 58849  | 61222  | 62173  | 67668  | 83721  |
| Paris 6e Arrondissement  | 41100  | 43224  | 45332  | 44919  | 47891  | 48905  | 56331  | 70891  |
| Paris 7e Arrondissement  | 51367  | 57092  | 57410  | 56985  | 62939  | 67461  | 74250  | 87811  |
| Paris 8e Arrondissement  | 36808  | 38749  | 39165  | 39314  | 40814  | 46403  | 52999  | 67897  |
| Paris 9e Arrondissement  | 59555  | 59474  | 58632  | 55838  | 58019  | 64134  | 70270  | 84969  |
| Paris 10e Arrondissement | 90372  | 94474  | 93373  | 89612  | 90083  | 86970  | 94046  | 113372 |
| Paris 11e Arrondissement | 146643 | 155006 | 151421 | 149102 | 154165 | 146931 | 159317 | 179727 |
| Paris 12e Arrondissement | 140296 | 144925 | 142425 | 136591 | 130257 | 138015 | 140900 | 155982 |
| Paris 13e Arrondissement | 182099 | 182386 | 179213 | 171533 | 171098 | 170818 | 163313 | 158280 |
| Paris 14e Arrondissement | 135964 | 141102 | 134382 | 132844 | 136574 | 138596 | 149137 | 167093 |
| Paris 15e Arrondissement | 233392 | 238190 | 232247 | 225362 | 223940 | 225596 | 231301 | 244080 |
| Paris 16e Arrondissement | 166361 | 167613 | 159706 | 161773 | 169863 | 179446 | 193590 | 214120 |
| Paris 17e Arrondissement | 167288 | 170156 | 164673 | 160860 | 161935 | 169513 | 186293 | 210299 |
| Paris 18e Arrondissement | 195233 | 201374 | 191523 | 184586 | 187657 | 186866 | 208970 | 236776 |
| Paris 19e Arrondissement | 187015 | 186116 | 184038 | 172730 | 165062 | 162649 | 144357 | 148862 |
| Paris 20e Arrondissement | 195814 | 197311 | 194018 | 182952 | 184478 | 171971 | 175795 | 188921 |

> Tableau généré avec [Tables Generator](https://www.tablesgenerator.com)

## 2. Première datavisualisation avec un line chart race (Flourish)

Pour créer le visuel des données récoltées, nous avons décidé d'utiliser le graphique  "Line Chart Race" avec trois paramètres suivantes: année, arrondissement et population. C'est un graphique en relief qui est souvent utilisé pour visualiser efficacement le classement des données (dans notre cas les arrondissements) à travers différentes mesures (population) au fil du temps. 

<iframe src='https://flo.uri.sh/visualisation/4874798/embed' title='Interactive or visual content' frameborder='0' scrolling='no' style='width:100%;height:600px;'></iframe><div style='width:100%!;margin-top:4px!important;text-align:right!important;'><a class='flourish-credit' href='https://public.flourish.studio/visualisation/4874798/?utm_source=embed&utm_campaign=visualisation/4874798' target='_top' style='text-decoration:none!important'><img alt='Made with Flourish' src='https://public.flourish.studio/resources/made_with_flourish.svg' style='width:105px!important;height:16px!important;border:none!important;margin:0!important;'> </a></div>


Comme vous pouvez le voir certaines arrondissements n'ont pas évolué au fils des années. Sachant que les données changeaient bien au fil des années, nous nous solmes rendus compte qu'il s'agit de graphique, voir outil qui ne permet pas illustrer la variation faible des données. 


## 3. Deuxième datavisualisation avec une carte (Datawrapper)

Cette datavisualisation a été réalisé en choisissant une carte des arrondissements de Paris (peu d'outils l'ont), ensuite, nos données ont été légérement modifiées (première colonne doit correspondre soit au code, code INSEE ou name), puis importées dans l'outil. Une chose importante a été rajoutée pour voir l'évolution d'habitants en cliquant sur arrondissement (Tooltips: {{ code }} arrondissement, en 1968: {{ _1968 }} habitants; en 1975: {{ _1975 }} habitants).

<iframe title="" aria-label="Carte" id="datawrapper-chart-Z2G3Y" src="https://datawrapper.dwcdn.net/Z2G3Y/1/" scrolling="no" frameborder="0" style="border: none;" width="690" height="411"></iframe>

Grace à la deuxième visualisation cartographique, nous pouvons visualiser l'emplacement de chaque arrondissement, ainsi que voir la densité de population en 2017 et en cliquant sur chaque arrondissement le nombre d'habitants entre 1968 et 2012.

## 4. Traitement des données de prix moyens par arrondissement

Les données que nous avons pu récupérer [ici] (https://basebien.com/PNSPublic/DocPublic/HistoriquedesprixaumappartementsanciensParispararrdt.pdf). 
Ces données représente une historique des prix au m2 standardisés des appartements anciens à Paris par arrondissement.Les données de la Base BIEN sont issues des actes authentiques signés dans les offices notariaux français. 
Les modifications suivantes ont été réalisées: changement du format (pdf vers csv), calcul du prix moyen par année, suppression des années pour lequelles nos ne possèdons pas d'informations (2020-2018), positionnement des lignes et des colonnes modifiés pour pouvoir faire une datavisualisation.

| Trimestre | Centre   | 1er      |    2e    |    3e    |    4e    |    5e    |    6e    |    7e    |
|-----------|----------|----------|:--------:|:--------:|:--------:|:--------:|:--------:|:--------:|
| T3 2020   | 12 870 € | 13 940 € | 12 250 € | 12 650 € | 13 660 € | 12 750 € | 14 590 € | 14 100 € |
| T2 2020   | 12 860 € | 13 100 € | 12 570 € | 12 820 € | 13 480 € | 12 740 € | 14 250 € | 14 020 € |
| T1 2020   | 12 340 € | 12 990 € | 11 830 € | 12 540 € | 12 640 € | 12 640 € | 14 250 € | 13 480 € |
| T4 2019   | 12 470 € | 13 240 € | 11 830 € | 12 330 € | 13 200 € | 12 420 € | 13 610 € | 13 540 € |
| T3 2019   | 12 150 € | 12 890 € | 11 200 € | 12 200 € | 12 780 € | 12 110 € | 14 170 € | 13 310 € |
| T2 2019   | 12 140 € | 12 520 € | 11 860 € | 11 970 € | 12 610 € | 11 880 € | 13 850 € | 12 850 € |
| T1 2019   | 11 780 € | 12 020 € | 11 630 € | 11 430 € | 12 710 € | 11 530 € | 13 740 € | 12 870 € |
| T4 2018   | 11 950 € | 12 060 € | 11 200 € | 11 880 € | 13 050 € | 11 390 € | 13 330 € | 12 680 € |
| T3 2018   | 11 820 € | 12 780 € | 11 360 € | 11 300 € | 12 750 € | 11 800 € | 13 000 € | 12 350 € |
| T2 2018   | 11 580 € | 12 270 € | 11 250 € | 11 150 € | 12 340 € | 11 290 € | 12 640 € | 12 310 € |
| T1 2018   | 11 330 € | 12 050 € | 11 120 € | 11 020 € | 11 860 € | 11 420 € | 12 600 € | 11 810 € |
| T4 2017   | 11 160 € | 11 560 € | 10 890 € | 11 170 € | 11 540 € | 11 100 € | 12 360 € | 11 530 € |
| T3 2017   | 11 130 € | 11 380 € | 10 590 € | 11 020 € | 11 840 € | 11 210 € | 12 020 € | 11 980 € |
| T2 2017   | 10 750 € | 11 060 € | 10 080 € | 10 310 € | 11 990 € | 11 010 € | 12 090 € | 11 690 € |
| T1 2017   | 10 750 € | 11 410 € |  9 830 € | 10 490 € | 11 630 € | 11 040 € | 11 730 € | 10 720 € |
| T4 2016   | 10 380 € | 10 250 € |  9 630 € | 10 260 € | 11 310 € | 10 720 € | 11 240 € | 11 130 € |
| T3 2016   | 10 410 € | 10 860 € |  9 920 € |  9 740 € | 11 550 € | 10 510 € | 11 250 € | 11 060 € |
| T2 2016   | 10 230 € | 10 630 € |  9 230 € |  9 960 € | 11 300 € | 10 390 € | 11 330 € | 11 230 € |
| T1 2016   | 10 060 € | 10 390 € |  9 670 € |  9 610 € | 11 330 € |  9 910 € | 11 370 € | 11 070 € |
| T4 2015   | 10 050 € | 11 030 € |  9 290 € |  9 550 € | 11 130 € | 10 300 € | 11 160 € | 10 860 € |
| T3 2015   | 10 120 € | 10 500 € |  9 560 € |  9 820 € | 11 520 € |  9 940 € | 11 560 € | 10 810 € |

> Tableau généré avec [Tables Generator](https://www.tablesgenerator.com)


Vous pouvez voir ci-dessus une partie les données finales:

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
| 12e |         8 178 € |         7 618 € |         7 530 € |         7 668 € |
| 13e |         8 098 € |         7 635 € |         7 353 € |         7 658 € |
| 14e |         8 805 € |         8 383 € |         8 240 € |         8 323 € |
| 15e |         8 855 € |         8 323 € |         8 163 € |         8 340 € |
| 16e |         9 358 € |         8 788 € |         8 570 € |         8 815 € |
| 17e |         8 880 € |         8 240 € |         8 000 € |         8 120 € |
| 18e |         8 008 € |         7 423 € |         7 130 € |         7 115 € |
| 19e |         7 035 € |         6 585 € |         6 483 € |         6 655 € |
| 20e |         7 458 € |         6 945 € |         6 768 € |         6 843 € |

> Tableau généré avec [Tables Generator](https://www.tablesgenerator.com)

## 5. Troisième datavisualisation avec Bar chart race (Flourish)

Pour visualiser ces données, nous avons décidé d'utiliser Bar chart race sur Flourish, ce que nous a permit avoir la visualisation dynamique au fil des années.

<iframe src='https://flo.uri.sh/visualisation/5154066/embed' title='Interactive or visual content' frameborder='0' scrolling='no' style='width:100%;height:600px;'></iframe><div style='width:100%!;margin-top:4px!important;text-align:right!important;'><a class='flourish-credit' href='https://public.flourish.studio/visualisation/5154066/?utm_source=embed&utm_campaign=visualisation/5154066' target='_top' style='text-decoration:none!important'><img alt='Made with Flourish' src='https://public.flourish.studio/resources/made_with_flourish.svg' style='width:105px!important;height:16px!important;border:none!important;margin:0!important;'> </a></div>


## 6. Visualisation de Paris avec Wikidata Query Service
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

> Si il y ac des images qui vous intéresse, vous pouvez voir le titre de lieu, ainsi que ses coordonnées géographiques.

<iframe style="width: 55vw; height: 50vh; border: none;" src="https://query.wikidata.org/embed.html#%23defaultView%3AImageGrid%0ASELECT%0A%20%20%3Farr%0A%20%20%28SAMPLE%20%28%3FtitleL%29%20AS%20%3Ftitle%29%0A%20%20%28SAMPLE%20%28%3Fimg%29%20AS%20%3Fimage%29%0A%20%20%28SAMPLE%20%28%3Fcoord%29%20AS%20%3Fcoordinates%29%20%7B%0A%0A%20%20%20%20%7B%0A%20%20%20%20%20%20SELECT%20DISTINCT%20%3Farr%20%7B%0A%20%20%20%20%20%20%20%20%3Farr%20%20wdt%3AP131%20wd%3AQ90%3B%7D%0A%20%20%20%20%7D%0A%20%20%20%20%23%20title%0A%20%20%20%20OPTIONAL%20%7B%20%3Farr%20rdfs%3Alabel%20%3FtitleL%20filter%20%28lang%28%3FtitleL%29%20%3D%20%22fr%22%29%20%7D%0A%20%20%20%0A%20%20%20%20%23%20image%0A%20%20%20%20OPTIONAL%20%7B%20%3Farr%20wdt%3AP18%20%3Fimg%20%7D%0A%20%20%20%0A%20%20%20%20%23%20coordinates%0A%20%20%20%20OPTIONAL%20%7B%20%3Farr%20wdt%3AP625%20%3Fcoord%20%7D%0A%0A%7D%20GROUP%20BY%20%3Farr%0ALIMIT%201500" referrerpolicy="origin" sandbox="allow-scripts allow-same-origin allow-popups" ></iframe>


Voir si c'est vrai: 

De 1990 à 1997 : une longue phase de baisse. En 7 ans, les prix en euros constants ont baissé de 42 %, soit -7.4 % en rythme annuel. Le marché est déprimé avec un nombre de vente qui est bien inférieur à celui des périodes précédentes.
De 1998 à 2008 : une longue hausse nationale (plus de 10 ans). Les volumes de vente sont très importants durant toute cette période. Les prix en euros constants augmentent de 141 %, soit +9.2 % en rythme annuel. Les notaires précisent que cette période a été boostée par un “contexte économique bien orienté” et surtout par un “crédit bancaire facile et bon marché”.
De 2008 à 2009 : la crise de liquidités et la paralysie bancaire. Les prix diminuent mais pendant une courte période (-4 % en euros constants).
De 2009 à 2011 : très forte envolée à Paris. En plus du fait que certains particuliers considèrent l’immobilier à Paris comme une valeur refuge, les banques centrales ont fait chuter les taux d’intérêt et le gouvernement a injecté des milliards d’euros pour relancer le marché immobilier.
Le résultat donne une véritable explosion des prix à Paris sur cette période : +35 % en euros constants en deux ans seulement. Une hausse a un rythme similaire à l’emballement de 1984-1990. Seulement celle-ci n’aura été que de deux ans, contre six pour la précédente flambée similaire.
De 2011 à 2013 : les notaires parlent de stagnation pour cette dernière phase. Les prix ne baissent que légèrement (-4 % en deux en euros constants, -2.3 % en rythme annuel). Ce sont surtout les volumes de vente qui s’ajustent.

## Conclution
#### Gestion du projet:

Ce projet nous a permis de vivre pleinement le processus qui s'appelle Data Wrangling, en partant des données brutes, nous avons réussi de les découvrir, structurer, valider et de publier les résultats sur cette page de github.

Complexités: les données brutes étaient mieux formatées ous xslx, que sous csv. Il faut adapter les données à chaque application, chaque application ayant ses limites (Flourish ne permet pas d'illustrer la variation faible des données, Datawrapper ne permet pas de faire un storytelling pour voir la densité de popoulation par année, Wikidata Query Service ne permet pas spécifier/filtrer le type de photos à afficher (uniquement de l'exterier, pas de plan/schèma de Paris et assez récentes)). L'bsence de données sur les prix de l'immobilier depuis 1968. 

#### Sujet: 
Le sujet en question présente pour moi un intéret particulier. En effet, il était intéressant de se pencher sur l'évolution de population par arrondissement. Grace aux plusieurs types de datavisualisation, nous avons pu mettre en avant differents problèmatiques. En outre, nous avons essayé de faire un lien entre l'évolution de population avec celle des prix de l'immobilier pour comprendre les raisons de ces changements.Sans parler, du coté esthétique, les photos de Paris à la fin. 

