# Cours 4 : La géométrie simple

## Objectifs pédagogiques :
1. Apprendre à utiliser Python pour effectuer des calculs géométriques.
2. Calculer les périmètres et les aires des figures simples.
3. Visualiser des figures géométriques à l’aide de la bibliothèque `turtle`.

---

## Plan du cours :

### Partie 1 : Calcul du périmètre (10 min)

#### Rappel mathématique :
- **Périmètre :** La somme des longueurs de tous les côtés d’une figure.
- Formules importantes :
  - Rectangle : \( P = 2 \times (L + l) \)
  - Carré : \( P = 4 \times c \)

#### En Python :
Exemple pour le rectangle :
```python
longueur = float(input("Entrez la longueur du rectangle : "))
largeur = float(input("Entrez la largeur du rectangle : "))
perimetre = 2 * (longueur + largeur)
print(f"Le périmètre du rectangle est {perimetre}.")
```

#### Pratique guidée :
1. Calculez le périmètre d’un carré à partir de la longueur d’un côté.
2. Écrivez un programme qui demande les dimensions d’un rectangle et affiche son périmètre.

#### Exercices supplémentaires :
1. Modifiez le programme pour accepter des valeurs en mètres et les convertir en centimètres avant le calcul.
2. Demandez à l’utilisateur de choisir entre un carré et un rectangle, puis calculez le périmètre en conséquence.

---

### Partie 2 : Calcul de l’aire (15 min)

#### Rappel mathématique :
- **Aire :** La surface occupée par une figure.
- Formules importantes :
  - Rectangle : \( A = L \times l \)
  - Carré : \( A = c^2 \)
  - Triangle : \( A = \frac{b \times h}{2} \)

#### En Python :
Exemple pour le triangle :
```python
base = float(input("Entrez la base du triangle : "))
hauteur = float(input("Entrez la hauteur du triangle : "))
aire = (base * hauteur) / 2
print(f"L’aire du triangle est {aire}.")
```

#### Pratique guidée :
1. Écrivez un programme pour calculer l’aire d’un carré donné la longueur d’un côté.
2. Calculez l’aire d’un rectangle avec des valeurs saisies par l’utilisateur.

#### Exercices supplémentaires :
1. Ajoutez une vérification pour que les dimensions saisies soient positives.
2. Modifiez le programme pour permettre à l’utilisateur de calculer l’aire de plusieurs figures dans une même exécution.

---

### Partie 3 : Visualisation avec `turtle` (15 min)

#### Introduction à `turtle` :
- `turtle` est une bibliothèque Python permettant de dessiner des formes géométriques.
- Exemple simple : Dessiner un carré :
  ```python
  import turtle

  t = turtle.Turtle()
  for _ in range(4):
      t.forward(100)  # Avance de 100 unités
      t.right(90)  # Tourne à droite de 90 degrés

  turtle.done()
  ```

#### Pratique guidée :
1. Dessinez un rectangle avec `turtle`.
2. Modifiez le programme pour demander les dimensions du rectangle à l’utilisateur.

#### Exercices supplémentaires :
1. Dessinez un triangle équilatéral avec `turtle`.
2. Ajoutez des couleurs aux figures (par exemple, remplissez un carré en rouge).
   ```python
   t.fillcolor("red")
   t.begin_fill()
   for _ in range(4):
       t.forward(100)
       t.right(90)
   t.end_fill()
   ```

---

### Partie 4 : Activité finale (15 min)

#### Objectif :
Créer un programme interactif qui :
1. Demande à l’utilisateur de choisir une figure (rectangle, carré, triangle).
2. Calcule et affiche son périmètre et son aire.
3. Dessine la figure avec `turtle`.

#### Exemple attendu :
```python
import turtle

def dessiner_rectangle(longueur, largeur):
    t = turtle.Turtle()
    for _ in range(2):
        t.forward(longueur)
        t.right(90)
        t.forward(largeur)
        t.right(90)
    turtle.done()

figure = input("Choisissez une figure (rectangle/carré/triangle) : ").lower()

if figure == "rectangle":
    longueur = float(input("Entrez la longueur : "))
    largeur = float(input("Entrez la largeur : "))
    print(f"Périmètre : {2 * (longueur + largeur)}")
    print(f"Aire : {longueur * largeur}")
    dessiner_rectangle(longueur, largeur)

elif figure == "carré":
    cote = float(input("Entrez la longueur du côté : "))
    print(f"Périmètre : {4 * cote}")
    print(f"Aire : {cote ** 2}")

elif figure == "triangle":
    base = float(input("Entrez la base : "))
    hauteur = float(input("Entrez la hauteur : "))
    print(f"Aire : {(base * hauteur) / 2}")
else:
    print("Figure non reconnue.")
```

---

## Résumé et devoir (5 min)

### Résumé :
- Le périmètre et l’aire sont des concepts fondamentaux en géométrie.
- Python facilite les calculs géométriques et permet de visualiser des figures avec `turtle`.

### Devoir :
1. Écrire un programme qui :
   - Demande à l’utilisateur les dimensions d’un rectangle.
   - Calcule et affiche son périmètre et son aire.
   - Dessine le rectangle avec `turtle`.

#### Exemple attendu :
```python
import turtle

longueur = float(input("Entrez la longueur du rectangle : "))
largeur = float(input("Entrez la largeur du rectangle : "))

print(f"Périmètre : {2 * (longueur + largeur)}")
print(f"Aire : {longueur * largeur}")

# Dessin avec turtle
t = turtle.Turtle()
for _ in range(2):
    t.forward(longueur)
    t.right(90)
    t.forward(largeur)
    t.right(90)

turtle.done()
