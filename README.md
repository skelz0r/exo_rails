# Générateur de playlists

## Objectif

L'objectif de ce projet est de créer une webapp permettant de générer des
playlists à l'aide de l'API de Spotify, plus particulièrement le endpoint de
génération de playlists basé sur des seeds : [Get Recommendations Based on
Seeds](https://developer.spotify.com/documentation/web-api/reference/#/operations/get-recommendations)

Ce dépot a pour objectif de guider pas à pas au développement de cette
application. Les fonctionnalités qui seront implémentées dans la version finale
seont:

- Un espace membre où l'inscription et la connexion se feront à l'aide d'un
  spotify connect
- Création de playlists basés sur des paramètres divers et variés tel que le
  genre de musiques, le niveau d'énergie, de popularité etc etc..
- Persistance des playlists sur Spotify et sur l'application, avec
  synchronisation sur les mises à jour / suppressions
- Partage des playlists

## Introduction

### Pré-requis

Avoir un minimum de connaissance en Rails: avoir fait un gros tutorial
d'introduction, un bootcamp du type THP/Le Wagon.

Maîtriser un minima les tests est un plus.

### Ce qui sera utilisé

Assurez-vous d'avoir installé sur votre système :

- Ruby >= 2.7
- Ruby on Rails 6
- PostgreSQL >= 11
- Redis

En terme de librairies dans le projet Rails :

- Une librairie de test unitaires
- Pour interagir avec Spotify: [RSpotify](https://github.com/guilhermesad/rspotify)

## Procédure à chaque étape

1. Créer une nouvelle branche `features/etape-N` avec N le numéro de l'étape
1. Effectuer les modifications pour répondre aux spécifications de l'étape
1. Créer une pull request et demander une review

Chaque étape sera accompagnée de tests unitaires, sauf indication contraire.

## Guidelines générales

Vous avez quelques guidelines disponibles ici: [Guidelines générales pour le
développement](./docs/guidelines_generales.md)

## Démarrage

### Initialisation du projet

```sh
gem install rails -v '~> 6.0'
rails new spotify_generator
cd spotify_generator/
```

N'oubliez pas de modifier le README pour y mettre toutes les informations
nécessaires concernant l'installation du projet.

### Les étapes

1. [Création d'un service pour interagir avec l'API de
   recommendations](./etapes/001_get_recommendations.md)
