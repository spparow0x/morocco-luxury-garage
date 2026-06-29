<div align="center">

<img src="mlg1-removebg-preview.png" alt="Morocco Luxury Garage" width="200"/>

# MOROCCO LUXURY GARAGE

### La Référence du Prestige Automobile au Maroc

[![GitHub](https://img.shields.io/badge/GitHub-spparow0x-181717?style=for-the-badge&logo=github)](https://github.com/spparow0x)
[![PHP](https://img.shields.io/badge/PHP-8.x-777BB4?style=for-the-badge&logo=php&logoColor=white)](https://www.php.net/)
[![MySQL](https://img.shields.io/badge/MySQL-8.0-4479A1?style=for-the-badge&logo=mysql&logoColor=white)](https://www.mysql.com/)
[![JavaScript](https://img.shields.io/badge/JavaScript-ES6+-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![CSS3](https://img.shields.io/badge/CSS3-Custom-1572B6?style=for-the-badge&logo=css3&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/CSS)
[![License](https://img.shields.io/badge/License-MIT-gold?style=for-the-badge)](LICENSE)

---

**Plateforme digitale premium dédiée à l'importation, la personnalisation et l'entretien de véhicules de prestige au Maroc.**

[🌐 Demo](#demo) · [🚀 Installation](#-installation) · [📖 Documentation](#-architecture-du-projet) · [📬 Contact](#-contact)

</div>

---

## 📸 Aperçu

<div align="center">

| Showroom | Configurateur 3D |
|----------|-----------------|
| Catalogue interactif avec filtrage avancé | Personnalisation visuelle en temps réel |

| Pièces Détachées | Panel Admin |
|-----------------|-------------|
| Catalogue premium avec gestion de stock | Dashboard complet de gestion |

</div>

---

## ✨ Fonctionnalités

### 🏎️ Showroom Virtuel
- Catalogue dynamique de supercars (Lamborghini, Ferrari, Porsche, McLaren, Aston Martin...)
- Filtrage avancé par marque, prix, puissance et disponibilité
- Fiches détaillées avec spécifications techniques complètes
- Système de commande et réservation intégré

### 🎨 Configurateur 3D — Expérience FORMA
- Interface immersive avec effets de particules
- Personnalisation en temps réel : couleurs extérieures, jantes, intérieur, matériaux
- Liaison directe avec le système de commandes spéciales VIP
- Résumé de configuration exportable

### ⚙️ Pièces Détachées Premium
- Catalogue de pièces d'origine avec indicateurs de stock en temps réel
- Recherche avancée par référence, marque et catégorie
- Système de demande de pièces avec suivi de commande
- Fiches produit détaillées

### 👑 Espace Client VIP
- Authentification sécurisée avec JWT
- Tableau de bord personnel avec suivi de toutes les demandes
- Historique des commandes et des maintenances
- Système de récupération de mot de passe par email

### 🔧 Gestion de Maintenance
- Planification de rendez-vous en ligne
- Choix du type de service et du véhicule
- Suivi de l'état des interventions en temps réel

### 🛡️ Panel d'Administration
- Dashboard avec statistiques globales (voitures, pièces, utilisateurs, commandes)
- CRUD complet : voitures, marques, pièces, utilisateurs
- Gestion des commandes spéciales, demandes de pièces et maintenances
- Système de mise à jour des statuts avec historique

---

## 💻 Stack Technique

```
┌─────────────────────────────────────────────────┐
│                   FRONTEND                       │
│  HTML5 · Vanilla JS (ES6+) · Vanilla CSS         │
│  Glassmorphism · Micro-animations · Responsive   │
├─────────────────────────────────────────────────┤
│                   BACKEND                        │
│  PHP 8.x · Architecture MVC from scratch         │
│  API REST JSON · Router personnalisé             │
├─────────────────────────────────────────────────┤
│                  SÉCURITÉ                        │
│  JWT · Bcrypt · PDO Prepared Statements          │
│  Rate Limiting · CORS · Input Validation         │
├─────────────────────────────────────────────────┤
│                BASE DE DONNÉES                   │
│  MySQL · Relations normalisées                   │
│  Tables : users, cars, brands, parts,            │
│  special_orders, maintenance, configurator       │
└─────────────────────────────────────────────────┘
```

---

## 📁 Architecture du Projet

```
morocco-luxury-garage/
│
├── index.html                  # Page d'accueil
├── catalogue.html              # Showroom / Catalogue des voitures
├── product.html                # Fiche détaillée d'une voiture
├── pieces.html                 # Catalogue des pièces détachées
├── piece-detail.html           # Fiche détaillée d'une pièce
├── commande-speciale.html      # Commande spéciale VIP
├── maintenance.html            # Demande de maintenance
├── 31d.html                    # Configurateur 3D (FORMA)
├── admin.html                  # Panel d'administration
├── mon-compte.html             # Espace client
├── forgot-password.html        # Récupération de mot de passe
├── reset-password.html         # Réinitialisation de mot de passe
│
├── main.js                     # Script principal (auth, navigation, UI)
├── Mlg-api.js                  # Gateway API (toutes les requêtes HTTP)
├── cars-data.js                # Données des voitures
├── piecesData.js               # Données des pièces détachées
├── style.css                   # Styles globaux
│
├── database.sql                # Export complet de la base de données
│
└── mlg-backend/                # API Backend PHP
    ├── index.php               # Point d'entrée de l'API
    ├── .htaccess               # Configuration Apache (URL rewriting)
    ├── .env.example            # Variables d'environnement (template)
    ├── setup_database.sql      # Script de création des tables
    │
    ├── config/
    │   ├── app.php             # Configuration générale
    │   └── database.php        # Configuration BDD
    │
    ├── controllers/
    │   ├── AdminController.php         # Endpoints admin (CRUD complet)
    │   ├── AuthController.php          # Authentification (login, register, JWT)
    │   ├── CarsController.php          # API voitures
    │   ├── ClientController.php        # API espace client
    │   ├── MaintenanceController.php   # API maintenance
    │   ├── PartsController.php         # API pièces détachées
    │   ├── ProductController.php       # API fiche produit
    │   └── SpecialOrderController.php  # API commandes spéciales
    │
    ├── core/
    │   ├── Database.php        # Singleton PDO
    │   ├── MailService.php     # Service d'envoi d'emails
    │   ├── Response.php        # Réponses JSON standardisées
    │   └── Validator.php       # Validation des données
    │
    ├── middleware/
    │   ├── Auth.php            # Middleware JWT
    │   ├── Cors.php            # Middleware CORS
    │   └── RateLimiter.php     # Protection anti-bruteforce
    │
    └── routes/
        └── Router.php          # Routeur de l'API
```

---

## 🚀 Installation

### Prérequis
- **[XAMPP](https://www.apachefriends.org/)** (ou WAMP / MAMP) avec PHP 8.x et MySQL
- **Git**

### Étapes

**1. Cloner le projet**
```bash
git clone https://github.com/spparow0x/morocco-luxury-garage.git
cd morocco-luxury-garage
```

**2. Configurer la base de données**
- Démarrez Apache et MySQL depuis XAMPP
- Ouvrez [phpMyAdmin](http://localhost/phpmyadmin)
- Créez une base de données : `morocco_luxury_garage`
- Importez le fichier `database.sql`

**3. Configurer l'environnement**
```bash
cp mlg-backend/.env.example mlg-backend/.env
```
Éditez le fichier `.env` :
```ini
DB_HOST=localhost
DB_NAME=morocco_luxury_garage
DB_USER=root
DB_PASS=
JWT_SECRET=votre_cle_secrete_ici
APP_ENV=development
```

**4. Lancer le projet**
```
http://localhost/morocco-luxury-garage/
```

---

## 🔑 API Endpoints

| Méthode | Endpoint | Description |
|---------|----------|-------------|
| `POST` | `/auth/register` | Inscription |
| `POST` | `/auth/login` | Connexion |
| `GET` | `/cars` | Liste des voitures |
| `GET` | `/cars/:id` | Détails d'une voiture |
| `GET` | `/parts` | Liste des pièces |
| `POST` | `/parts/requests` | Demande de pièce |
| `POST` | `/special-orders` | Commande spéciale |
| `POST` | `/maintenance` | Demande de maintenance |
| `GET` | `/admin/stats` | Statistiques (admin) |
| `GET` | `/admin/cars` | Gestion voitures (admin) |
| `GET` | `/admin/users` | Gestion utilisateurs (admin) |

---

## 🎨 Design

Le design s'appuie sur une identité visuelle luxueuse et immersive :

- **Palette** : Noir profond (`#050505`) et Or (`#c9a84c`)
- **Typographie** : Cormorant Garamond (titres) + Jost (corps)
- **Effets** : Glassmorphism, curseur personnalisé doré, micro-animations
- **Responsive** : Adapté à tous les écrans

---

## 👤 Auteur

<div align="center">

Développé avec 💛 par [**@spparow0x**](https://github.com/spparow0x)

</div>

---

<div align="center">

**⭐ Si ce projet vous plaît, n'hésitez pas à lui donner une étoile !**

</div>
