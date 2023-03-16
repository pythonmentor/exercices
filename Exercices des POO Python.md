# Exercices de programmation de classes en Python

L'objectif des exercices suivants et de vous entraîner à la création de classes avec le langage de programmation python. Chaque exercice propose de créer plusieurs classes qui vont travailler ensemble à la résolution d'un problème.

Je vous propose de travailler sur chaque classe l'une après l'autre de manière a découper le problèmes en petits morceaux.

Dans un premiers temps, nous n'utilisons pas ces classes mais nous allons très vite créer un petit site web qui pourra les exploiter.


# Exercice 1:

Créez une classe Tache avec les attributs et méthodes suivantes :

**Attributs :**

- titre (str) : Le titre de la tâche
- description (str) : Une brève description de la tâche
- terminee (True/False) : Un booléen indiquant si la tâche est terminée ou non (par défaut : False)

**Méthodes :**

- `__str__(self)` : Retourne une représentation sous forme de texte de la tâche
- terminer_tache(self) : Change l'état de la tâche à "terminée"

Créez une classe Utilisateur avec les attributs et méthodes suivantes :

**Attributs :**

- nom (str) : Le nom de l'utilisateur
- liste_taches (List[Tache]) : Une liste de tâches appartenant à l'utilisateur (par défaut : [])

**Méthodes :**

- ajouter_tache(self, tache: Tache) : Ajoute une nouvelle tâche à la liste de tâches de l'utilisateur
- supprimer_tache(self, index: int) : Supprime une tâche de la liste de tâches de l'utilisateur en fonction de son index
- afficher_taches(self) : Affiche toutes les tâches de l'utilisateur avec leur état (terminée ou non)

Créer un mini programme qui crée un utilisateur et qui peut lui ajouter des tâches

# Exercice 2

Voici un exercice de programmation orientée objet (POO) en Python pour gérer un système de panier, de produits, de commandes et 
d'utilisateurs. Cet exercice comprend quatre classes : Produit, Panier, Commande et Utilisateur.

Créez les classes suivantes avec leurs attributs et méthodes :

## La classe Produit :

**Attributs :**

- id (int) : L'identifiant unique du produit
- nom (str) : Le nom du produit
- prix (float) : Le prix du produit

**Méthodes :**

- `__str__(self)` : Retourne une représentation sous forme de texte du produit

## La classe Panier :

**Attributs :**

- produits (Dict[int, int]) : Un dictionnaire contenant les identifiants des produits et leurs quantités respectives

**Méthodes :**

- ajouter_produit(self, produit: Produit, quantite: int) : Ajoute une quantité d'un produit au panier
- supprimer_produit(self, produit_id: int) : Supprime un produit du panier
- modifier_quantite(self, produit_id: int, nouvelle_quantite: int) : Modifie la quantité d'un produit dans le panier
- vider_panier(self) : Vide le panier de tous les produits
- afficher_panier(self) : Affiche tous les produits et leurs quantités dans le panier

## La classe Commande :

**Attributs :**

- id (int) : L'identifiant unique de la commande
- panier (Panier) : Le panier associé à la commande
- statut (str) : Le statut de la commande (par exemple, "En attente", "Expédiée", "Livrée")

**Méthodes :**

- `__str__(self)` : Retourne une représentation sous forme de texte de la commande
- changer_statut(self, nouveau_statut: str) : Change le statut de la commande

## la classe Utilisateur :

**Attributs :**

- nom (str) : Le nom de l'utilisateur
- commandes (Dict[int, Commande]) : Un dictionnaire contenant les identifiants des commandes et les commandes associées

**Méthodes :**

- passer_commande(self, panier: Panier) : Crée une nouvelle commande à partir d'un panier et l'ajoute aux commandes de l'utilisateur
- afficher_commandes(self) : Affiche toutes les commandes de l'utilisateur avec leur statut


# Exercice 3

Voici exercice pour modéliser un blog. Cet exercice comprend quatre classes : Blog pour représenter le blog lui-même, Article pour représenter un article de blog, Auteur pour représenter un auteur, Commentaire pour représenter un commentaire et Categorie pour représenter une catégorie d'articles.


Créez les classes suivantes avec leurs attributs et méthodes, en travaillant sur une classe à la fois:

## La classe Auteur :

**Attributs :**

- id (int) : L'identifiant unique de l'auteur
- nom (str) : Le nom de l'auteur

**Méthodes :**

- `__str__(self)` : Retourne une représentation sous forme de chaîne de l'auteur

## La classe Categorie :

**Attributs :**

- id (int) : L'identifiant unique de la catégorie
- nom (str) : Le nom de la catégorie

**Méthodes :**

- `__str__(self)` : Retourne une représentation sous forme de chaîne de la catégorie

## La classe Article :

**Attributs :**

- id (int) : L'identifiant unique de l'article
- titre (str) : Le titre de l'article
- contenu (str) : Le contenu de l'article
- auteur (Auteur) : L'auteur de l'article
- categorie (Categorie) : La catégorie de l'article
- commentaires (List[Commentaire]) : Une liste de commentaires associés à l'article

**Méthodes :**

- ajouter_commentaire(self, commentaire: Commentaire) : Ajoute un commentaire à l'article
- `__str__(self)` : Retourne une représentation sous forme de chaîne de l'article

## La classe Commentaire :

**Attributs :**

- id (int) : L'identifiant unique du commentaire
- auteur (str) : Le nom de l'auteur du commentaire
- contenu (str) : Le contenu du commentaire

**Méthodes :**

- `__str__(self)` : Retourne une représentation sous forme de chaîne du commentaire

## La classe Blog :

**Attributs :**

- articles (Dict[int, Article]) : Un dictionnaire contenant les identifiants des articles et les articles associés
- auteurs (Dict[int, Auteur]) : Un dictionnaire contenant les identifiants des auteurs et les auteurs associés
- categories (Dict[int, Categorie]) : Un dictionnaire contenant les identifiants des catégories et les catégories associées
- commentaires (Dict[int, Commentaire]) : Un dictionnaire contenant les identifiants des commentaires et les commentaires associés

**Méthodes :**

- ajouter_article(self, article: Article) : Ajoute un article au blog
- supprimer_article(self, article_id: int) : Supprime un article du blog en fonction de son identifiant
- ajouter_auteur(self, auteur: Auteur) : Ajoute un auteur au blog
- supprimer_auteur(self, auteur_id: int) : Supprime un auteur du blog en fonction de son identifiant
- ajouter_categorie(self, categorie: Categorie) : Ajoute une catégorie au blog
- supprimer_categorie(self, categorie_id: int) : Supprime une catégorie du blog en fonction de son identifiant
- ajouter_commentaire(self, commentaire: Commentaire) : Ajoute un commentaire au blog
- supprimer_commentaire(self, commentaire_id: int) : Supprime un commentaire du blog en fonction de son identifiant
- afficher_tout(self) : Affiche tous les articles, auteurs, catégories et commentaires présents dans le blog
