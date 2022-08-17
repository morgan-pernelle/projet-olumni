# O'lumni

## O'lumni front-end

### Présentation du projet

O’lumni est un réseau social, le partage entre Alumni O’clock est une force.
Partager autour du dev ! Poser des question, créer un tuto, donner et démontrer des ressources, partager ses expériences. Faire vivre la communauté au delà du cadre de la formation, attention la bienveillance et le respect de chacun reste le mot d’ordre !

### Problématique

Manque de persistance sur les posts / informations délivré(e)s à la communauté des alumni. Près de 4 000 personnes sont sur le slack pro et peu sont actifs, sans doute pour éviter le flood notamment.

Les informations postées sur le slack pro disparaissent au bout de 30 jours. C’est dommage car les nouveaux alumni n’auront pas accès aux réponses antérieures que ce soit sur les problématiques rencontrées sur différents sujets comme : TP, recherche d’emploi, aide sur blocage code etc.

## O'lumni back-end

### Présentation du projet

O’lumni est un réseau social, le partage entre Alumni O’clock est une force.
Partager autour du dev ! Poser des question, créer un tuto, donner et démontrer des ressources, partager ses expériences.
Faire vivre la communauté au delà du cadre de la formation, attention la bienveillance et le respect de chacun reste le mot d’ordre !

[Lien du notion](https://vaulted-lute-aed.notion.site/Cahier-Des-Charges-54fcc6d50c4047269f96bf364123f296)

### Installation du projet

Installation des composants :

- `composer install`

Création et configuration du `.env.local` en prenant le `.env` en exemple

Création des clé SSL pour les token JWT :

- `bin/console lexik:jwt:generate-keypair`

Création de la BDD :

- `bin/console doctrine:database:create`

Lancement des migrations :

- `bin/console doctrine:migrations:migrate`

Installation des fausses données :

- `bin/console doctrine:fixtures:load -n --group=dev`

Installation des données pour la mise en prod :

- `bin/console doctrine:fixtures:load -n --group=prod`

Lancement du serveur PHP :

- `php -S 0.0.0.0:8000 -t public`
