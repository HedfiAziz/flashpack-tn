<div align="center">
  <img src="static/images/logo.png" alt="Logo FlashPack TN" width="200"/>

  # ⚡ FlashPack TN 
  **Plateforme E-commerce de Packaging Premium & Sur-Mesure**

  [![Python](https://img.shields.io/badge/Python-3.12-blue.svg)](https://www.python.org/)
  [![Flask](https://img.shields.io/badge/Flask-Framework-black.svg?logo=flask)](https://flask.palletsprojects.com/)
  [![PostgreSQL](https://img.shields.io/badge/PostgreSQL-Neon.tech-336791.svg?logo=postgresql&logoColor=white)](https://neon.tech/)
  [![Hosting](https://img.shields.io/badge/Hosting-Oxahost-red.svg)](https://www.oxahost.tn/)
  [![Status](https://img.shields.io/badge/Status-En_Production-brightgreen.svg)]()
</div>

---

## 📝 À propos du projet

**FlashPack TN** est une application web e-commerce complète, moderne et performante développée avec Python (Flask). Elle est spécialement conçue pour la présentation et la vente en ligne de solutions d'emballage sur-mesure (sachets Doypack, emballages personnalisés, etc.).

Le projet a évolué d'un prototype local vers une **infrastructure cloud moderne et sécurisée**, intégrant un design responsive mobile-first premium, une base de données PostgreSQL externalisée, et un déploiement continu sur un serveur de production Oxahost.

---

## 🏗️ Architecture Technique & Infrastructure Cloud

* **Framework Backend :** Python 3.12 avec **Flask** & **SQLAlchemy** (ORM).
* **Base de Données de Production :** **PostgreSQL** hébergé sur **Neon.tech** (Serverless PostgreSQL Cloud) connecté de manière sécurisée via des variables d'environnement (`DATABASE_URL`).
* **Hébergement Web :** **Oxahost** (Environnement cPanel / DirectAdmin avec support Python WSGI).
* **Interface Utilisateur (UI/UX) :** Refonte complète du CSS (`style.css`) axée sur une esthétique "Mobile-First" premium, moderne et fluide.
* **Pipeline de Migration :** Migration réussie à 100 % des données depuis SQLite (`flashpack.db`) vers PostgreSQL Neon avec typage strict (booléens, limites d'entiers et dates).

---

## 🚀 Fonctionnalités Principales

* **Catalogue Dynamique :** Affichage optimisé des produits d'emballage avec filtrage et recherche.
* **Gestion Intelligente des Stocks :** Indicateurs visuels en temps réel (En stock, Rupture, Stock faible) et blocage automatique des achats si le produit est indisponible.
* **Tarification Variable & Dynamique :** Mise à jour instantanée du prix en fonction de la capacité/dimension sélectionnée par le client.
* **Personnalisation & Import de Design :** Possibilité pour les clients d'importer leurs visuels (JPG, PNG, PDF) directement depuis la fiche produit ou de demander une création graphique sur-mesure.
* **Panier & Gestion de Commande :** Tunnel d'achat fluide avec calcul automatique du total HT/TTC.
* **Espace Administrateur Complet :** Dashboard sécurisé pour gérer le catalogue produit, les prix, les dimensions, les stocks et suivre le statut des commandes clients en temps réel.

---

## 🗺️ Navigation & Description des Pages

* 🏠 **Page d'Accueil (`home.html`) :** Vitrine de la marque. Présentation des produits phares, des engagements (qualité, livraison 24/48h) et accès rapide au catalogue.
* 🛍️ **Boutique / Catalogue (`boutique.html`) :** Liste complète des solutions d'emballage avec prévisuels, prix de base et détails rapides.
* 📦 **Fiche Produit (`produit.html`) :** Page détaillée avec galerie d'images, choix des dimensions (calcul de prix dynamique), gestion du stock et module d'upload de fichiers clients.
* 🛒 **Panier (`panier.html`) :** Récapitulatif interactif des articles sélectionnés avec validation de commande.
* ⚙️ **Panel Administrateur (`/admin`) :** Interface sécurisée permettant de créer/modifier/supprimer des produits, de mettre à jour les stocks et d'administrer les commandes clients.

---

## 📂 Structure du Projet

```text
flashpack-tn/
│
├── app.py                  # Application Flask principale, configuration BDD & routes
├── requirements.txt        # Dépendances Python (Flask, psycopg2-binary, Flask-SQLAlchemy, etc.)
├── README.md               # Documentation officielle du projet
├── passenger_wsgi.py       # Point d'entrée WSGI pour l'hébergement Oxahost
│
├── static/                 # Fichiers statiques et médias
│   ├── css/
│   │   └── style.css       # Design responsive premium Mobile-First
│   ├── images/             # Logos, bannières et visuels du site
│   └── uploads/            # Designs importés par les clients et images produits
│
└── templates/              # Modèles HTML (Jinja2)
    ├── base.html           # Layout principal (Header, Navigation, Footer)
    ├── home.html           # Page d'accueil
    ├── boutique.html       # Catalogue complet
    ├── produit.html        # Fiche produit interactive
    ├── panier.html         # Panier et validation de commande
    └── admin/              # Espace d'administration
        └── dashboard.html  # Tableau de bord de gestion
