# Langage Javascript

> ✔️ Auto validation par l'étudiant

## 🎓 J'ai compris et je peux expliquer

- les `structures` de base du langage  ✔️
- les normes `ecmascript`  ✔️
- l'utilisation de l'`asynchrone`  ✔️
- les spécifités du mot-clef `this`  ✔️

## 💻 Je code en Javascript

### Un exemple de code commenté  ✔️

```javascript
class PokemonAPI {
    constructor(apiUrl) {
        this.apiUrl = apiUrl;
    }

    async getPokemonById(id) {
        // Utiliser "this.apiUrl" pour faire référence à l'URL de l'API PokeAPI
        const response = await fetch(`${this.apiUrl}/pokemon/${id}`);
        const pokemonData = await response.json();
        return pokemonData;
    }
}

// Créer une instance de la classe PokemonAPI avec l'URL de l'API de la PokeAPI
const pokeAPI = new PokemonAPI('https://pokeapi.co/api/v2');

// Utiliser la méthode getPokemonById pour obtenir les informations d'un pokémon spécifique 
pokeAPI.getPokemonById(1).then(data => console.log(data));
```

### Utilisation dans un projet  ✔️

[[lien github](...)](https://github.com/chambrin/PokeNext)

Description :

### J'ai utilisé ce langage en production  ✔️

[[lien du projet](...)](https://poke-next-topaz.vercel.app/)

Description : pokedex utilisant la pokeapi

### J'ai utilisé ce langage en environement professionnel  ✔️

Description : quotidiennement

## 🌐 J'utilise des ressources

### Titre

- lien
- description

## 🚧 Je franchis les obstacles

### Point de blocage  ✔️

Description:

Plan d'action : (à valider par le formateur)

- action 1  ✔️
- action 2 ✔️
- ...

Résolution :

## 📽️ J'en fais la démonstration

- J'ai ecrit un [tutoriel](...)  ✔️
- J'ai fait une [présentation](...)  ✔️

