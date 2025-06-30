# 🧮 Exemples d'utilisation de Fedoo pour la simulation numérique en mécanique

Ce projet s’inscrit dans le cadre d’un **cours de simulation numérique**, et présente deux exemples concrets d’utilisation de la bibliothèque **[Fedoo](https://fedoo.dev)** pour la mécanique des milieux continus.

> 💡 **Basé sur le dépôt original** : [https://github.com/3MAH/fedoo](https://github.com/3MAH/fedoo)  
> Merci aux auteurs pour leur travail pédagogique et la mise à disposition d'exemples accessibles.

---

## Objectif

Ces exemples pédagogiques montrent comment :

- Créer des maillages **2D** et **3D**.
- Définir des lois de comportement **élastique**.
- Appliquer des **conditions aux limites**.
- Résoudre des problèmes statiques linéaires en **contrainte plane** ou en **3D**.
- Visualiser les champs de **déplacement**, de **contrainte** et de **déformation**.

---

## Exemple 1 : Traction 2D – Influence des conditions aux limites

📄 **Fichier :** `traction_conditions_limites.ipynb`

Ce premier notebook étudie une plaque carrée soumise à une traction verticale, dans deux cas :

1. Encastrement en bas (`dx = 0`)
2. Blocage uniquement vertical (`dx` libre)

- Observer l’effet de la contrainte de déplacement horizontal sur la réponse mécanique.
- Analyser les champs de déplacement (`Disp_XX`, `Disp_YY`), contraintes (`Stress_XX`, `Stress_YY`) et déformations (`Strain_XX`, `Strain_YY`).
- Comprendre l’effet de **Poisson** et l’impact des conditions aux limites sur la redistribution des efforts.

---

## Exemple 2 : Poutre en I 3D – Flexion verticale

📄 **Fichier :** `poutre_I_flexion.ipynb`

Ce second exemple montre comment modéliser une **poutre en I 3D** soumise à une charge verticale à son centre.

- Création d’un maillage structuré 2D en forme de I, extrudé en 3D.
- Passage à des éléments de type **wedge (15 nœuds)**.
- Définition d’un matériau **élastique isotrope**.
- Application de conditions aux limites reproduisant une flexion :
  - Encastrement partiel à la base.
  - Chargement vertical en haut au centre.

---

## Technologies utilisées

- **Fedoo** : bibliothèque Python de simulation par éléments finis  
- **Numpy** : calcul numérique  
- **Pyvista** : visualisation 3D interactive

---

## Installation

### Dépendances nécessaires
(*installées via un environnement Miniconda ou pip standard*) :

```bash
pip install fedoo numpy pyvista
