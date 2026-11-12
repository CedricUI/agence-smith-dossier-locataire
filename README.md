# Agence SMITH — Espace candidat

Code de l’espace candidat livré le 12 novembre 2026. HTML, CSS et JavaScript sans framework ni dépendance à installer. Les styles sont dans public/index.html.

## Déployer sur Vercel via GitHub

1. Décompressez l’archive.
2. Créez un dépôt GitHub et ajoutez le CONTENU du dossier agence-smith-vercel : public/, vercel.json et ce README.
3. Dans Vercel, créez un projet et importez ce dépôt.
4. Réglages : Framework Preset = Other ; Root Directory = dossier contenant vercel.json ; Build Command = vide ; Output Directory = public. Aucune variable d’environnement nécessaire.
5. Lancez Deploy. Le fichier vercel.json contient déjà les réglages de compilation et de sortie.

Documentation : https://vercel.com/docs/builds
Configuration : https://vercel.com/docs/project-configuration/vercel-json

## Tester localement

Depuis le dossier du projet, avec Python 3 installé :

    python3 -m http.server 8000 --directory public

Ouvrez http://localhost:8000.

## Fonctionnement

- Création de compte et connexion email/mot de passe SIMULÉES. Aucun contrôle d’identité, aucun mot de passe sauvegardé.
- Le bouton Google est une simulation : aucun OAuth Google.
- La liste de préparation et la référence saisie sont enregistrées dans le localStorage du navigateur. Il s’agit d’un profil de démonstration unique par navigateur, pas de comptes utilisateurs distincts.
- Le bouton de dépôt ouvre https://tally.so/r/8NaJbr. L’intégration Tally → Make → Airtable reste gérée dans ces services ; elle n’est pas contenue dans ce code.
- Le statut Airtable n’est pas consulté depuis ce site. Les cases cochées ne constituent pas un dépôt de documents.
- Le fichier n’embarque aucune clé API ni accès à Airtable.
- La connexion ChatGPT protégeant l’ancienne publication n’est pas incluse : les restrictions d’accès de la nouvelle publication dépendent des paramètres Vercel.
- Montserrat est chargée via Google Fonts, avec Arial en repli.

## Modifier

- public/index.html : contenus, charte graphique et lien Tally (élément tallyLink).
- public/app.js : connexion simulée, liste de préparation, sauvegarde locale.
- vercel.json : configuration d’hébergement.

Cette archive concerne l’espace candidat, pas l’interface d’administration Airtable ni le scénario Make. Utilisez uniquement des données fictives.
