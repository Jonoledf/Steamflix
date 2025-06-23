# SteamFlix - Site de Streaming

Une plateforme de streaming de films avec panel d'administration.

## Technologies utilisées

- Frontend: React, Tailwind CSS
- Backend: Node.js, Express, MongoDB
- Authentication: JWT

## Fonctionnalités

- 🎬 Catalogue de films avec recherche et filtrage
- 👤 Authentification utilisateur
- 🔐 Panel d'administration pour gérer les films
- 🎨 Interface moderne et responsive

## Installation

1. Cloner le projet
```bash
git clone <repository-url>
cd steamflix
```

2. Installer les dépendances
```bash
# Installation des dépendances frontend
cd client
npm install

# Installation des dépendances backend
cd ../server
npm install
```

3. Configuration

- Créer un fichier `.env` dans le dossier `server` avec les variables suivantes :
```env
PORT=5000
MONGODB_URI=mongodb://localhost:27017/steamflix
JWT_SECRET=votre_secret_jwt_super_securise
```

4. Démarrer MongoDB
```bash
# Assurez-vous que MongoDB est installé et en cours d'exécution sur votre machine
```

## Démarrage

1. Démarrer le backend
```bash
cd server
npm run dev
```

2. Démarrer le frontend (dans un nouveau terminal)
```bash
cd client
npm start
```

L'application sera accessible à l'adresse : http://localhost:3000

## Identifiants de test

- Email: admin@steamflix.com
- Mot de passe: admin123

## Structure du projet

```
steamflix/
├── client/                # Frontend React
│   ├── src/
│   │   ├── components/   # Composants réutilisables
│   │   ├── pages/       # Pages de l'application
│   │   └── services/    # Services API
│   └── ...
└── server/               # Backend Node.js
    ├── models/          # Modèles MongoDB
    ├── routes/          # Routes API
    ├── middleware/      # Middleware (auth, etc.)
    └── ...
```

## API Endpoints

### Auth
- POST /api/auth/register - Inscription
- POST /api/auth/login - Connexion
- GET /api/auth/me - Obtenir l'utilisateur courant

### Movies
- GET /api/movies - Liste des films
- GET /api/movies/featured - Films en vedette
- GET /api/movies/:id - Détails d'un film
- POST /api/movies - Ajouter un film (admin)
- PUT /api/movies/:id - Modifier un film (admin)
- DELETE /api/movies/:id - Supprimer un film (admin)
