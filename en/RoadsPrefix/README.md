# Road prefix syntax

## Track directions

* `w` One-way
* `W` Two-way

*When omitted, it will serve any of the types*

## Symmetry of the pathway
*applicable only when two-way track*

* `s` Symmetric
* `S` Asymetric

*When omitted, it will serve any of the types*

## Highway indicator

* `h` Highway only
* `H` Urban track types only

*When omitted, it will serve any of the types*

## Road exits

* `f` Exit starting out on a highway bound for another route smaller or urban
* `i` Exit ending on a highway originating from a minor highway
* `e` Exit connecting roads of equal size

*When omitted, it will serve any of the types*

**NOTE:** Only applies to one-way highways (implies `hw` also, even if omitted or placed in reverse).

### Route size comparison order
* Continuous path (one that has continuation has priority)
* It is a highway (urban roads have no priority)
* Number of tracks (the higher, the more priority)
* Track width (the higher, the more priority)

## Type of track
* `G` Pathways at ground level
* `B` Elevated paths and bridges
* `T` Tunnels
* `D` Dams

*When omitted, it will serve any of the types*

## Lane count

* `(X,Y)` from X (inclusive) to Y (excluding Y) ranges. When X or Y is omitted, X = 0 and Y = 255.
* `(Z)` exactly Z lanes.

*When omitted, it will serve any number of lanes (equivalent to `(,)`)*

## Track Width

* `[X,Y]` from X (inclusive) to Y (excluding Y) meters wide. When X or Y is omitted, X = 0 and Y = 999.
* `[Z]` exactly Z meters wide.

*When omitted, it will serve any size (equivalent to `[,]`)*

## Highway type (since 3.0)
* `p` Is assigned to a Highway Type register
* `P` Isn't assigned to a Higway Type register


## Arguments available for nomenclature
Use these strings to reference the following variables on the format:

Id | Description | Since version | Observation
---| ----------- | ------------- | -----------
`{0}` | Name generated from name files (default for streets and highways)| 1.0 | -     
`{1}`| Destination road name | 1.0 | **Implies the entry applies only for one-way tracks!**
`{2}` | Source of road name  | 1.0 | **Implies the entry applies only for one-way tracks!**
`{3}` | Mileage track of origin, in kilometers and as integer value  | 1.0 | **Implies the entry applies only for one-way tracks!**
`{4}` | Mileage track of origin, in kilometers and with one decimal place  | 1.0 | **Implies the entry applies only for one-way tracks!**
`{5}` | Source district/neighbor city  | 1.1 | -    
 `{6}` | Target district/neighbor city  | 1.1 |  -    
 `{7}` | Cardinal direction of the road (8 directions) |1.1| **Implies the entry applies only for one-way tracks!**
 `{8}` | Long name of Highway Type  | 3.0 |**Implies `p`**
`{9}` | Forced name of Highway Type  | 3.0 |**Implies `p`**
`{10}`| Short name of Highway Type | 3.0 |**Implies `p`**
