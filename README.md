# 🧮 Exemples d'utilisation de Fedoo pour la simulation numérique en mécanique

Ce projet s’inscrit dans le cadre d’un **cours de simulation numérique**, et présente trois exemples concrets d’utilisation de la bibliothèque **[Fedoo](https://fedoo.dev)** pour la mécanique des milieux continus.

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

📄 **Fichier :** `Fedoo___conditions_aux_limites.ipynb`

Ce premier notebook étudie une plaque carrée soumise à une traction verticale, dans deux cas :

1. Encastrement en bas (`dx = 0`)
2. Blocage uniquement vertical (`dx` libre)

- Observer l’effet de la contrainte de déplacement horizontal sur la réponse mécanique.
- Analyser les champs de déplacement (`Disp_XX`, `Disp_YY`), contraintes (`Stress_XX`, `Stress_YY`) et déformations (`Strain_XX`, `Strain_YY`).
- Comprendre l’effet de **Poisson** et l’impact des conditions aux limites sur la redistribution des efforts.

---

## Exemple 2 : Poutre en I 3D – Flexion verticale

📄 **Fichier :** `Fedoo_I_shape_beam_bending.ipynb`

Ce second exemple montre comment modéliser une **poutre en I 3D** soumise à une charge verticale à son centre.

- Création d’un maillage structuré 2D en forme de I, extrudé en 3D.
- Passage à des éléments de type **wedge (15 nœuds)**.
- Définition d’un matériau **élastique isotrope**.
- Application de conditions aux limites reproduisant une flexion :
  - Encastrement partiel à la base.
  - Chargement vertical en haut au centre.

---
## Exemple 3 : Compaction hydrostatique d'une sphère

📄 **Fichier :** `Fedoo_3Dsphere.ipynb`

Ce notebook présente la simulation de la **compaction isotrope** d’une sphère en 3D. Il s'agit d'un cas d'étude classique en mécanique non seulement pour valider le comportement élastique sous contraintes hydrostatiques, mais aussi pour visualiser l'évolution du déplacement radial dans une géométrie sphérique.

- Chargement d’un maillage volumique sphérique (format `.msh`, généré par Gmsh).
- Extraction automatique de la surface pour identifier les **nœuds de bord**.
- Application d’un **déplacement radial vers le centre** sur tous les nœuds de la surface, simulant une **compression hydrostatique** (isotrope).
- Définition d’un matériau **élastique isotrope linéaire** (type acier).
- Résolution du problème par la méthode des éléments finis avec Fedoo.


---

## Technologies utilisées

- **Fedoo** : bibliothèque Python de simulation par éléments finis  
- **Numpy** : calcul numérique  
- **Pyvista** : visualisation 3D interactive

---

## Installation

### Dépendances nécessaires
(*installées via un environnement Miniconda*) :

```bash
pip install fedoo numpy pyvista

---
## Conclusion

Ce projet présente plusieurs exemples de simulations numériques, notamment dans le contexte de l’ingénierie des procédés, utilisant la plateforme Fedoo, un environnement collaboratif pour la modélisation et la simulation. Ces exemples démontrent la capacité des simulations à reproduire numériquement des phénomènes physiques complexes (écoulement, échange thermique, etc.).

Les simulations numériques s’intègrent de manière stratégique dans l’industrie digitale pour plusieurs raisons :

- Elles permettent de prédire et optimiser le comportement de systèmes industriels avant tout prototypage réel.
- Elles favorisent une réduction des coûts et des temps de développement.
- Elles facilitent l’intégration de l’intelligence artificielle via l’analyse de grandes quantités de données simulées (ex. : calibration de modèles, apprentissage de comportements complexes).
- Les environnements comme Fedoo illustrent l’évolution vers des outils collaboratifs, modulaires et accessibles, essentiels dans une démarche Industrie 4.0.

Les avancées récentes en simulations numériques combinent puissance de calcul, interface utilisateur simplifiée, et reproductibilité scientifique. Des outils comme Fedoo illustrent bien cette tendance : ils rendent la simulation plus accessible, modulaire, et efficace. En s'appuyant sur des formats ouverts, des bibliothèques Python et une logique de configuration plutôt que de codage systématique, ces outils permettent de mieux explorer, comprendre et communiquer les phénomènes complexes. En somme, la simulation numérique devient non seulement un pilier de la recherche scientifique moderne, mais aussi un levier pédagogique essentiel pour apprendre à modéliser le réel.



