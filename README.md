```markdown
# 🏋️‍♂️ Gestion des Salles de Sport

## 📘 Contexte

Suite à une expérience décevante dans une grande chaîne de salles de sport – où les inscriptions sont encore gérées à la main – nous avons décidé de proposer une solution numérique pour faciliter la gestion des membres, des séances et des entraîneurs. Ce projet est né d’un besoin réel d’optimisation, avec en bonus : une inscription gratuite de 3 mois offerte par le propriétaire en échange de notre solution.

---

## 🎯 Objectif

Développer un système centralisé pour gérer :
- Les différentes salles de sport
- Les inscriptions des membres
- L’organisation des séances de sport
- L’affectation des entraîneurs

---

## 🧱 Modèle de Données

### 📍 Salle
- `id_salle` (clé primaire)
- `nom`
- `adresse`
- `telephone`

### 👤 Membre
- `id_membre` (clé primaire)
- `nom`
- `prenom`
- `adresse`
- `date_naissance`
- `sexe`
- `id_salle` (clé étrangère)

### 🧑‍🏫 Entraîneur
- `id_entraineur` (clé primaire)
- `nom`
- `prenom`
- `age`
- `specialite`

### 🗓️ Séance
- `id_seance` (clé primaire)
- `type_sport`
- `horaire`
- `id_salle` (clé étrangère)

### 📅 Participation
> Relation entre Membre et Séance (max 20 participants par séance)
- `id_membre` (clé étrangère)
- `id_seance` (clé étrangère)

### 🧑‍🤝‍🧑 Animation
> Relation entre Entraîneur et Séance (max 2 entraîneurs par séance)
- `id_entraineur` (clé étrangère)
- `id_seance` (clé étrangère)

---

## 🛠️ Technologies suggérées

| Élément | Outils possibles |
|--------|------------------|
| Base de données | PostgreSQL / MySQL / SQLite |
| Backend (API) | Node.js / Python Flask / Django |
| Frontend (interface web) | React / Next.js / Vue |
| Authentification | JWT / OAuth / Auth0 |
| Hébergement | Vercel, Render, Railway, Heroku, etc. |

---

## 🚀 Fonctionnalités clés (MVP)

- [x] Gestion des salles
- [x] Enregistrement des membres
- [x] Création et planification des séances
- [x] Affectation des entraîneurs
- [x] Inscription des membres aux séances
- [x] Respect des limites (20 membres / 2 entraîneurs par séance)

---

## 📌 Contraintes

- Un membre ne peut participer qu’aux séances de sa salle d’inscription.
- Une séance ne peut accueillir que **20 membres max**.
- Une séance ne peut être animée que par **2 entraîneurs max**.

---

## ✅ Résultat attendu

Un système efficace, intuitif et scalable permettant :
- Une meilleure gestion des ressources humaines (entraîneurs)
- Une gestion optimisée du planning des séances
- Une réduction des erreurs humaines liées à l’inscription manuelle

---

## 💡 Auteur

Projet réalisé par AMARA GBOKO, dans le cadre d’un checkpoint de formation à gomycode.

```

---
