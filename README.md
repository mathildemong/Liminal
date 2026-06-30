
# Liminal

Portfolio personnel développé avec React, présentant mes projets, mon parcours et un moyen de me contacter directement.

## Aperçu

Liminal est une application web one-page construite avec **Create React App**. Elle inclut :

- Une page d'accueil avec un effet machine à écrire (typewriter)
- Une navigation fluide entre les sections (React Router)
- Des transitions animées entre les sections
- Un formulaire de contact fonctionnel envoyant directement un email (sans backend)
- Un design responsive basé sur Bootstrap

## Stack technique

- **React 18** — bibliothèque UI
- **React Router DOM** — navigation
- **React Bootstrap** + **Bootstrap 5** — composants UI et mise en page responsive
- **React Icons** — icônes
- **React Transition Group** — animations de transition
- **Typewriter Effect** — effet de texte animé
- **EmailJS** — envoi d'emails côté client (formulaire de contact)
- **React Helmet Async** — gestion des balises `<head>` (SEO/meta)
- **Web Vitals** — mesure des performances

## Installation

Clone le dépôt puis installe les dépendances :

```bash
git clone https://github.com/mathildemong/Liminal.git
cd Liminal
yarn install
# ou
npm install
```

## Lancer le projet en local

```bash
yarn start
# ou
npm start
```

L'application sera accessible sur [http://localhost:3000](http://localhost:3000).

## Configuration du formulaire de contact

Le formulaire utilise **EmailJS** pour envoyer les messages sans serveur backend. Tu dois créer un fichier `.env` à la racine du projet avec tes propres identifiants EmailJS :

```
REACT_APP_EMAILJS_SERVICE_ID=ton_service_id
REACT_APP_EMAILJS_TEMPLATE_ID=ton_template_id
REACT_APP_EMAILJS_PUBLIC_KEY=ta_public_key
```

> Crée un compte sur [emailjs.com](https://www.emailjs.com/) pour obtenir ces valeurs.

## Build de production

```bash
yarn build
# ou
npm run build
```

Les fichiers optimisés sont générés dans le dossier `build/`.

## Déploiement

Le projet est configuré pour être déployé sur **GitHub Pages** :

```bash
yarn deploy
```

Cette commande build le projet, duplique `index.html` en `404.html` (pour gérer le routing côté client sur GitHub Pages), puis publie le contenu du dossier `build/`.

## Structure du projet

```
Liminal/
├── public/        # fichiers statiques (favicon, index.html, etc.)
├── src/           # code source de l'application React
├── .env           # variables d'environnement (à ne pas committer)
├── package.json
└── README.md
```

## Scripts disponibles

| Commande         | Description                                      |
|------------------|---------------------------------------------------|
| `yarn start`     | Lance l'app en mode développement                  |
| `yarn build`     | Build l'app pour la production                    |
| `yarn test`      | Lance les tests                                    |
| `yarn deploy`    | Build et déploie sur GitHub Pages                  |
| `yarn eject`     | Expose la configuration Webpack (irréversible)     |

## Licence

Voir le fichier [LICENSE](./LICENSE) pour plus de détails.
