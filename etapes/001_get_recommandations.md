# Création d'un service pour interagir avec l'API de recommandations

## Objectif

Permettre à travers un service d'interagir avec l'API de recommandation et de
retourner une liste d'ID de tracks.

## Ce qui est attendu

- Une classe `GetRecommandationsTracks` qui prend en paramétres :
  - `genres`, un tableau de genres, limités aux [genres définies par
    Spotify](https://developer.spotify.com/console/get-available-genre-seeds/)
  - `danceability`, un entier entre 0 et 100 qui définie le niveau de
    "dancabilité"
  - `energy`, un entier entre 0 et 100 qui définie le niveau "d'énergie" de la
    playlist

En bonus:

- Un fichier de test qui vérifie:
  - que l'API est bien appelée avec les bons paramètres (que ce soit via la
    librairie `RSpotify` ou à travers un call HTTP classique)
  - que le service renvoie bien une liste d'id de tracks

Étant donné la complexité de mettre en place des tests ici, vous pouvez omettre
cette étape.

## Conseils

- Mettez votre classe dans le dossier `app/services`
- Pour l'authentification via `RSpotify`, créer un initializer dans
  `config/initializers` avec l'initialisation de la librairie
- Pour la gestion des secrets, utilisez soit
  [dotenv](https://github.com/bkeepers/dotenv) soit les [credentials
  rails](https://edgeguides.rubyonrails.org/security.html#environmental-security)
