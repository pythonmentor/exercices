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


