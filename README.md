# Projet de datavisualisation: Arrondissements de Paris

![arrondissement de paris](https://www.de-nicher.com/wp-content/uploads/sites/5/2019/06/carte-arrondissements-off.jpg)



# Table des matières

1. [Origine et traitement des données](##OrigineEtTraitementDesDonnées)
2. [Première datavisualisation avec l'outil Flourish](##1datavizFlourish)
3. [Deuxième datavisualisation avec l'outil Datawrapper](##2datavizDatawrapper)
4. [Troisième datavisualisation avec l'outil OpenRefine](##3datavizOpenrefine)
5. [Visualisation de Paris avec Wikidata Query Service](##4queryWikiData)

## 1. Origine et traitement des données

Les données de l'évolution démographique au fil des années ont été trouvées sur [INSEE](https://www.insee.fr/fr/statistiques/4515941#consulter). Nous avons décidé de garder uniquement la partie qui nous intéresse: arrondissement, année, population. Les données d'origine étant bien définie, nous n'avons pas eu à réaliser de travaux préparatoires ni a utiliser d'outils particuliers. Sur la base de ces trois informations, nous avons décidé de visualiser l'évolution des arrondissements de Paris entre 1970 et 2015.

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

## 2. Première datavisualisation avec l'outil Flourish

Pour créer le visuel des données récoltées, nous avons décidé d'utiliser le graphique  "Line Chart Race" avec trois paramètres suivantes: année, arrondissement et population. C'est un graphique en relief qui est souvent utilisé pour visualiser efficacement le classement des données (dans notre cas les arrondissements) à travers différentes mesures (population) au fil du temps. 

<iframe src='https://flo.uri.sh/visualisation/4874798/embed' title='Interactive or visual content' frameborder='0' scrolling='no' style='width:100%;height:600px;'></iframe><div style='width:100%!;margin-top:4px!important;text-align:right!important;'><a class='flourish-credit' href='https://public.flourish.studio/visualisation/4874798/?utm_source=embed&utm_campaign=visualisation/4874798' target='_top' style='text-decoration:none!important'><img alt='Made with Flourish' src='https://public.flourish.studio/resources/made_with_flourish.svg' style='width:105px!important;height:16px!important;border:none!important;margin:0!important;'> </a></div>

Comme vous pouvez le voir certaines arrondissements n'ont pas évolué au fils des années. Sachant que les données changeaient bien au fil des années, nous nous solmes rendus compte qu'il s'agit de graphique, voir outil qui ne permet pas illustrer la variation faible des données. 


## 3. Deuxième datavisualisation avec l'outil Datawrapper

Cette datavisualisation a été réalisé en choisissant une carte des arrondissements De Paris (peu d'outils l'ont), ensuite, nos données ont été légérement modifiées (première colonne doit correspondre soit au code, code INSEE ou name), puis importées dans l'outil. Une chose importante a été rajoutée pour voir l'évolution d'habitants en cliquant sur arrondissement (Tooltips: {{ code }} arrondissement, en 1968: {{ _1968 }} habitants; en 1975: {{ _1975 }} habitants).

<iframe title="" aria-label="Carte" id="datawrapper-chart-Z2G3Y" src="https://datawrapper.dwcdn.net/Z2G3Y/1/" scrolling="no" frameborder="0" style="border: none;" width="690" height="411"></iframe>

Grace à la deuxième visualisation cartographique, nous pouvons visualiser l'emplacement de chaque arrondissement, ainsi que voir la densité de population en 2017 et en cliquant sur chaque arrondissement le nombre d'habitants entre 1968 et 2012.

## 4. Troisième datavisualisation avec l'outil OpenRefine

Voir si je peux récupérer les données ici: https://m2paris.fr

## 5. Visualisation de Paris avec Wikidata Query Service
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


## Conclution
#### Gestion du projet:

Complexités: les données brutes étaient mieux formatées ous xslx, que sous csv. Il faut adapter les données à chaque application,chaque application ayant ses limites (Flourish ne permet pas d'illustrer la variation faible des données, Datawrapper ne permet pas de faire un storytelling pour voir la densité de popoulation par année). L'bsence de données sur les prix de l'immobilier depuis 1968. 

#### Sujet: 
Le sujet en question présente pour moi un intéret particulier. En effet, il était intéressant de se pencher sur l'évolution de population par arrondissement. Grace aux différents types de datavisualisation, nous avons pu mettre en avant differents problèmatiques. En outre, nous avons essayé de faire un lien entre l'évolution de population avec celle des prix de l'immobilier pour comprendre les raisons de ces changements.

