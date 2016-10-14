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
