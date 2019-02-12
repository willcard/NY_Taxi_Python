# New York Taxi Python data visualisation

## Description du contexte

Dans le cadre de notre unité Python nous devions, en utilisant le langage Python, créer et générer des graphiques représentant les données et expliquant ces dernières.
Nous avons donc choisi d'utiliser les données kaggle suivante : https://www.kaggle.com/naveenkaveti/eda-10-points/data
Ce dataset regroupe les données recueillis sur les taxi new-yorkais lors de l'année 2016.

## Les données

Les données sont sous un format csv
Le fichier à une taille de 231,4 Mo
Vous pouvez télécharger les données à l'URL suivant : http://perso.esiee.fr/~coviller/NY_taxi.csv
Dans ce dataset, nous pouvons trouver différentes données intéressantes comme les lieux de départs et d'arrivées des courses de taxi, le moment de ces arrivées et départs, le nombre de passagers par taxi etc.
Pour plus de détail, nous vous invitons à aller sur la page kaggle qui explique de manière exhaustive le dataset (https://www.kaggle.com/naveenkaveti/eda-10-points/data)

## Création du dashboard

Afin que le notebook contenant nos différents graphiques puisse ce lancer correctement, il faut lancer jupyter avec la commande suivante : 
- jupyter notebook --NotebookApp.iopub_data_rate_limit=10000000000

Ainsi, comme notre dataset comprend un nombre très important de lignes, le notebook n'atteindra pas sa limite de base qui l'empêcherait d'afficher certains graphiques.

## Téléchagement du dataset
Le dataset étant important, son télécargement peut prende du temps.
Pour palier à cela, le dataset est fourni au format csv, il vous suffira de décommenter la ligne suivante (supprimer le # devant la ligne): 
- #dl_data = pd.read_csv("NY_taxi.csv")

Et de commenter ces deux lignes (rajouter un # devant chaque lignes) :
- data_url = "http://perso.esiee.fr/~coviller/NY_taxi.csv"
- dl_data = pd.read_csv(io.StringIO(requests.get(data_url).content.decode('utf-8')))
