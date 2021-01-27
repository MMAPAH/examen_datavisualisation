# Projet de datavisualisation - Arrondissements de Paris

![arrondissement de paris](https://lh3.googleusercontent.com/proxy/cBGnHZlcpeen8_ueDc7JRoC7o3r2UwBtVurtDdw8VE3hIWe9-enWEJBCtVjwdCiZ144P9tWNEgiBe8eSvI-CqLSNcoSr3EQN1m4dnknQvCaKfPA5lgTlDy4I3KpOnvOYsCnaah5bKlFmxu22Bf70KBKI0gOsPf_wwbY3feyhHW8)

# Table des matières

1. [Origine et traitement des données](##OrigineEtTraitemenDesDonnées)
2. [Première datavisualisation avec l'outil Flourish](##1datavizFlourish)
3. [Deuxième datavisualisation avec l'outil Datawrapper](##2datavizDatawrapper)
4. [Troisième datavisualisation avec l'outil WikiData](##3datavizWikiData)

## Origine et traitement des données

Les données de l'évolution démographique au fil des années ont été trouvées sur [INSEE](https://www.insee.fr/fr/statistiques/4515941#consulter). Nous avons décidé de garder uniquement la partie qui nous intéresse: arrondissement, année, population. Les données d'origine étant bien définie, nous n'avons pas eu à réaliser de travaux préparatoires ni a utiliser d'outils particuliers. Sur la base de ces trois informations, nous avons décidé de visualiser l'évolution des arrondissements de Paris entre 1970 et 2015.

## Première datavisualisation avec l'outil Flourish

Pour créer le visuel des données récoltées, nous avons décidé d'utiliser le graphique  "Line Chart Race" avec trois paramètres suivantes: année, arrondissement et population. C'est un graphique en relief qui est souvent utilisé pour visualiser efficacement le classement des données (dans notre cas les arrondissements) à travers différentes mesures (population) au fil du temps. 

<iframe src='https://flo.uri.sh/visualisation/4874798/embed' title='Interactive or visual content' frameborder='0' scrolling='no' style='width:100%;height:600px;'></iframe><div style='width:100%!;margin-top:4px!important;text-align:right!important;'><a class='flourish-credit' href='https://public.flourish.studio/visualisation/4874798/?utm_source=embed&utm_campaign=visualisation/4874798' target='_top' style='text-decoration:none!important'><img alt='Made with Flourish' src='https://public.flourish.studio/resources/made_with_flourish.svg' style='width:105px!important;height:16px!important;border:none!important;margin:0!important;'> </a></div>

Comme vous pouvez le voir certaines arrondissements n'ont pas évolué au fils des années. Sachant que les données changeaient bien au fil des années, nous nous solmes rendus compte qu'il s'agit de graphique, voir outil qui ne permet pas illustrer la variation faible des données.

## Deuxième datavisualisation avec l'outil Datawrapper

<iframe title="" aria-label="Carte" id="datawrapper-chart-Z2G3Y" src="https://datawrapper.dwcdn.net/Z2G3Y/1/" scrolling="no" frameborder="0" style="border: none;" width="600" height="411"></iframe>

Grace à la deuxième visualisation cartographique, nous pouvons voir les arrondissements les plus peuplées.

## Visualisation de Paris avec Wikidata Query Service
```sparql
#defaulView:ImageGrid
SELECT DISTINCT ?arr ?image
WHERE {?arr wdt:P131 wd:Q90; # c'est un arrondissement de paris 
            wdt:P18 ?image # avec une image
       }
LIMIT 1000
```

<iframe style="width:100%;height:600px; border: none;" src="https://query.wikidata.org/embed.html#%23defaulView%3AImageGrid%0ASELECT%20DISTINCT%20%3Farr%20%3Fimage%0AWHERE%20%7B%3Farr%20wdt%3AP131%20wd%3AQ90%3B%20%23%20c%27est%20un%20arrondissement%20de%20paris%20%0A%20%20%20%20%20%20%20%20%20%20%20%20wdt%3AP18%20%3Fimage%20%23%20avec%20une%20image%0A%20%20%20%20%20%20%20%7D%0ALIMIT%201000%0A%0A%0A" referrerpolicy="origin" sandbox="allow-scripts allow-same-origin allow-popups" ></iframe>


## Conclution:


