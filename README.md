<div align="center">

<img src="mlg1-removebg-preview.png" alt="Morocco Luxury Garage" width="200"/>

# MOROCCO LUXURY GARAGE

### The Ultimate Luxury Automotive Platform in Morocco

[![GitHub](https://img.shields.io/badge/GitHub-spparow0x-181717?style=for-the-badge&logo=github)](https://github.com/spparow0x)
[![PHP](https://img.shields.io/badge/PHP-8.x-777BB4?style=for-the-badge&logo=php&logoColor=white)](https://www.php.net/)
[![MySQL](https://img.shields.io/badge/MySQL-8.0-4479A1?style=for-the-badge&logo=mysql&logoColor=white)](https://www.mysql.com/)
[![JavaScript](https://img.shields.io/badge/JavaScript-ES6+-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![CSS3](https://img.shields.io/badge/CSS3-Custom-1572B6?style=for-the-badge&logo=css3&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/CSS)
[![License](https://img.shields.io/badge/License-MIT-gold?style=for-the-badge)](LICENSE)

---

**A premium digital platform for importing, customizing, and maintaining luxury & exotic vehicles in Morocco.**

[🌐 Demo](#demo) · [🚀 Installation](#-installation) · [📖 Documentation](#-project-architecture) · [📬 Contact](#-author)

</div>

---

## ✨ Features

### 🏎️ Virtual Showroom
- Dynamic supercar catalog (Lamborghini, Ferrari, Porsche, McLaren, Aston Martin...)
- Advanced filtering by brand, price, horsepower, and availability
- Detailed spec sheets with full technical specifications
- Built-in ordering and reservation system

### 🎨 3D Configurator — FORMA Experience
- Immersive interface with particle effects
- Real-time customization: exterior colors, wheels, interior, materials
- Direct integration with VIP special order system
- Exportable configuration summary

### ⚙️ Premium Spare Parts
- OEM parts catalog with real-time stock indicators
- Advanced search by reference, brand, and category
- Parts request system with order tracking
- Detailed product pages

### 👑 VIP Client Portal
- Secure authentication with JWT
- Personal dashboard with full request tracking
- Order and maintenance history
- Email-based password recovery system

### 🔧 Maintenance Management
- Online appointment scheduling
- Service type and vehicle selection
- Real-time intervention status tracking

### 🛡️ Admin Panel
- Dashboard with global statistics (cars, parts, users, orders)
- Full CRUD: cars, brands, parts, users
- Special order, parts request, and maintenance management
- Status update system with history

---

## 💻 Tech Stack

```
┌─────────────────────────────────────────────────┐
│                   FRONTEND                       │
│  HTML5 · Vanilla JS (ES6+) · Vanilla CSS         │
│  Glassmorphism · Micro-animations · Responsive   │
├─────────────────────────────────────────────────┤
│                   BACKEND                        │
│  PHP 8.x · MVC Architecture from scratch         │
│  REST JSON API · Custom Router                   │
├─────────────────────────────────────────────────┤
│                  SECURITY                        │
│  JWT · Bcrypt · PDO Prepared Statements          │
│  Rate Limiting · CORS · Input Validation         │
├─────────────────────────────────────────────────┤
│                  DATABASE                        │
│  MySQL · Normalized Relations                    │
│  Tables: users, cars, brands, parts,             │
│  special_orders, maintenance, configurator       │
└─────────────────────────────────────────────────┘
```

---

## 📁 Project Architecture

```
morocco-luxury-garage/
│
├── index.html                  # Landing page
├── catalogue.html              # Showroom / Car catalog
├── product.html                # Car detail page
├── pieces.html                 # Spare parts catalog
├── piece-detail.html           # Part detail page
├── commande-speciale.html      # VIP special order
├── maintenance.html            # Maintenance request
├── 31d.html                    # 3D Configurator (FORMA)
├── admin.html                  # Admin panel
├── mon-compte.html             # Client dashboard
├── forgot-password.html        # Password recovery
├── reset-password.html         # Password reset
│
├── main.js                     # Main script (auth, navigation, UI)
├── Mlg-api.js                  # API gateway (all HTTP requests)
├── cars-data.js                # Cars dataset
├── piecesData.js               # Spare parts dataset
├── style.css                   # Global styles
│
├── database.sql                # Full database export
│
└── mlg-backend/                # PHP Backend API
    ├── index.php               # API entry point
    ├── .htaccess               # Apache config (URL rewriting)
    ├── .env.example            # Environment variables (template)
    ├── setup_database.sql      # Table creation script
    │
    ├── config/
    │   ├── app.php             # App configuration
    │   └── database.php        # Database configuration
    │
    ├── controllers/
    │   ├── AdminController.php         # Admin endpoints (full CRUD)
    │   ├── AuthController.php          # Authentication (login, register, JWT)
    │   ├── CarsController.php          # Cars API
    │   ├── ClientController.php        # Client portal API
    │   ├── MaintenanceController.php   # Maintenance API
    │   ├── PartsController.php         # Spare parts API
    │   ├── ProductController.php       # Product page API
    │   └── SpecialOrderController.php  # Special orders API
    │
    ├── core/
    │   ├── Database.php        # PDO Singleton
    │   ├── MailService.php     # Email service
    │   ├── Response.php        # Standardized JSON responses
    │   └── Validator.php       # Data validation
    │
    ├── middleware/
    │   ├── Auth.php            # JWT Middleware
    │   ├── Cors.php            # CORS Middleware
    │   └── RateLimiter.php     # Anti-bruteforce protection
    │
    └── routes/
        └── Router.php          # API Router
```

---

## 🚀 Installation

### Prerequisites
- **[XAMPP](https://www.apachefriends.org/)** (or WAMP / MAMP) with PHP 8.x and MySQL
- **Git**

### Steps

**1. Clone the repository**
```bash
git clone https://github.com/spparow0x/morocco-luxury-garage.git
cd morocco-luxury-garage
```

**2. Set up the database**
- Start Apache and MySQL from XAMPP
- Open [phpMyAdmin](http://localhost/phpmyadmin)
- Create a new database: `morocco_luxury_garage`
- Import the `database.sql` file

**3. Configure environment**
```bash
cp mlg-backend/.env.example mlg-backend/.env
```
Edit the `.env` file:
```ini
DB_HOST=localhost
DB_NAME=morocco_luxury_garage
DB_USER=root
DB_PASS=
JWT_SECRET=your_secret_key_here
APP_ENV=development
```

**4. Launch the project**
```
http://localhost/morocco-luxury-garage/
```

---

## 🔑 API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| `POST` | `/auth/register` | User registration |
| `POST` | `/auth/login` | User login |
| `GET` | `/cars` | List all cars |
| `GET` | `/cars/:id` | Car details |
| `GET` | `/parts` | List all parts |
| `POST` | `/parts/requests` | Request a part |
| `POST` | `/special-orders` | Place a special order |
| `POST` | `/maintenance` | Request maintenance |
| `GET` | `/admin/stats` | Dashboard stats (admin) |
| `GET` | `/admin/cars` | Manage cars (admin) |
| `GET` | `/admin/users` | Manage users (admin) |

---

## 🎨 Design Philosophy

The design is built around a luxurious and immersive visual identity:

- **Palette**: Deep Black (`#050505`) & Gold (`#c9a84c`)
- **Typography**: Cormorant Garamond (headings) + Jost (body)
- **Effects**: Glassmorphism, custom golden cursor, micro-animations
- **Responsive**: Fully adapted to all screen sizes

---

## 👤 Author

<div align="center">

Built with 💛 by [**@spparow0x**](https://github.com/spparow0x)

</div>

---

<div align="center">

**⭐ If you like this project, don't forget to give it a star!**

</div>
