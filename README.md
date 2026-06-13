# FoodSaver AI – Assistant anti-gaspillage alimentaire

Building AI course project – Éléments d’IA

## Summary

FoodSaver AI aide les particuliers à réduire le gaspillage alimentaire en proposant des recettes personnalisées à partir des aliments qu’ils ont déjà chez eux. L’utilisateur saisit les produits proches de leur date de péremption, et l’IA suggère des repas simples et rapides.

## Background

Le gaspillage alimentaire est un problème majeur : un tiers de la production mondiale est perdue. En France, chaque personne jette en moyenne 30 kg de nourriture par an, dont une partie encore consommable.

- Problème : on ne sait pas toujours quoi cuisiner avec les restes ou les aliments qui vont bientôt expirer.
- Fréquence : très courant, surtout dans les familles actives.
- Motivation personnelle : réduire mon propre gaspillage et faire des économies.
- Importance : moins de déchets = moins d’émissions de CO₂ et plus d’argent dans le porte‑monnaie.

## How it is used

L’application se présente comme un chat simple ou une page web.

1. L’utilisateur liste les aliments qu’il a (ex : « 2 tomates, 1 oignon, 200g de riz »).
2. L’IA recherche des recettes compatibles.
3. L’utilisateur reçoit 3 suggestions avec temps de préparation et niveau de difficulté.

Exemple d’utilisation : le mercredi soir, avant d’aller faire les courses, on vérifie ce qu’il reste et on cuisine avec.

![anti-gaspi illustration](https://upload.wikimedia.org/wikipedia/commons/thumb/8/8d/Food_loss_and_waste_FAO_2011.jpg/800px-Food_loss_and_waste_FAO_2011.jpg)

## Data sources and AI methods

**Sources de données :**
- API publique de recettes (ex : Spoonacular, Edamam)
- Données personnelles saisies par l’utilisateur (aliments disponibles)

**Méthodes IA utilisées :**
- Traitement du langage naturel (NLP) pour comprendre les aliments saisis en français courant.
- Correspondance par mots‑clés + pondération (TF‑IDF) entre les ingrédients saisis et les bases de recettes.
- Système de recommandation simple (basé sur la popularité ou le temps de cuisson).

## Challenges

Ce que le projet **ne résout pas** :
- Ne gère pas les allergies complexes (sauf si l’utilisateur les précise).
- Nécessite une base de recettes pré‑existante (ne génère pas de recettes “inventées”).
- Ne lit pas automatiquement les dates de péremption (saisie manuelle).

Limites éthiques : l’application ne doit pas encourager à consommer des aliments clairement avariés. Un avertissement “si l’aspect ou l’odeur est anormal, ne pas consommer” sera affiché.

## What next?

Pour faire grandir le projet :
- Ajouter un scan d’étiquette par photo (reconnaissance d’images).
- Synchronisation avec un frigo connecté.
- Mode “surprise” : l’IA choisit une recette parmi les ingrédients disponibles.
- Version communautaire : les utilisateurs partagent leurs propres recettes anti‑gaspi.

Compétences nécessaires : Python (Flask/Django pour le web), apprentissage automatique (scikit‑learn), un peu d’API.

## Acknowledgments

- Inspiration : Too Good To Go, l’application “Frigo vide” (idée similaire).
- Image FAO / Wikimedia Commons : [Food loss and waste](https://commons.wikimedia.org/wiki/File:Food_loss_and_waste_FAO_2011.jpg) (licence CC BY‑SA 3.0).
- API Edamam (exemple de source de recettes).
