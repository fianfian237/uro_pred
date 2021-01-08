# uro_pred

Des vidéos présentant des tumeurs (urologie) ont été présentées à une centaine d'urologue. Ces derniers devaient premièrement fournir leur description de la tumeur observée selon 8 critère (taille de la tumeur, nombre de caillots observés, la base de la tumeur est-elle fine ou épaisse, etc) avant de donner leur diagnostic sur la tumeur observée (tumeur à un stade avancé ou pas, tumeur bénine ou pas)

Un nettoyage a été effectué et deux modèles ont été entrainés et retenus. Ces modèles prédisent en fonction de valeurs correspondant aux 8 critères de description le stade et le grade de la tumeur correspondante

Ce dépôt permet donc de déployer une appli en local pour obtenir les résultats de la prédiction. Le frontend a été réalisé avec les module dash et plotly de python, le backend est un serveur nginx+gunicorn+flask où le modèle entrainé reçoit des requêtes https et renvoie les prédictions.

Pour l'installer et tester, il faut :
* d'abord avoir au préalable docker, docker-compose et git sur sa machine
* ensuite cloner le repo
* enfin exécuter le scipt shell - il clonera les repos correspondant au frontend et backend, en fera des containers docker et installera les dépendances
* Une fois l'installation terminée, il suffira de se rendre à l'adresse localhost:8050 dans son navigateur
