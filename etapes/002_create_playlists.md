# Service pour créer une playlist à partir de tracks

## Objectif

Permettre à travers un service de créer une playlist sur Spotify.

## Ce qui est attendu

- Une classe `CreateSpotifyPlaylist` qui prend en paramètres:
  - `tracks`, un tableau de `RSpotify::Track`
  - `name`, une chaîne de caractère qui correspond au nom de la playlist

En bonus:

- Un fichier de test qui vérifie:
  - que l'API est bien appelée avec les bons paramètres
  - que le service renvoie bien un id de playlist

Étant donné la complexité de mettre en place des tests ici (utilisation de stub), vous pouvez omettre
cette étape.

## Conseils

- Vous pouvez utiliser la classe `GetRecommendationsTracks` pour les tracks
