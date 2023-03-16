# Exercice 1:

Créez une classe Tache avec les attributs et méthodes suivantes :

Attributs :

- titre (str) : Le titre de la tâche
- description (str) : Une brève description de la tâche
- terminee (True/False) : Un booléen indiquant si la tâche est terminée ou non (par défaut : False)

Méthodes :

- `__str__(self)` : Retourne une représentation sous forme de texte de la tâche
- terminer_tache(self) : Change l'état de la tâche à "terminée"

Créez une classe Utilisateur avec les attributs et méthodes suivantes :

Attributs :

- nom (str) : Le nom de l'utilisateur
- liste_taches (List[Tache]) : Une liste de tâches appartenant à l'utilisateur (par défaut : [])

Méthodes :

- ajouter_tache(self, tache: Tache) : Ajoute une nouvelle tâche à la liste de tâches de l'utilisateur
- supprimer_tache(self, index: int) : Supprime une tâche de la liste de tâches de l'utilisateur en fonction de son index
- afficher_taches(self) : Affiche toutes les tâches de l'utilisateur avec leur état (terminée ou non)

