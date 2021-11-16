# Intégration de RSpotify pour la création effective de la playlist sur Spotify

## Objectif

Lors de la création d'une playlist en base de données, générer une playlist en
fonction des critères du modèle, sur Spotify.

## Ce qui est attendu

- La playlist générée sur Spotify devra comporter 20 chansons
- La playlist générée sur Spotify aura le nom attribué au modèle `Playlist`
  (attribut `name`)
- Les chansons seront récupérées à travers le endpoint [Get Recommendations Based on
  Seeds](https://developer.spotify.com/documentation/web-api/reference/#/operations/get-recommendations)), en utilisant la librairie [RSpotify](https://github.com/guilhermesad/rspotify)
- Le modèle `Playlist` doit stocker l'identifiant de la playlist Spotify (dans
  un champ que l'on peut nommer `spotify_id`)
- La vue de la playlist doit contenir un lien vers la playlist sur Spotify

Concernant les tests, il faudra:

- Vérifier que la librairie `RSpotify` a bien été appelée
- Pour éviter que dans les tests systèmes des playlists se crée à chaque fois
  que vous faites tourner les tests, il va falloir "mocker" les appels à
  `RSpotify`

## Conseils

- Pour la génération de la playlist sur Spotify, il faudrait vérifier que le
  modèle `Playlist` est valide avant de tenter une génération
- Afin de pouvoir tester en isolation et rendre le code clair, le mieux est
  d'encapsuler toute la génération de la playlist dans une classe à part

## Ressources

- [RSpotify](https://github.com/guilhermesad/rspotify)
- Pour les tests, quelques tutorials:
  - [Test Doubles: in theory, in Minitest and in
    RSpec](https://ieftimov.com/post/test-doubles-theory-minitest-rspec/)
