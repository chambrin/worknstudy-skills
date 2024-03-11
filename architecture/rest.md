# REST API

> ✔️ Auto validation par l'étudiant

## 🎓 J'ai compris et je peux expliquer

- les verbes HTTP  ✔️
- les statuts HTTP ✔️
- les endpoints  ✔️
- CORS  ✔️
- la nomenclature recommandée pour les routes  ✔️

## 💻 J'utilise

### Un exemple personnel commenté  ✔️
```javascript
// Déclaration d'une fonction asynchrone nommée GET qui attend une requête entrante (request) et un objet de réponse (res).
            export async function GET(request: Request, res: Response) {
// Dans cette fonction, nous définissons l'objet 'data' qui représente un utilisateur dans cette implémentation.
                const data = {"id": 1, "name": "Aur\u00e9lie Delaunay du Pr\u00e9vost", "email": "elisabethlombard@example.com", "username": "richardpereira", "job": "assistant de gestion en PME", "gender": "Femme", "phone_number": "+33 (0)3 65 76 33 39", "website": "http://perrot.fr/", "address": "703, rue de Barre, 61122 Martel", "birthdate": "1978-04-23", "age": 45, "interests": ["Cin\u00e9ma", "Photo"], "user_image_url": "/random_avatar/user_1.png", "background_image_url": "https://source.unsplash.com/random/1920x1080"};
// Retournons une nouvelle réponse avec un corps qui est une version de 'data' convertie en JSON.
// Nous spécifions aussi un code de statut de 200 pour indiquer que la requête a été traitée avec succès.
                return new Response(JSON.stringify(data), {
                    status: 200,
                    headers: {
                        'Access-Control-Allow-Origin': '*',
                        'Access-Control-Allow-Methods': 'GET, POST, PUT, DELETE, OPTIONS',
                        'Content-Type': 'application/json',
                        'Access-Control-Allow-Headers': 'Content-Type, Authorization',
                    },
                });
            }
```
### Utilisation dans un projet  ✔️

https://github.com/chambrin/random-user-generator-api

Description :

### Utilisation en production si applicable ✔️

site : https://random-user-generator-api-delta.vercel.app/

exemple de lien api : https://random-user-generator-api-delta.vercel.app/api/user/1

Description : Un projet qui crée des liens API de faux utilisateurs, pour faciliter le développement.

### Utilisation en environement professionnel  ✔️

Description : Création de diverses API REST pour rendre les informations de base de données disponibles via une API REST.

## 🌐 J'utilise des ressources

- Pas de ressource spécifique.

## 🚧 Je franchis les obstacles

### Point de blocage  ✔️

Description: Pas de blocage

Plan d'action : (à valider par le formateur)


Résolution :

## 📽️ J'en fais la démonstration

- J'ai ecrit un [tutoriel](...)  ✔️
- J'ai fait une [présentation](...) ✔️
