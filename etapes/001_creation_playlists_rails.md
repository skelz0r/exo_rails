# Création de playlists (sans API)

## Objectif

Permettre de créer des playlists en base données en spécifiant des critères. A
ce stade aucune interaction avec Spotify ne doit être implémenté.

## Ce qui est attendu

- Implémentation d'un modèle `Playlist` ayant pour attributs:
  - `name`, une chaîne de caractères
  - `genres`, un tableau de genres, limités aux [genres définies par
    Spotify](https://developer.spotify.com/console/get-available-genre-seeds/)
- `danceability`, un entier entre 0 et 100 qui définie le niveau de
  "dansabilité"
- `energy`, un entier entre 0 et 100 qui définie le niveau "d'énergie" de la
  playlist
- Un controller permettant de créer une playlist:
  - Une action `new` qui rend en vue un formulaire
  - Une action `create` qui créer le modèle `Playlist`
  - Une action `show` qui affiche une playlist

Niveau tests:

- Des validations de base sur les attributs du modèle `Playlist`
- Des tests systèmes sur la création de playlists:
  - Un test qui vérifie qu'avec les bons attributs la playlist se crée et
    affiche la dite playlist
  - Un test qui vérifie qu'avec au moins un attribut non valide que la playlist
    ne se crée pas, et que des erreurs sont affichés

Il ne faut pas, à ce stade, implémenter d'interaction avec Spotify.

## Conseils

- Cette étape permet de mettre en place le squelette de base de l'application:
  le tout utilise les fonctionnalités de base du framework rails, il n'y a pas
  besoin d'installer une quelconque librairie tierce
- Pour les tests systèmes, vous pouvez utiliser, au choix:
  - La stack de tests de Rails: [System
    testing](https://guides.rubyonrails.org/testing.html#system-testing)
  - [Capybara](https://github.com/teamcapybara/capybara)
