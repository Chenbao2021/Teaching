# Exercices Scratch (version de Python)

## Exercice 01 : Entrer 5 nombres et afficher somme, max, min

```scratch
1. Créer une liste appelée `nombres`
2. Répéter 5 fois :
   - Demander à l'utilisateur d'entrer un nombre
   - Ajouter ce nombre à la liste `nombres`
3. Initialiser 3 variables : `somme`, `min`, `max` au premier élément de `nombres`
4. Répéter pour chaque `valeur` de `nombres` :
   - Ajouter `valeur` à `somme`
   - Si `valeur > max`, mettre `max = valeur`
   - Si `valeur < min`, mettre `min = valeur`
5. Afficher `somme`, `min`, `max`
```

## Exercice 02 : Inverser une liste de prénoms

```scratch
1. Créer une liste `prenoms` avec 5 prénoms
2. Créer une liste vide `inverse`
3. Répéter de `longueur de prenoms` à 1 :
   - Ajouter `élément i de prenoms` à la liste `inverse`
4. Afficher `inverse`
```

## Exercice 03 : Nombres pairs

```scratch
1. Créer une liste `entiers`
2. Répéter 10 fois :
   - Demander un nombre à l'utilisateur
   - Ajouter ce nombre à la liste `entiers`
3. Créer une liste `pairs`
4. Pour chaque nombre dans `entiers` :
   - Si `nombre mod 2 = 0`, l’ajouter à `pairs`
5. Afficher `pairs`
```

## Exercice 04 : Ajouter un élément à une liste

```scratch
1. Créer une liste `maListe`
2. Créer un bloc personnalisé `ajouter_element`
3. Dans ce bloc :
   - Ajouter l’élément à `maListe`
   - Afficher `maListe`
```

## Exercice 05 : Trouver le maximum

```scratch
1. Créer une liste de nombres `maListe`
2. Créer un bloc `trouver_max`
3. Dans ce bloc :
   - Initialiser une variable `max` avec le premier élément de `maListe`
   - Répéter pour chaque élément :
     - Si élément > `max`, alors `max = élément`
   - Afficher `max`
```

## Exercice 06 : Est présent ?

```scratch
1. Créer une liste `maListe`
2. Créer un bloc `est_present (valeur)`
3. Dans ce bloc :
   - Répéter pour chaque élément :
     - Si élément = valeur, afficher "Vrai", sortir
   - Sinon afficher "Faux"
```

## Exercice 07 : Compter les éléments

```scratch
1. Créer une liste `maListe`
2. Utiliser le bloc `longueur de maListe` pour obtenir le nombre total d’éléments
3. Afficher cette valeur
```

## Exercice 08 : Supprimer les doublons

```scratch
1. Créer une liste `originale`
2. Créer une liste vide `sans_doublons`
3. Pour chaque élément de `originale` :
   - Si l’élément n’est pas dans `sans_doublons`, l’ajouter
4. Afficher `sans_doublons`
```

## Exercice 09 : Éléments communs entre deux listes

```scratch
1. Créer deux listes : `liste1` et `liste2`
2. Créer une liste vide `communs`
3. Pour chaque élément de `liste1` :
   - Si l’élément est dans `liste2` et pas dans `communs`, l’ajouter
4. Afficher `communs`
```

## Exercice 10 : Compter les éléments uniques

```scratch
1. Créer une liste `maListe`
2. Créer une liste vide `uniques`
3. Pour chaque élément de `maListe` :
   - Compter combien de fois il apparaît
   - Si une seule fois, l’ajouter à `uniques`
4. Afficher `longueur de uniques`
```

## Exercice 11 : Réordonner selon un motif

```scratch
1. Créer deux listes : `liste` (éléments) et `motif` (indices)
2. Créer une liste vide `reordonnée`
3. Pour chaque indice `i` dans `motif` :
   - Si `i <= longueur de liste`, alors ajouter `élément i de liste` à `reordonnée`
4. Afficher `reordonnée`
```

