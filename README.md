# projet-kubernetes

----------- Nathan RAILLON et Damien PHILIPPE ------------

Cluster kubernetes réalisé dans le cadre d'un projet universitaire

Le premier noeud contient une application web composée d'un serveur web avec Wordpress généré via le fichier wordpress-deployment.yaml et d'une base de données mysql générée par le fichier mysql-deployment.yaml. Les deux services s'éxecutent sur deux pods différents.
Le fichier kustomization.yaml a été utilisé afin d'automatiser le déploiement des deux pods et de générer un mot de passe pour la partie base de données.
