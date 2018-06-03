# Syntaxte du préfixe des routes

## Direction de la voie

* `w` Un sens
* `W` Dans les deux sens

*Lorsqu'il est omis, il sera utilisé pour n'importe quel type de sens*

## Symmétrie de la voie
*Applicable seulement lorsque la voie est à double sens*

* `s` Symmétrique
* `S` Asymétrique

*Lorsqu'il est omis, il sera utilisé pour n'importe quel type de sens*

## Indicateur d'autoroute

* `h` Seulement pour l'autoroute
* `H` Seulement pour les voies urbaines

*Lorsqu'il est omis, il sera utilisé pour n'importe quel type de voie*

## Sortie de route

* `f` Sortie d'une autoroute vers une route urbaine ou plus petite
* `i` Sortie se terminant sur une autoroute provenant d'une route secondaire 
* `e` Sortie de route/voie en raccordement avec une autre route/voie de même taille

*Lorsqu'il est omis, il sera utilisé pour n'importe quel type de route/voie*

**NOTE:** Ne s'applique qu'aux autoroutes à sens unique (implique également `hw` même s'il est omis ou placé à l'envers).

### ordre de comparaison des tailles de route
* Chemin continu (la priorité à celui qui continu)
* C'est une autoroute (les routes urbaines n'ont pas de priorité)
* Nombre de voies (plus il est élevé, plus il a la priorité)
* Largeur de la voie (plus il est élevé, plus il a la priorité)

## Type de voie
* `G` Voies au niveau du sol
* `B` Voies et ponts élevés
* `T` Tunnels
* `D` Quais (ou barrages)

*Lorsqu'il est omis, il sera utilisé pour n'importe quel type de route/voie*

## Nombre de voies

* `(X,Y)` de X (inclus) à Y (sauf Y). Quand X ou Y est omis, X = 0 et Y = 255.
* `(Z)` exactement Z voies.

*Lorsqu'il est omis, il prendra un nombre quelconque de voies (équivalent à `(,)`)*

## Largeur de voie

* `[X,Y]` de X (inclus) à Y (sauf Y) mètres de large. Quand X ou Y est omis, X = 0 et Y = 999.
* `[Z]` exactement Z mètres de large.

*Lorsqu'il est omis, il prendra n'importe quelle largeur de voie (équivalent à `[,]`)*

## Arguments disponibles pour la nomenclature
Utilisez ces chaînes pour référencer les variables suivantes pour le format:

Id | Description | Depuis la version | Observation
---| ----------- | ------------- | -----------
`{0}` | Nom généré à partir des fichiers noms (par défaut pour les rues et les autoroutes)| 1.0 | -     
`{1}`| Nom de la route de destination | 1.0 | **Implique que l'entrée s'applique uniquement uax voies à sens unique !**
`{2}` | Source du nom de la route  | 1.0 | **Implique que l'entrée s'applique uniquement aux voies à sens unique !**
`{3}` | Voie kilométriqued'origine, en km et en valeur entière  | 1.0 | **Implique que l'entrée s'applique uniquement aux voies à sens unique !**
`{4}` | Km d'origine, en km et avec une décimale  | 1.0 | **Implique que l'entrée s'applique uniquement aux voies à sens unique !**
`{5}` | Source district / ville voisine  | 1.1 | -    
 `{6}` | Quartier ciblé / ville voisine  | 1.1 |  -    
 `{7}` | Direction cardinale de la route (8 directionss) |1.1| **Implique que l'entrée s'applique uniquement aux voies à sens unique !**
