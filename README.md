# Software/web development & consulting contracts generator in French & English

## Introduction

Ce dépôt est un fork de [tibastral/contrats-francais](https://github.com/tibastral/contrats-francais).

This is a fork of [tibastral/contrats-francais](https://github.com/tibastral/contrats-francais).
The end goal is to generate high-quality, peer-reviewed, customizable contracts.

# Requirements

Ruby >= 2.2.0
Last tested with Ruby 2.4.0

## Features
Ce fork ne vise pas particulièrement les contrats de type "développement agile", à l'inverse du dépôt d'origine de @tibastral, et propose plus de modes de tarifications (horaire, au projet...) De plus, il vise à générer des contrats en langue anglaise ou française, au choix.
De plus il permet de générer des contrats orientés développement produit ou orientés conseil/consulting.

This fork doesn't focus on "agile software dev" practices, unlike the original @tibastral repository. Moreover, it aims to generate contracts both in French and English.
Moreover, it allows to generate dev-oriented contracts or consulting contracts.

## Roadmap / wishlist

- Consulting contract in english. Right now it is the same as dev mode.
- Better API.
- Better way to manage particular conditions of contract for each contract generated, allow to keep history of contracts locally.
- Validation of modifications by a lawyer.
- Make it a gem ?

## Usage

**Pour générer un contrat**, vous devez d'abord:

* installer les dépendances ruby/bundler: `bundle`
* définir vos informations personnelles dans `config.json` (`config.sample.json` est dispo en exemple).
* définir les conditions particulières de contrat dans `src/fr/dev/pcc.md` ou `src/fr/consulting/pcc.md`

Une fois ceci fait, vous pouvez générer les contrats en exécutant `rake locale=fr` .

Dans le cas d'un contrat orienté consulting, vous devez exécuter `rake locale=fr mode=consulting`

**To generate a contract**, you must:

* install dependencies: `bundle`
* configure personal information in `config.json` (`config.sample.json` is an example).
* write particular conditions of contract in `src/en/dev/pcc.md` or `src/en/consulting/pcc.md`

* Define language export in `.env`. (see `.env.example`) Beware, only FR & EN languages are available.

You can now generate PDF contracts with `rake locale=en`
You can also generate consulting contracts with `rake locale=en mode=consulting`

## Contribute

Pull requests bienvenues !
Pull request welcome !

## License

MIT
