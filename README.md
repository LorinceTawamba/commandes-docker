# COMMANDES DOCKER

<H3>Voici la liste des commandes Docker que j'utilise au quotidien pour optimiser mon travail.</H3>

## Table des matières

- [Générales](#générales)
- [Images](#images) 
- [Docker Hub](#docker-hub) 
- [Conteneurs](#conteneurs)
- [Contributeurs](#contributeurs)

## Générales

1. **Obtenir de l'aide sur les commandes docker :**

    ```properties
    docker --help
    ```
   
1. **Version de docker disponible sur la machine :**

    ```properties
    docker --version
    ```

1. **Obtenir les informations sur docker :**

    ```properties
    docker info
    ```

## Images 

1. **Créer une image à partir d'un Dockerfile :**

    ```properties
    docker build -t <image_name>:<tag> .
    ```

1. **Créer une image à partir d'un Dockerfile sans le cache :**

    ```properties
    docker build -t <image_name> . –no-cache
    ```

1. **Obtenir la liste des images docker en local :**

    ```properties
    docker images
    ```

1. **Supprimer une image docker :**

    ```properties
    docker rmi <image_name>
    ```

1. **Supprimer toutes les images docker inutilisées :**

    ```properties
    docker image prune
    ```

## Docker Hub 

1. **Se connecter à Docker :**

    ```properties
    docker login -u <username>
    ```

1. **Publier une image sur Docker Hub :**

    ```properties
    docker push <username>/<image_name or image_ID>
    ```

1. **Rechercher une image sur Docker Hub :**

    ```properties
    docker search <image_name>
    ```

1. **Extraire une image Docker depuis un Docker Hub :**

    ```properties
    docker pull <image_name>
    ```

## Conteneurs  

1. **Créer et exécuter un conteneur à partir d'une image, avec un nom personnalisé :**

    ```properties
    docker run --name <container_name> <image_name>
    ```

1. **Exécutez un conteneur et publiez les ports d’un conteneur sur l’hôte :**

    ```properties
    docker run -p <host_port>:<container_port> <image_name>
    ```

1. **Exécuter un conteneur en arrière-plan :**

    ```properties
    docker run -d <image_name>
    ```

1. **Démarrer un conteneur existant :**

    ```properties
    docker start <container_name> (or <container-id>)
    ```

1. **Arrêter un conteneur existant :**

    ```properties
    docker stop <container_name> (or <container-id>)
    ```

1. **Arrêter plusieurs conteneurs :**

    ```properties
    docker stop <container_name1> (or <container-id1>) <container_name2> (or <container-id2>) <container_name3> (or <container-id3>)
    ```

1. **Redémarrer le conteneur :**

    ```properties
    docker restart <container_name> (or <container-id>)
    ```

1. **Arrêter et retirer un conteneur :**

    ```properties
    docker rm {options} <container_name or ID>
    ```

1. **Ouvrir un shell à l'intérieur d'un conteneur en cours d'exécution :**

    ```properties
    docker exec -it <container_name> sh
    ```

1. **Récupérer et suivre les journaux d'un conteneur :**

    ```properties
    docker logs -f <container_name>
    ```

1. **Inspecter un conteneur en cours d'exécution :**

    ```properties
    docker inspect <container_name> (or <container_id>)
    ```

1. **Répertorier les conteneurs actuellement en cours d'exécution :**

    ```properties
    docker ps [options..]

		--a flag:  shows us all the containers, stopped or running.
		--l flag: shows us the latest container.
		--q flag: shows only the Id of the containers. 
    ```

1. **Lister tous les conteneurs Docker (en cours d'exécution et arrêtés) :**

    ```properties
    docker ps --all
    ```

1. **Afficher les statistiques d'utilisation des ressources :**

    ```properties
    docker container stats
    ```

1. **Exécuter de nouvelles commandes dans un conteneur en cours d'exécution :**

    ```properties
    docker exec {options} 

		--d flag: for running the commands in the background.
		--i flag: it will keep STDIN open even when not attached.
		--e flag: sets the environment variables
    ```

1. **Correspondance des ports :**

    ```properties
    docker run -d -p <port_on_host>:<port_on_container> <container_name> 
    ```

1. **Après avoir exécuté les conteneurs en utilisant l'image actuelle, vous pouvez effectuer les mises à jour des conteneurs en interagissant avec les conteneurs à partir de ces conteneurs. Vous pouvez créer une image en utilisant les commandes suivantes :**

    ```properties
    docker commit <container_name> (or <container_id>) <new_image_name>:tag  
    ```

1. **Sauvegarder le conteneur avec l'information de l'auteur :**

    ```properties
    docker commit -a "Author Name" <container_name> (or <container_id>) <new_image_name>:tag 
    ```

1. **Sauvegarder le conteneur avec un message :**

    ```properties
    docker commit -m "Your message here" <container_name> (or <container_id>) <new_image_name>:tag
    ```

1. **Detruire le conteneur :**

    ```properties
    docker kill <container_name> (or <container_id>)
    ```


## Contributeurs

- [Lorince Tawamba](https://github.com/LorinceTawamba)

---

Happy coding! 
