# flights-  
# ✈️ Analyse des Réservations de Vols (SQL & Pandas)

> **« Un projet original de Guillaume Saint-Cirgue, extrait du Cahier de Vacances Data & IA 2026. »**

Ce projet pratique met en application des concepts fondamentaux de la gestion de bases de données relationnelles et de la Data Analyse en Python. L'objectif est de manipuler, filtrer et analyser des données de vols, de passagers et de réservations à l'aide de requêtes **SQL** (SQLite3) et de la bibliothèque **Pandas**.

---

## 📊 Structure des Données

La base de données relationnelle en mémoire est composée de trois tables principales :
* **`passengers`** : Informations sur les clients (Nom, prénom, email, nationalité).
* **`flights`** : Détails des vols (Numéro, origine, destination, prix, appareil, capacité).
* **`bookings`** : Suivi des réservations (Passager, vol associé, classe de siège, statut de la réservation).

---

## 🛠️ Fonctionnalités & Exercices Validés

Le projet est découpé en plusieurs étapes d'analyse de données, toutes validées avec succès par des tests unitaires (`assert`) :

1. **Exploration Initiale** : Création du schéma relationnel, application des contraintes (`PRIMARY KEY`, `FOREIGN KEY`, `CHECK`) et insertion des données.
2. **Filtrage Simple** : 
   * Recherche des vols au départ de Nice triés par horaire.
   * Extraction des vols économiques (prix inférieur à 100€).
3. **Agrégations & Business Intelligence** :
   * Analyse des statuts de réservation (confirmées, annulées, en attente).
   * Calcul du chiffre d'affaires total et du volume de réservations par destination.
4. **Segmentation Client** :
   * Zoom sur la clientèle de la destination phare (*New York JFK*).
   * Identification des clients à relancer (réservations en attente).
   * Détection des passagers sans aucune réservation en cours (Jointure Gauche / `LEFT JOIN`).
5. **Analyses Avancées** :
   * Extraction des vols dont le prix est supérieur à la moyenne globale (Sous-requêtes SQL).
   * Identification des clients "ambassadeurs" (ayant effectué plusieurs réservations).

---

## 📈 Recommandation Stratégique (Data Visualisation)

Une analyse graphique du chiffre d'affaires par destination (générée via `matplotlib`) met en évidence les résultats suivants :

* **New York JFK** se positionne largement en tête avec un chiffre d'affaires confirmé de **3 280,00 €** pour 5 réservations.
* **Paris CDG** arrive en deuxième position avec **388,00 €** pour 4 réservations.

**💡 Conclusion :** La recommandation stratégique finale est de **renforcer en priorité la ligne Nice - New York JFK**, car c'est de loin la destination la plus rentable qui bénéficie d'une demande récurrente et forte.

---

## 🚀 Technologies Utilisées

* **Python 3**
* **SQLite3** (Moteur SQL embarqué)
* **Pandas** (Pour la manipulation des données sous forme de DataFrames)
* **Matplotlib** (Pour la visualisation des résultats)
