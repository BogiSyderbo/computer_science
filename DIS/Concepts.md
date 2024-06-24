## Relational database

Cardinality: number of rows

Degree: number of columns


# E/R Model

## Entity

*Objects* with *attributes*

## Entity set

A collection of similar entities.

All entities in a set have the same set of attributes

Each entity has a *key*

Each attribute has a *domain*
## Relationship
Association among two or more entities

Relationships can have roles
## Relationship set
Collection of similar relationship

An $n$-ary relationship set $R$ relates $n$ entity sets $E_1, \ldots, E_n$

Each relationship in $R$ involves entities $e_1$ in $e_1,\ldots,e_n$ in $E_n$


## Notation
![[Drawing 2024-05-02 13.49.21.excalidraw]]



# Relational Calculus


## RC-Eval Computer Shop
```
∃ model_1, model_2, hd_2. 
PC(model_1, _, _, hd_1, _) ∧ PC(model_2, _, _, hd_2, _) ∧ (¬ model_1 = model_2) ∧ (hd_1 = hd_2)
```

There are two different computer models (`model_1` and `model_2`) that have the same hard drive size (`hd_1 = hd_2`).


```
minimum_price <- MIN p; maker, type Product(maker, model, type) ∧
(PC(model, _, _, _, p) ∨ Laptop(model, _, _, _, _, p) ∨ Printer(model, _, _, p))
```
the `minimum_price` as the minimum price among all products (PCs, Laptops, or Printers) that have a `maker`, a `model`, and a `type`.


∃ maker. Laptop(_, _, _, _, 15, _)

	