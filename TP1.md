# Exercice 1

Objectif de l'ontologie
------------
Pour formaliser les différents concepts de la gestion d'un restaurant.

Scénario d'utilisation
-------------
Proposer aux clients des cartes, en fonction de leurs langues, de l'heure(midi, soir)/date(repas d'été =/= repas d'hiver, journée spéciale ...),
Proposer au gérant de gérer les coûts du restaurant.
Proposer au gérant la gestion des stocks des ingrédients.
Proposer aux cuisiniers la liste des ingrédients pour un repas.
Les controlleurs peuvent s'assurer de la bonne gestion des stock(Date de consommation, Outils en règles, ...), des normes de sécurités.

Quelques quetions à répondre
-----------------------
Gérant : Puis-je avoir les coûts de productions des frites ?
Gérant : Combien de Coca-Cola avons-nous en stock ?

Clients : Ce restaurant propose-t'il des boissons gazeuse sans sucre ?
Clients : Quels sont les repas végétariens de ce restaurants ?

Cuisiners : Quels sont les ingrédients nécessaire à la réalisation d'un boeuf bourguignon ?

Controlleurs : Les ingrédients en stock sont-ils encore "mangeable" ?
Controlleurs : Les cuisiniers suivent-ils les normes de sécurité ?

Utilisateurs potentiels
---------------------
- Les clients d'un restaurant
- Cuisiniers (preparation des repas)
- Gérant du restaurant (toute la partie gestion, coût)
- Controlleurs : gestion partie sécurité

Périmètre de l'ontologie
----------------------
- Terme courant (Localisation : pas le latin)
- La recette d'un repas

Ne gère pas :
- La gestion du personnel du restaurant.
- Les serveurs du restaurants.

Niveau de formalisation et granularité visé
---------------------
Cuisiniers : Termes techniques et spécifique à la cuisine (épices : cumin, ..)
Clients : terme plus général (un plat non salé, ...)
Gérant :  Termes plus techniques et spécifique à la gestion des coûts.
Controlleur : Terme plu spécifique à la sécurité et la gestion des stocks



Principaux termes et concepts
------------------
Localisation
Etablissement
Ingrédient
Cout
Carte
Repas
Client
Date
Quantité
Boisson
Cuisinier

----------------------
Edit 14/10

Nous appellons Consommable, toute entitée consommable du restaurant (Boisons, plat, entrée et dessert).

Nous considérons le prix comme un Concept à part entière.

Prix représente :
- Prix d'un Consommable
- Prix d'un ingrédient (il peut être intéressant d'avoir une date pour pouvoir comparé l'évolution des prix)
- Prix d'un menu
- Quantité ?
  Certains Consommables (Huîtres Normandes) ont un Qté/Prix (6/11€; 9/15€).
  Nullable = 1 ?
  Nous pouvons imaginé un prix de gros sur les ingrédients





Prix possède aussi une monnaie précise  (Euro, dollar, ...). Un ingrédient pourrait être acheté dans une monnaie différente
de la monnaie locale.


Menu :
- Nom (Langue ?)
- Ensemble de consommable spécifique (comme un plat particulier : une purée, un steak ...) ou général (une boisson quelconque ).
  - Référence à un plat spécifique + référence à un type de consommable.
- Prix
- Age Restricted ? (-12 ans) : Nullable
- Durée (nullable)

Commandable ?
- Menu
- Consommable
  - Boisson
    - Chaude
    - Froide
    - Vin ?
  - Mangeable (is_vegetarien)
    - Accompagnement (?)
    - Plat
    - Entrée
    - Dessert

Les Allergènes ??????

Commande ?
- Date
- Ensemble de Commandable
- Prix (redondant ? calculable avec l'ensemble des commandes).

Restaurant
- Nom (Pas de traduction du nom du restaurant)

-------------------
J'ai regarder des menus d'autres restaurants, que celui présenté en TP2, histoire d'avoir une meilleur idée de ce qui était attendu
en terme d'ontologie.

Commandable ?
- Menu
- Consommable
  - Boisson
    - Chaude
    - Froide
    - Vin ?
    - Apéritif ?
  - Mangeable (is_vegetarien)
  - Entrée
    - Plat
    - Accompagnement (?)
    - Dessert


Approvisionnement
Fournisseur ?
Ingrédient
Prix

----------------
J'ai relu l'entête du TP1
Il nous ai demandé "à terme la réalisation d'une application de gestion de la carte, des prises de commandes et de l'approvisionnement"

Il ne nous est pas demandé de gérer la préparation des plats.

Stock:
- à la base je n'y voyais pas d'intérêt, il nous suffisait d'avoir les ingrédient, avec leur quantité en stock.
Mais, après mûr réflexion, je me demande s'il ne serait pas mieux d'avoir un stock.
Ingrédient 
