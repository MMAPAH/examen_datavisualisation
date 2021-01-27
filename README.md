# Projet de datavisualisation - Arrondissements de Paris

![arrondissement de paris](https://lh3.googleusercontent.com/proxy/cBGnHZlcpeen8_ueDc7JRoC7o3r2UwBtVurtDdw8VE3hIWe9-enWEJBCtVjwdCiZ144P9tWNEgiBe8eSvI-CqLSNcoSr3EQN1m4dnknQvCaKfPA5lgTlDy4I3KpOnvOYsCnaah5bKlFmxu22Bf70KBKI0gOsPf_wwbY3feyhHW8)

# Table des matières

1. [Origine et traitement des données](##OrigineEtTraitemenDesDonnées)
2. [Première datavisualisation avec l'outil Flourish](##1datavizFlourish)
3. [Deuxième datavisualisation avec l'outil Datawrapper](##2datavizDatawrapper)
4. [Troisième datavisualisation avec l'outil OpenRefine](##3datavizOpenrefine)
5. [Visualisation de Paris avec Wikidata Query Service](##4queryWikiData)

## Origine et traitement des données

Les données de l'évolution démographique au fil des années ont été trouvées sur [INSEE](https://www.insee.fr/fr/statistiques/4515941#consulter). Nous avons décidé de garder uniquement la partie qui nous intéresse: arrondissement, année, population. Les données d'origine étant bien définie, nous n'avons pas eu à réaliser de travaux préparatoires ni a utiliser d'outils particuliers. Sur la base de ces trois informations, nous avons décidé de visualiser l'évolution des arrondissements de Paris entre 1970 et 2015.

Données brutes:

Données finales:
| District |  1968  |  1975  |  1982  |  1990  |  1999  |  2007  |  2012  |  2017  |
|:--------:|:------:|:------:|:------:|:------:|:------:|:------:|:------:|:------:|
| 1        | 32332  | 22793  | 18509  | 18360  | 16888  | 17915  | 17100  | 16266  |
| 2        | 35357  | 26328  | 21203  | 20738  | 19585  | 21745  | 22390  | 20900  |
| 3        | 56252  | 41706  | 36094  | 35102  | 34248  | 34576  | 35991  | 34115  |
| 4        | 54029  | 40466  | 33990  | 32226  | 30675  | 28572  | 27769  | 28088  |
| 5        | 83721  | 67668  | 62173  | 61222  | 58849  | 62664  | 60179  | 58850  |
| 6        | 70891  | 56331  | 48905  | 47891  | 44919  | 45332  | 43224  | 41100  |
| 7        | 87811  | 74250  | 67461  | 62939  | 56985  | 57410  | 57092  | 51367  |
| 8        | 67897  | 52999  | 46403  | 40814  | 39314  | 39165  | 38749  | 36808  |
| 9        | 84969  | 70270  | 64134  | 58019  | 55838  | 58632  | 59474  | 59555  |
| 10       | 113372 | 94046  | 86970  | 90083  | 89612  | 93373  | 94474  | 90372  |
| 11       | 179727 | 159317 | 146931 | 154165 | 149102 | 151421 | 155006 | 146643 |
| 12       | 155982 | 140900 | 138015 | 130257 | 136591 | 142425 | 144925 | 140296 |
| 13       | 158280 | 163313 | 170818 | 171098 | 171533 | 179213 | 182386 | 182099 |
| 14       | 167093 | 149137 | 138596 | 136574 | 132844 | 134382 | 141102 | 135964 |
| 15       | 244080 | 231301 | 225596 | 223940 | 225362 | 232247 | 238190 | 233392 |
| 16       | 214120 | 193590 | 179446 | 169863 | 161773 | 159706 | 167613 | 166361 |
| 17       | 210299 | 186293 | 169513 | 161935 | 160860 | 164673 | 170156 | 167288 |
| 18       | 236776 | 208970 | 186866 | 187657 | 184586 | 191523 | 201374 | 195233 |
| 19       | 148862 | 144357 | 162649 | 165062 | 172730 | 184038 | 186116 | 187015 |
| 20       | 188921 | 175795 | 171971 | 184478 | 182952 | 194018 | 197311 | 195814 |

> Générer avec [Tables Generator](https://www.tablesgenerator.com)

## Première datavisualisation avec l'outil Flourish

Pour créer le visuel des données récoltées, nous avons décidé d'utiliser le graphique  "Line Chart Race" avec trois paramètres suivantes: année, arrondissement et population. C'est un graphique en relief qui est souvent utilisé pour visualiser efficacement le classement des données (dans notre cas les arrondissements) à travers différentes mesures (population) au fil du temps. 

<iframe src='https://flo.uri.sh/visualisation/4874798/embed' title='Interactive or visual content' frameborder='0' scrolling='no' style='width:100%;height:600px;'></iframe><div style='width:100%!;margin-top:4px!important;text-align:right!important;'><a class='flourish-credit' href='https://public.flourish.studio/visualisation/4874798/?utm_source=embed&utm_campaign=visualisation/4874798' target='_top' style='text-decoration:none!important'><img alt='Made with Flourish' src='https://public.flourish.studio/resources/made_with_flourish.svg' style='width:105px!important;height:16px!important;border:none!important;margin:0!important;'> </a></div>

Comme vous pouvez le voir certaines arrondissements n'ont pas évolué au fils des années. Sachant que les données changeaient bien au fil des années, nous nous solmes rendus compte qu'il s'agit de graphique, voir outil qui ne permet pas illustrer la variation faible des données. 


## Deuxième datavisualisation avec l'outil Datawrapper

Cette datavisualisation a été réalisé en choisissant une carte des arrondissements De Paris (peu d'outils l'ont), ensuite, nos données ont été légérement modifiées (premier colonne doit correcpondre soit au code, code INSEE ou name), puis importées dant l'outil. Une chose importante a été rajoutée pour voir l'évolution d'habitants en cliquant sur arrondissement (Tooltips: {{ code }} arrondissement, en 1968: {{ _1968 }} habitants; en 1975: {{ _1975 }} habitants).

<iframe title="" aria-label="Carte" id="datawrapper-chart-Z2G3Y" src="https://datawrapper.dwcdn.net/Z2G3Y/1/" scrolling="no" frameborder="0" style="border: none;" width="600" height="411"></iframe>

Grace à la deuxième visualisation cartographique, nous pouvons visualiser l'emplacemment de chaque arrondissement, ainsi que voir la dentité de population en 2017 et en cliquant sur chaque arrondissement le nombre d'habitants entre 1968 et 2012.

## Troisième datavisualisation avec l'outil OpenRefine

## Visualisation de Paris avec Wikidata Query Service
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

<iframe style="width: 40vw; height: 50vh; border: none;" src="https://query.wikidata.org/embed.html#%23defaultView%3AImageGrid%0ASELECT%0A%20%20%3Farr%0A%20%20%28SAMPLE%20%28%3FtitleL%29%20AS%20%3Ftitle%29%0A%20%20%28SAMPLE%20%28%3Fimg%29%20AS%20%3Fimage%29%0A%20%20%28SAMPLE%20%28%3Fcoord%29%20AS%20%3Fcoordinates%29%20%7B%0A%0A%20%20%20%20%7B%0A%20%20%20%20%20%20SELECT%20DISTINCT%20%3Farr%20%7B%0A%20%20%20%20%20%20%20%20%3Farr%20%20wdt%3AP131%20wd%3AQ90%3B%7D%0A%20%20%20%20%7D%0A%20%20%20%20%23%20title%0A%20%20%20%20OPTIONAL%20%7B%20%3Farr%20rdfs%3Alabel%20%3FtitleL%20filter%20%28lang%28%3FtitleL%29%20%3D%20%22fr%22%29%20%7D%0A%20%20%20%0A%20%20%20%20%23%20image%0A%20%20%20%20OPTIONAL%20%7B%20%3Farr%20wdt%3AP18%20%3Fimg%20%7D%0A%20%20%20%0A%20%20%20%20%23%20coordinates%0A%20%20%20%20OPTIONAL%20%7B%20%3Farr%20wdt%3AP625%20%3Fcoord%20%7D%0A%0A%7D%20GROUP%20BY%20%3Farr%0ALIMIT%201500" referrerpolicy="origin" sandbox="allow-scripts allow-same-origin allow-popups" ></iframe>


## Conclution:



