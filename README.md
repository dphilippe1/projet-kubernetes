# projet-kubernetes

----------- Nathan RAILLON et Damien PHILIPPE ------------

Concernant la mise en place de Grafana couplé à Prometheus sur Kubernetes, voici les étapes nécessaires :

Tout d'abord, il est nécessaire d'installer Prometheus sur le cluster Kubernetes en utilisant un fichier de configuration Prometheus approprié. Cela est réalisé en utilisant un fichier de déploiement Kubernetes, qui définit les conteneurs nécessaires et les ressources requises.

Ensuite, il est nécessaire de configurer Prometheus pour collecter des métriques à partir des conteneurs Kubernetes en utilisant le module de collecte de métriques Kubernetes de Prometheus. Ceci est réalisé en ajoutant des annotations aux conteneurs pour indiquer à Prometheus quelles métriques collecter.

Ensuite, il faut installer Grafana en utilisant un fichier de déploiement Kubernetes.

Pour cela il est important de configurer Grafana pour se connecter à Prometheus en tant que source de données. Cela peut être fait en ajoutant une "datasource" Prometheus dans les paramètres de Grafana, soit en spécifiant l'URL d'accès à Prometheus, soit via l'interface graphique de Grafana.

À la suite de ces étapes, il est possible de créer des tableaux de bord Grafana pour afficher les métriques collectées par Prometheus en utilisant les widgets Grafana pour visualiser les données, et des requêtes Prometheus pour les récupérer.


Concernant la partie applicative wordpress :

Le dossier wordpress contient 3 fichiers distincts :
- un fichier kustomization.yaml qui est un outil permettant de modeler les configurations Kubernetes et de gérer des collections de configurations
- un fichier wordpress-deployment.yaml qui contient la configuration relative au déploiement de la partie applicative web et du CMS Wordpress
- un fichier mysql-deployment qui contient la partie "backend" avec le déploiement relatif à la base de données

L'implémentation de l'ensemble de l'application Wordpress s'effectue grâce au fichier kustomisation.yaml qui permet lancer simulatanément le "frontend" et le "backend" ainsi que de générer un mot de passe (secret) pour l'accès à la base de données mysql.
