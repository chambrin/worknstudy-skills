# Docker

> ❌ A travailler

> ✔️ Auto validation par l'étudiant

## 🎓 J'ai compris et je peux expliquer

- la création d'une image docker / ✔️
- l'éxécution d'un container  ✔️
- l'orchestration de containers avec docker-compose / ✔️


## 💻 J'utilise

### Un exemple personnel commenté  ✔️
```yml
version: '3' # Utilise la version 3 de la syntaxe de Docker Compose

services: # Définit les différents services de votre application

  # Configuration pour le service Frontend
  frontend:
    build: ./frontend # build le Dockerfile dans le dossier ./frontend
    ports:
      - '3000:3000' # expose le port 3000 du conteneur vers l'hôte
    depends_on:
      - backend # dépend du service backend
    deploy:
      resources:
        limits:
          cpus: '0.50' # limite la CPU à 50%
          memory: 2G # limite la mémoire à 2 GB

  # Configuration similaire pour le service Backend
  backend:
    build: ./backend
    ports:
      - '8000:8000'
    depends_on:
      - database
    deploy:
      resources:
        limits:
          cpus: '0.50'
          memory: 2G

  # Configuration pour la base de données
  database:
    build: ./database
    environment:
      POSTGRES_USER: ${POSTGRES_USER}
      POSTGRES_PASSWORD: ${POSTGRES_PASSWORD}
      POSTGRES_DB: ${POSTGRES_DB}
    ports:
      - '5432:5432'
    deploy:
      resources:
        limits:
          cpus: '0.50'
          memory: 4G # 4 GB pour la base de données

  # Configuration pour le service de documentation
  documentation:
    build: ./documentation
    volumes:
      - ./documentation/site:/usr/src/app # monte le volume vers /usr/src/app
    ports:
    - '8081:8081'
    deploy:
      resources:
        limits:
          cpus: '0.50'
          memory: 200M # 200 MB pour le service de documentation

  # Configuration pour le script
  script:
    build: ./script
    deploy:
      resources:
        limits:
          cpus: '0.50'
          memory: 2G

  # Configuration pour Portainer, un outil de gestion de conteneurs Docker
  portainer:
    image: portainer/portainer
    volumes:
      - /var/run/docker.sock:/var/run/docker.sock # connexion à Docker
    ports:
      - '9000:9000'

  # Configurations pour différents outils de surveillance (Prometheus, Grafana, Node Exporter)
  
  # Configuration pour PGAdmin, une interface web pour PostgreSQL
  pgadmin:
    image: dpage/pgadmin4
    environment:
      PGADMIN_DEFAULT ```yaml
      EMAIL: "pgadmin4@pgadmin.org"
      PGADMIN_DEFAULT_PASSWORD: "admin"
    deploy:
      resources:
        limits:
          cpus: '0.50'
          memory: 4G
    ports:
      - "5050:80"
    depends_on:
      - database # dépend du service database

```
### Utilisation dans un projet  ✔️

[lien github](https://github.com/chambrin/next.gold)

Description : Starter kit de dev

### Utilisation en production si applicable / ✔️

[lien du projet](https://www.npmjs.com/package/next-gold)

Description : 

### Utilisation en environement professionnel  ✔️

Description :Migrations d'un ancien serveur contenant plusieurs applications web, pour une meilleure maniabilité et gestion des applications, ainsi qu'intégration de pipelines.

## 🌐 J'utilise des ressources

### Titre

- lien
- description

## 🚧 Je franchis les obstacles

### Point de blocage  ✔️

Description: Pas de point de blocage


Résolution :

## 📽️ J'en fais la démonstration

- J'ai ecrit un [tutoriel](...)  ✔️
- J'ai fait une [présentation](...)  ✔️
