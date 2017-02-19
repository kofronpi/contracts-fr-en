# Contrat de maintenance

Le développeur, {{ company.name }} assurera un service de maintenance d'une (1) application web de type Ruby on Rails hébergée sur Heroku au Client, {{ client.name }}, et ce à partir du 1er octobre 2016.

Cette prestation permet d'assurer la fiabilité et le bon fonctionnement du site web sous Rails. Les services de contrôle (monitoring) et de tests automatiques permettent d'être proactif et de détecter les éventuels problèmes dès qu'ils surviennent, afin d'éviter au maximum de perdre des leads et clients potentiels.

## 1. Services

Le développeur fournira les services suivant au Client dans le cadre du présent contrat de maintenance :

+ Mises à jour de sécurité applicative critiques (Ruby, Rails, librairies) déployées en moins de 48 heures
+ Mises à jour applicatives hebdomadaires (Ruby, Rails)
+ Contrôle de l'uptime (temps de bon fonctionnement) de l'application web abonnements.origo.energy en continu
+ Test automatique quotidien du formulaire d'abonnement
+ Gestion sur Heroku (backups de la base de données, historique des logs pour audit, gestion des add-ons et configuration) - inclut des charges supplémentaires directement facturées au Client via Heroku, paiement à mettre en place par le Client
+ Système de ticket pour des bugs éventuels qui pourraient être détectés par le Client - n'inclut pas le développement de nouvelles fonctionnalités qui rentre dans le cadre du contrat de prestation séparé
+ Conseil technique et technologique
+ Jusqu'à 4 heures par mois incluses dans le contrat de maintenance, toute heure supplémentaire de maintenance sera facturée au tarif horaire habituel du Développeur ( {{ company.hourly_rate }} de l'heure).
Les heures non utilisées sont consommées à améliorer la structure de l'application existante- exemple : tests unitaires et intégration continue, optimisation, correction de bugs.

Tout développement de nouvelle fonctionnalité doit se faire via un contrat de prestation séparé avec des conditions générales de vente spécifiques.

## 2. Responsabilité et délais

Le Développeur ne pourra être tenu responsable de délais dans le temps d'accès en bonne conditions à l'application web imputés à des dysfonctionnements chez les prestataires et services qui hébergent le serveur de l'application (par exemple Heroku a un uptime de 99,9% en moyenne en Europe).

Pendant toute la durée de ce contrat de maintenance, le Client accepte que le Développeur soit le seul fournisseur de service de maintenance de l'application. Si une partie tierce autre que le Développeur effectue des changements sur la base de données / l'application ou le serveur hébergeant cette application, le Développeur ne saurait être tenu responsable des effets de ces changements. Toute erreur crée devra être réparée par le Développeur dans les conditions énoncées dans la partie 1.

Le Développeur s'engage à répondre dans les 48 heures ouvrées par email (hors week-end). Ce package de maintenance n'inclut PAS une hotline téléphonique.

Les requêtes et tickets reçus après 18:00 GMT+2 seront traités le jour ouvré suivant.

## 3. Paiement et engagement

Le Client accepte de payer {{ company.name }} un total de 300 € HT par mois pour le package de maintenance décrit ci-dessus. Le paiement doit avoir lieu la première semaine de chaque mois.

Comme précisé dans la loi Française, des pénalités de retard de paiement s'appliqueront au taux annuel de refinancement de la BCE majoré de 10 points, plus une compensation de 40 euros pour les frais de recouvrement.

Le Client s'engage pour une durée minimale de trois mois. Toute interruption du contrat doit être notifiée au Développeur au moins un mois à l'avance. Tout mois de maintenance entamé est dû en totalité.

## 4. Force majeure et faute du Client

Le Développeur n’engagera pas sa responsabilité en cas de force majeure ou de faute du Client, telles que définies ci-après :

Sera considéré comme un cas de force majeure opposable au Client tout empêchement, limitation ou dérangement du fait d’incendie, d’épidémie, de pandémie, d’explosion, de tremblement de terre, de catastrophes industrielles et nucléaires, de défaillance des réseaux de transmission, d’effondrement des installations, d’utilisation illicite ou frauduleuse des mots de passe, codes ou références fournis au Client, de piratage informatique et faille de sécurité imputable à l’hébergeur du Livrable ou à une 0-day (faille non révélée à ce jour et donc non corrigeable via ce pack de maitenance), d’inondation, de panne d’électricité, de guerre, d'attentats terroristes, d’embargo, de loi, d’injonction, de demande ou d’exigence de tout gouvernement, de perquisition, de réquisition, de grève, de boycott, ou autres circonstances hors du contrôle raisonnable du Développeur.

Sera considérée comme une faute du Client opposable à ce dernier toute mauvaise utilisation du Livrable, faute, négligence, omission ou défaillance de sa part ou de celle de ses préposés, non-respect des conseils donnés par le Développeur.

## 5. Permissions

Le Client donnera au Développeur tous les accès et droits nécessaires pour effectuer le travail décrit ci-dessus (exemple : Heroku, GitLab).

## 6. Loi applicable et jurisdiction

Ce présent contrat de maintenance est soumis à la loi Française.

En cas de litige juridique, la compétence exclusive est attribuée aux tribunaux de Lyon, même pour les procédures d’urgence ou conservatoire en référé ou par requête, nonobstant pluralité de défendeurs ou appel en garantie.

## Signatures

En cochant les cases suivantes, le Client reconnaît qu'il a lu et approuvé :

[        ] Les conditions de ce contrat de maintenance par {{ company.name }}

EN TÉMOIGNAGE DE QUOI, les Parties ont approuvé ce contrat de maintenance, prenant effet à partir du 1er octobre 2016.

Le Client

_{{ client.name }}_

Par:


Titre:


Signature:


<br/>
<br/>
<br/>
Le Développeur

{{ company.name }}

Signature :


