Atelier-A1_MongoDB-avec-Docker
 A1 - MongoDB avec Docker

Pour cet exercice, j'ai commencé par configurer MongoDB avec Docker Compose en utilisant l'image mongo:7.

J'ai créé le fichier compose.yaml pour définir le service, le port de connexion, les identifiants ainsi que le volume qui permet de conserver les données.

Une fois la configuration terminée, j'ai lancé le conteneur avec la commande docker compose up -d. J'ai ensuite vérifié qu'il était bien démarré avec docker compose ps.

Je me suis ensuite connectée à MongoDB depuis PowerShell avec mongosh, en utilisant les identifiants définis dans le fichier de configuration.

Dans MongoDB, j'ai sélectionné la base de données support, puis j'ai utilisé la commande updateOne pour ajouter ou mettre à jour un document dans la collection tickets.

Le document enregistré contient le code T-101 et le sujet Acces au portail. J'ai vérifié son enregistrement avec findOne.

Pour terminer, j'ai arrêté le conteneur avec docker compose down, puis je l'ai relancé avec docker compose up -d. Après m'être reconnectée à MongoDB, j'ai recherché le même document.

Il était toujours présent et son identifiant n'avait pas changé. Cela m'a permis de vérifier que les données étaient bien conservées grâce au volume mongo-data associé au répertoire /data/db.

Cet exercice m'a notamment permis de mieux comprendre le fonctionnement de Docker Compose, la connexion à une base MongoDB et l'intérêt des volumes pour conserver les données même après la suppression d'un conteneur.

Résultat : le service fonctionne et le test de persistance est validé.
