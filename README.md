# Software/web development contracts generator in French & English

## Introduction

Ce dépôt est un fork de [tibastral/contrats-francais](https://github.com/tibastral/contrats-francais)

This is a fork of [tibastral/contrats-francais](https://github.com/tibastral/contrats-francais).
The end goal is to generate high-quality, peer-reviewed, customizable contracts.


## Features
Ce fork ne vise pas particulièrement les contrats de type "développement agile", à l'inverse du dépôt d'origine de @tibastral, ni la tarification horaire. De plus, il vise à générer des contrats en langue anglaise ou française, au choix.

This fork doesn't focus on "agile software dev" practices, unlike the original @tibastral repository. Moreover, it aims to generate contracts both in French and English.


## Roadmap

Work in progress.

----

## Usage

**Pour générer un contrat**, vous devez d'abord:

* installer les dépendances ruby/bundler: `bundle`
* définir vos informations personnelles dans `config.json` (`config.sample.json` est dispo en exemple).
* définir la langue souhaitée pour générer les pdf dans `.env`. Attention, seule la traduction en anglais est fournie. PR acceptées !

une fois ceci fait, vous pouvez générer les contrats en faisant `bundle exec foreman run rake`

**To generate a contract**, you must:

* install dependencies: `bundle`
* configure personal information in `config.json` (`config.sample.json` is an example).
* Define language export in `.env`. (see `.env.example`) Beware, only FR & EN languages are available. Pull requests welcome !

You can now generate PDF contracts with `bundle exec foreman run rake`

## License

MIT
