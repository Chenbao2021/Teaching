# Cours 1 : Introduction à Python et révision des opérations simples

## Objectifs pédagogiques :
1. Découvrir l’environnement Python et les bases de la syntaxe.
2. Apprendre à utiliser les fonctions `print()` et `input()`.
3. Réviser les opérations mathématiques de base : addition, soustraction, multiplication, division.

---

## Plan du cours :

### Partie 1 : Découverte de Python (10 min)

#### Présentation rapide :
- Python est un langage de programmation qui permet de donner des instructions à l’ordinateur.
- Il est utilisé pour créer des jeux, résoudre des problèmes, et bien plus encore !

#### Premiers pas : afficher un message
- Syntaxe de base pour afficher quelque chose :
  ```python
  print("Bonjour tout le monde !")
  ```
- **Pratique :** Demandez aux élèves d’écrire leur premier programme Python qui affiche leur prénom :
  ```python
  print("Je m'appelle [Prénom]")
  ```

---

### Partie 2 : Introduction aux nombres et opérations (15 min)

#### Révision des opérations mathématiques de base
- Python peut effectuer des calculs simples :
  - Addition : `5 + 3`
  - Soustraction : `10 - 7`
  - Multiplication : `4 * 6`
  - Division : `8 / 2`

#### Exemple :
```python
print(5 + 3)  # Affiche 8
print(10 - 7)  # Affiche 3
print(4 * 6)  # Affiche 24
print(8 / 2)  # Affiche 4.0
```

#### Pratique :
- Demandez aux élèves de calculer :
  - `12 + 7`
  - `15 - 4`
  - `3 * 8`
  - `20 / 5`

---

### Partie 3 : Demander une entrée utilisateur avec `input()` (15 min)

#### Pourquoi utiliser `input()` ?
- `input()` permet de rendre le programme interactif en demandant une information à l’utilisateur.

#### Syntaxe de base :
```python
nom = input("Comment t'appelles-tu ? ")
print(f"Bonjour, {nom} !")
```

#### Exemple avec des nombres :
```python
nombre1 = int(input("Entrez un premier nombre : "))
nombre2 = int(input("Entrez un deuxième nombre : "))
somme = nombre1 + nombre2
print(f"La somme de {nombre1} et {nombre2} est {somme}.")
```

#### Pratique :
- Demandez aux élèves de créer un programme qui :
  1. Demande deux nombres.
  2. Affiche leur produit.

---

### Partie 4 : Activité finale (15 min)

#### Objectif :
Créer une calculatrice simple qui peut effectuer différentes opérations mathématiques.

#### Exemple attendu :
```python
print("Bienvenue dans la calculatrice !")
nombre1 = int(input("Entrez le premier nombre : "))
operation = input("Entrez l’opération (+, -, *, /) : ")
nombre2 = int(input("Entrez le deuxième nombre : "))

if operation == "+":
    print(f"Résultat : {nombre1 + nombre2}")
elif operation == "-":
    print(f"Résultat : {nombre1 - nombre2}")
elif operation == "*":
    print(f"Résultat : {nombre1 * nombre2}")
elif operation == "/":
    if nombre2 != 0:
        print(f"Résultat : {nombre1 / nombre2}")
    else:
        print("Division par zéro impossible.")
else:
    print("Opération invalide.")
```

#### Pratique :
- Demandez aux élèves d’ajouter une fonctionnalité pour répéter les calculs jusqu’à ce que l’utilisateur tape "stop".

---

## Résumé et devoir (5 min)

### Résumé :
- Python permet d’afficher des messages avec `print()` et de demander des informations avec `input()`.
- Les opérations mathématiques de base (+, -, *, /) sont faciles à réaliser en Python.

### Devoir :
1. Écrire un programme qui demande :
   - Un nombre entier.
   - Calcule et affiche son carré.

2. **Exemple attendu :**
   ```python
   nombre = int(input("Entrez un nombre : "))
   carre = nombre ** 2
   print(f"Le carré de {nombre} est {carre}.")
   
