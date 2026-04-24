<div align="center">
  <img src=static/images/logo.png alt="Logo FlashPack TN" width="200"/>

  # ⚡ FlashPack TN 
  **Plateforme E-commerce de Packaging Premium & Sur-Mesure**

  [![Python](https://img.shields.io/badge/Python-3.x-blue.svg)](https://www.python.org/)
  [![Flask](https://img.shields.io/badge/Flask-Framework-black.svg?logo=flask)](https://flask.palletsprojects.com/)
  [![Status](https://img.shields.io/badge/Status-En_développement-orange.svg)]()
</div>

---

## 📝 À propos du projet

**FlashPack TN** est une application web e-commerce développée en Python (Flask) spécialement conçue pour la vente de solutions d'emballage (sachets Doypack, emballages personnalisés, etc.). 

Le projet se distingue par une interface utilisateur premium, une gestion dynamique des prix selon les dimensions, et un système complet permettant aux clients de personnaliser leurs emballages en envoyant leurs propres designs.

---

## 🚀 Fonctionnalités Principales

* **Catalogue Dynamique :** Affichage optimisé des produits avec filtrage.
* **Gestion Intelligente des Stocks :** Indicateurs visuels en temps réel (En stock, Rupture, Stock faible) et blocage automatique des achats si le produit est indisponible.
* **Tarification Variable :** Les prix se mettent à jour instantanément en fonction de la capacité/dimension sélectionnée par le client.
* **Personnalisation (Upload de fichiers) :** Les clients peuvent importer leurs propres designs (JPG, PNG, PDF) directement depuis la fiche produit ou demander une création graphique.
* **Panier & Commande :** Système de panier d'achat fluide.
* **Dashboard Administrateur :** Interface sécurisée pour gérer le catalogue, les stocks et les commandes.

---

## 🗺️ Description des Pages

Le site est structuré pour offrir le meilleur parcours utilisateur possible :

* 🏠 **Page d'Accueil (`home.html`) :** Vitrine de la marque. Présentation des best-sellers, de la proposition de valeur (livraison 24/48h, qualité premium) et appels à l'action vers la boutique.
* 🛍️ **Boutique / Catalogue (`boutique.html`) :** Liste complète de tous les produits d'emballage disponibles, avec leurs images, prix de base et un accès rapide aux fiches techniques.
* 📦 **Fiche Produit (`produit.html`) :** Page détaillée d'un article. Elle affiche la galerie d'images, la description, les spécifications, le sélecteur de dimensions (mettant à jour le prix dynamiquement), l'état du stock et les options d'importation de design client.
* 🛒 **Panier (`panier.html`) :** Récapitulatif des produits sélectionnés, calcul du prix total HT/TTC et validation de la commande.
* ⚙️ **Panel Administrateur :** Zone réservée au propriétaire de la boutique pour ajouter/supprimer des produits, modifier les prix, et mettre à jour les niveaux de stock dans la base de données.

---

## 📂 Structure du Projet

Voici l'architecture complète du projet dès la racine :

```text
flashpack-tn/
│
├── app.py                  # Point d'entrée principal (Configuration Flask et Routes)
├── requirements.txt        # Liste des dépendances (Flask, SQLAlchemy, etc.)
├── README.md               # Documentation du projet
│
├── instance/               # Dossier généré par Flask contenant la DB locale
│   └── flashpack.db        # Base de données SQLite (Produits, Utilisateurs, Commandes)
│
├── static/                 # Ressources statiques (Publiques)
│   ├── css/                
│   │   └── style.css       # Feuilles de style globales et design premium
│   ├── images/             # Images des produits, bannières et logos
│   └── uploads/            # Fichiers de design importés par les clients
│
└── templates/              # Fichiers HTML (Moteur de rendu Jinja2)
    ├── base.html           # Layout principal (Header, Footer, Navigation)
    ├── home.html           # Page d'accueil
    ├── boutique.html       # Page catalogue
    ├── produit.html        # Fiche technique d'un produit (prix dynamique, stock)
    ├── panier.html         # Page du panier d'achat
    └── admin/              # Templates pour le tableau de bord administrateur
        └── dashboard.html
