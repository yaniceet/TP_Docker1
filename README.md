# TP Docker
## Partie 1 Database
### Question 1-1: Cela nous évite d’écrire des mots de passe visible dans l’image et permettre de changer la configuration à l’exécution sans reconstruire l’image 
# TP partie 02
### Question 2-1: Les Testcontainers sont une bibliothèque Java faite pour faciliter les Tests d'Intégration en fournissant des dépendances de services courantes comme les bases de données sous forme de conteneurs Docker jetables.
### Question 2-2: On les utilise pour protéger les identifiants comme le nom d'utilisateur et le mot de passe Docker Hub (DOCKER_USERNAME et DOCKER_PASSWORD), ils sont chiffrés et ne sont jamais exposés en clair dans le code du workflow (main.yml) ou dans les logs d'exécution publics de GitHub Actions.
