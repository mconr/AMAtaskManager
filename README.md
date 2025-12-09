
# GProjet – Guide de démarrage complet

## Présentation
GProjet est une application de gestion de projets Agile (Scrum) permettant de suivre les sprints, les tâches, les membres et de générer des rapports PDF détaillés. Elle se compose d’un backend Node.js/Express/PostgreSQL et d’un frontend React/Vite.

## LOGIN
<img width="1920" height="967" alt="image" src="https://github.com/user-attachments/assets/bfcf1c1c-e74f-42d9-b07f-e74be205c9e1" />

## PAGE DES PROJETS
<img width="1920" height="967" alt="image" src="https://github.com/user-attachments/assets/ece22f12-0fff-4e9c-a5e6-633e1bbbc7c5" />

## TABLEAU DES ISSUES
<img width="1920" height="1043" alt="image" src="https://github.com/user-attachments/assets/de986c4f-23d7-408e-9de0-5c9131512cf9" />

## STATS DU PROJET
<img width="1920" height="1043" alt="image" src="https://github.com/user-attachments/assets/5a6cbec8-2a32-422a-af06-41f393f01abc" />

##
<img width="1920" height="1553" alt="image" src="https://github.com/user-attachments/assets/08d26987-5127-4d18-adc1-26424df0c7f7" />

##
<img width="1920" height="1552" alt="image" src="https://github.com/user-attachments/assets/d7176646-93ac-48a5-abf8-b94e57752345" />


## PROFILE
<img width="1920" height="1043" alt="image" src="https://github.com/user-attachments/assets/06dc69a4-167e-43a6-be42-f43beaaee8ea" />


---

## Prérequis
- **Node.js** (v18+ recommandé)
- **npm** (v9+ recommandé)
- **PostgreSQL** (v14+ recommandé)
- **Git**

---

## Installation

### 1. Cloner le projet
```bash
git clone https://github.com/AmineSaif/cdp-project-developpement.git
cd cdp-project-developpement
```

### 2. Backend
```bash
cd backend
npm install
```

#### Configuration de la base de données
- Créez une base PostgreSQL (ex: `gprojet_db`).
- Copiez `.env.example` en `.env` et renseignez :
	```env
	DB_HOST=localhost
	DB_PORT=5432
	DB_USER=postgres
	DB_PASSWORD=VotreMotDePasse
	DB_NAME=gprojet_db
	JWT_SECRET=VotreSecret
	```

#### Démarrage du backend
```bash
npm run dev
```
- Accès API : `http://localhost:5000/api`

### 3. Frontend
```bash
cd ../frontend
npm install
```

#### Configuration du frontend
- Copiez `.env.example` en `.env` et adaptez l’URL de l’API :
	```env
	VITE_API_URL=http://localhost:5000/api
	```

#### Démarrage du frontend
```bash
npm run dev
```
- Accès application : `http://localhost:5173`

---

## Fonctionnalités principales
- **Gestion des projets, sprints, tâches et membres**
- **Tableaux de bord et statistiques**
- **Génération de rapports PDF (projet & sprint)**
- **Authentification JWT**
- **Charts et visualisations (Recharts)**

---

## Structure du projet
```
cdp-project-developpement/
├── backend/
│   ├── controllers/
│   ├── models/
│   ├── routes/
│   ├── app.js
│   └── ...
├── frontend/
│   ├── src/
│   │   ├── pages/
│   │   ├── components/
│   │   └── ...
│   └── ...
└── README.md
```

---

## Installation des dépendances clés

### Backend
- express
- sequelize
- pg
- dotenv
- jsonwebtoken
- cors

### Frontend
- react
- vite
- axios
- jspdf
- jspdf-autotable
- recharts

---

## Lancement rapide
1. Démarrer PostgreSQL et créer la base.
2. Configurer `.env` dans `backend` et `frontend`.
3. Installer les dépendances dans chaque dossier.
4. Lancer le backend puis le frontend.
5. Accéder à l’application via le navigateur.

---

## Génération des rapports PDF
- **Rapport projet** : bouton sur la page statistiques du projet.
- **Rapport sprint** : bouton sur la page du sprint concerné.
- Les rapports incluent toutes les informations pertinentes (métadonnées, membres, tâches, avancement, etc).

---

## Problèmes fréquents
- **Page blanche** : vérifier les exports/imports React.
- **Erreur 404 API** : vérifier la configuration de l’URL dans le frontend et le démarrage du backend.
- **Connexion DB** : vérifier les paramètres dans `.env` et que PostgreSQL est bien lancé.

---

## Contribution
- Forkez le repo, créez une branche, proposez vos modifications via Pull Request.

---

## Auteur
- Monir CHELH & Amine Saif & AMEZIANE Adnane

---

## Licence
MIT
