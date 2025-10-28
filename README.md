# TP Docker
## Partie 1 Database
### Question 1-1: Cela nous évite d’écrire des mots de passe visible dans l’image et permettre de changer la configuration à l’exécution sans reconstruire l’image 
### Question 1-2: Nous avons besoin d'un volume Docker attaché à notre conteneur PostgreSQL pour garantir la persistance des données. Les données de cette base de données sont stockées sur le système de fichiers du serveur hôte distant.
### Question 1-3: Vu qu'on utilise une image de base de données comme PostgreSQL, il est plus facile d'utiliser directement l'image officielle du Docker Hub avec des commandes docker run ou docker-compose, au lieu que de créer un Dockerfile personnalisé.

# TP partie 02
### Question 2-1: Les Testcontainers sont une bibliothèque Java faite pour faciliter les Tests d'Intégration en fournissant des dépendances de services courantes comme les bases de données sous forme de conteneurs Docker jetables.
### Question 2-2: On les utilise pour protéger les identifiants comme le nom d'utilisateur et le mot de passe Docker Hub (DOCKER_USERNAME et DOCKER_PASSWORD), ils sont chiffrés et ne sont jamais exposés en clair dans le code du workflow (main.yml) ou dans les logs d'exécution publics de GitHub Actions.
### Question 2-3: needs: est essentiel car il définit l'ordre d'exécution entre les différentes tâches du pipeline. Nous utilisons needs: build-and-test-backend pour garantir que la tâche de construction et de publication de l'image Docker se lance seulement si la tâche d'Intégration Continue a réussi (est passé au vert). Cela empêche de gaspiller des ressources et d'exposer publiquement un risque, en construisant et en poussant une image Docker qui contiendrait du code qui ne compilera pas ou qui aura des tests échoués.
### Question 2-4: On push les images Docker pour les stocker dans un registre distant et centralisé afin qu'elles puissent être récupérées et utilisées par d'autres systèmes pour le déploiement.
# TP partie 3
## Facts
### Question 3-1: L'inventaire est la principale configuration d'Ansible. Il définit quels hôtes Ansible doit gérer et comment il doit s'y connecter. Les commandes de base sont des commandes simples exécutées une seule fois directement depuis la ligne de commande, sans utiliser de Playbook. Elles sont pratiques pour des tâches rapides et des vérifications.

