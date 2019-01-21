# Mini-projet final

On approche de la fin de la formation ! L'occasion de faire le point... Je te propose un mini projet qui permettra de récapituler les connaissances acquises depuis le début.

Au programme :
* React
* Modélisation de base de données
* API REST avec Node.js / Express
* Redux

Le thème : un site de e-commerce.

## User Stories

* En tant que visiteur, je veux consulter une liste des produits
* En tant que visiteur, je veux pouvoir filtrer les produits par leur nom
* En tant que visiteur, je veux pouvoir ajouter un produit à mon panier
* En tant que visiteur, je peux créer mon compte et m'y connecter
* En tant que visiteur, je veux éditer les données de mon compte
* En tant que visiteur, je veux pouvoir passer une commande
* En tant que visiteur, je veux consulter l'historique de mes commandes
* En tant qu'administrateur, je veux pouvoir créer/modifier/supprimer un produit
* En tant qu'administrateur, je veux pouvoir consulter la liste de toute les commandes passées

**En option**

* En tant qu'administrateur, je veux pouvoir créer/modifier/supprimer une catégorie de produits
* En tant qu'administrateur, je veux pouvoir attribuer une catégorie à un produit
* En tant qu'administrateur, je veux pouvoir ajouter une photo au produit (au lieu d'une URL en dur)
* En tant que visiteur, je veux pouvoir filtrer les produits par leur catégorie

## Données

Tu auras besoin de 4 tables. **Les relations entre les tables ne sont pas indiquées ici**, cela fait partie de l'exercice que de trouver quelle(s) colonne(s) ajouter à chaque table pour que le tout fonctionne :

* `product` contiendra les champs suivants :

    * `brand` la marque du produit, par ex. "Asus" (`string` sauf si tu tiens **vraiment** à créer une table `brand` pour les marques)
    * `name` le nom du produit, par ex. "Moniteur 24 pouces Full HD XBZ2"
    * `reference`, une référence pour le produit à 6 chiffres, par ex `762874`
    * `slug` le nom du produit "slugifié", concaténation de la marque, du nom, par ex. `asus-moniteur-24-pouces-full-hd-xbz2`
    * `description`, par ex. "Moniteur d'une qualité d'affichage exceptionnelle avec sa résolution de 1920x1080 pixels"
    * `price` le prix du produit
    * `picture` l'URL d'une image

* `order` :

    * `date` la date de la commande (type `DATETIME` en MySQL)

* `order_product` :

    * `quantity` la quantité du produit dans la commande
    * `price` le prix unitaire du produit pour cette commande (le champ `price` de `product` pouvant varier dans le temps)

**En option**

* `category` :

    * `name` le nom de la catégorie, par ex: "Informatique"
    * `slug` le nom "slugifié", par ex : `informatique`

## Structure du projets

Trois répertoires :

* `back`
* `front-public` pour la partie visiteur
* `front-admin` pour la partie admin

N'oublie pas d'utiliser ESLint !!