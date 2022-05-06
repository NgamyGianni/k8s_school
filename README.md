# Déploiement d'un couple (serveur - base de données) sur kubernetes

## Problème

Il nous a été demandé de créer 2 conteneurs à partir de 2 images et de leur permettre d'interagir entre eux dans un kubernetes.

## Stratégie

Le travail se divise en 2 parties :
    - le déploiement du serveur (node-redis)
    - le déploiement de la base de donnée (redis)

Pour cela, j'ai opté pour la création de 2 conteneurs. Le premier, pour le déploiement du serveur nécessite la création de 3 fichiers, un pour le déploiement, un pour le service et un pour le (ou les) pod, tandis que le deuxième, pour le déploiement de la base de donnée nécessite la création de 2 fichiers, un pour le déploiement et un pour le service. 

## Architecture

Les fichiers commençants par "gianni_deployment" seront utilisés pour configurer et déployer les conteneurs.
Les fichiers commençants par "gianni_service" seront utilisés pour configurer les services.
Les fichiers commençants par "gianni_pod" seront utilisés pour configurer les pods.