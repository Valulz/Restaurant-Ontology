RDF


Menu





Plat:
nom
nom_anglais
prix
  en fct° qté


Menu
  Entrée + Plat     ->  (ref Entree + ref Plat)
  Plat + Dessert    ->  (ref Plat + ref Dessert)
  Entree + Plat + Dessert  -> (ref Entree + ref Plat + ref Dessert)
  Petit Roi -> (ref Plat (Précis) + Dessert)


Dessert
  Fromages

Entrée

Plat (Menu) (Viande | Poissons + Accompagnement)
  Poissons
  Viandes

  Accompagnement ?
    frites
    Puree
    Legumes  Salade

Meal - Repas


Plat (Mangeable)
  - id_plat

Lang
  - nom
  - ref plat

prix
  - cout
  - qté (@nullable = 1)
  - ref_plat

Menu
  - id_menu
  - nom

Menu_Plat
  - ref_menu
  - ref_plat

Ingredient
  - id_ing
  - nom
  - qté_stock (?)

Ing_Plat
  - ref_ing
  - ref_plat

Meal
  type
