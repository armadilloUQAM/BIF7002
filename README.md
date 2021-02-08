Tutorial sur les CNN et les RNN pour l'analyse de séquences
============================================================

Ce répertoire inclus les fichiers pour la présentation : 
* L'utilisation de l'apprentissage profond dans l'analyse des séquences génomiques 

Usage 
==========================================

Pour ce tutorial, vous devez avoir une installation fonctionnelle de tensorflow, keras, seqinr et ggplot2 en R.

Exemple d'installation avec conda

conda env create --name deeplearning --file environment.yml

Une fois l'environnement créé, utilisez la commande suivante pour l'activer

conda activate deeplearning


Sur un ordinateur personnel, en utilisant RStudio
==================================================

Dans la console de RStudio:
1. Tapez: `install.packages("keras")`
2. Tapez: `library(keras)`
3. Tapez: `install_keras()` ou `install_keras(tensorflow = "gpu")`
4. Tapez: `install.packages("ggplot2")`
5. Tapez: `install.packages("seqinr")` 
6. Ouvrir le fichier dpsites.R ou dpsites_LSTM.R 
7. Dans le menu Session, Utilisez la commande: Set the Working Directory to -> Source file location
8. Executez le code

* La librairie keras est une api pour faire de l'apprentissage profond. La librairie  ggplot2 est pour la visualisation des résultats. *
* La librairie seqinr est utilisée pour charger les fichiers fasta *

Ce tutorial comprend différents fichiers
==========================================

Le fichier *dpsites.R* décrit un 1D CNN utilisé pour détecter des sites de clivages dans des séquences protéiques. 
Executer la commande: RScript dpsites.R

Le fichier *dpsites_LSTM.R* décrit l'utilisation d'un LSTM pour accomplir la même tâche, avec une plus haute précision avec des 'cellules mémoires'.
Executer la commande: RScript dpsites_LSTM.R

Le fichier *sequences.txt* contient des domaines de clivages pour la NIa protease du Plum pox virus.

Le fichier *labels.txt* contient des 'labels' soit 0 pour un site alléatoire non-clivable ou 1 pour un site de clivage. 

Le fichier *test.fasta*  contient la polyprotéine du Plum pox virus.

Le fichier *Example_DPSite.R.pdf* présente une vue graphique des résultats. 


Ce code est largement inspiré de l'article:

Zou, J., Huss, M., Abid, A., Mohammadi, P., Torkamani, A., & Telenti, A. (2018). A primer on deep learning in genomics. Nat Genet. 2019 Jan;51(1):12-18. doi: 10.1038/s41588-018-0295-5.

