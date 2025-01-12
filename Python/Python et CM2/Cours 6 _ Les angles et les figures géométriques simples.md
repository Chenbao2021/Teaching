# Cours 6 : Les angles et les figures géométriques simples

## Objectifs pédagogiques :
1. Comprendre les bases des angles et des figures géométriques.
2. Apprendre à utiliser Python pour dessiner des figures avec des angles spécifiques.
3. Découvrir la bibliothèque `turtle` pour visualiser des concepts géométriques.

---

## Plan du cours :

### Partie 1 : Les types d’angles (10 min)

#### Rappel mathématique :
- **Angles importants :**
  - Angle droit : \( 90^\circ \)
  - Angle aigu : inférieur à \( 90^\circ \)
  - Angle obtus : supérieur à \( 90^\circ \) mais inférieur à \( 180^\circ \)

#### En Python :
- Utilisation de la bibliothèque `math` pour convertir des angles :
  ```python
  import math

  angle_radian = math.radians(90)  # Convertir 90° en radians
  print(f"90 degrés en radians : {angle_radian}")
  ```

#### Pratique guidée :
1. Convertissez les angles suivants en radians : \( 45^\circ \), \( 120^\circ \), \( 270^\circ \).
2. Créez une fonction pour convertir un angle donné en radians.
   ```python
   import math

   def convertir_en_radians(angle_degre):
       return math.radians(angle_degre)

   print(convertir_en_radians(45))
   ```

#### Exercices supplémentaires :
1. Demandez à l’utilisateur de saisir un angle en degrés et affichez sa valeur en radians.
2. Créez un programme qui vérifie si un angle donné est aigu, droit, ou obtus.

---

### Partie 2 : Dessiner des figures simples avec `turtle` (15 min)

#### Introduction à `turtle` :
- `turtle` permet de dessiner des figures géométriques en spécifiant des longueurs et des angles.
- Exemple : Dessiner un triangle équilatéral :
  ```python
  import turtle

  t = turtle.Turtle()
  for _ in range(3):
      t.forward(100)  # Longueur des côtés
      t.left(120)     # Angle entre les côtés

  turtle.done()
  ```

#### Pratique guidée :
1. Dessinez un carré avec `turtle`.
   ```python
   import turtle

   t = turtle.Turtle()
   for _ in range(4):
       t.forward(100)
       t.left(90)

   turtle.done()
   ```
2. Modifiez le programme pour demander à l’utilisateur la longueur des côtés.

#### Exercices supplémentaires :
1. Dessinez un pentagone régulier (5 côtés égaux).
2. Créez une fonction qui dessine un polygone en fonction du nombre de côtés et de leur longueur.
   ```python
   def dessiner_polygone(cotes, longueur):
       import turtle
       t = turtle.Turtle()
       angle = 360 / cotes

       for _ in range(cotes):
           t.forward(longueur)
           t.left(angle)

       turtle.done()
   
   dessiner_polygone(6, 80)  # Exemple pour un hexagone
   ```

---

### Partie 3 : Calcul des angles internes des polygones (10 min)

#### Rappel mathématique :
- La somme des angles internes d’un polygone à \( n \) côtés est donnée par :
  \( (n - 2) \times 180^\circ \).
- Exemple : Pour un pentagone (5 côtés) :
  \( (5 - 2) \times 180 = 540^\circ \).

#### En Python :
```python
def somme_angles(n):
    return (n - 2) * 180

print(somme_angles(5))  # Résultat : 540
```

#### Pratique guidée :
1. Écrivez un programme qui calcule la somme des angles internes d’un polygone donné.
2. Ajoutez une fonctionnalité pour calculer la mesure d’un angle interne si tous les angles sont égaux (polygones réguliers).
   ```python
   def angle_interne(n):
       return somme_angles(n) / n

   print(angle_interne(6))  # Résultat : 120° pour un hexagone régulier
   ```

#### Exercices supplémentaires :
1. Créez un programme interactif qui demande le nombre de côtés d’un polygone et affiche la somme des angles internes et la mesure d’un angle interne.
2. Dessinez le polygone correspondant avec `turtle`.

---

### Partie 4 : Activité finale (15 min)

#### Objectif :
Créer un programme interactif qui :
1. Demande à l’utilisateur de choisir une figure (triangle, carré, polygone).
2. Calcule la somme des angles internes et affiche les résultats.
3. Dessine la figure choisie avec `turtle`.

#### Exemple attendu :
```python
def dessiner_polygone(cotes, longueur):
    import turtle
    t = turtle.Turtle()
    angle = 360 / cotes

    for _ in range(cotes):
        t.forward(longueur)
        t.left(angle)

    turtle.done()

figure = input("Choisissez une figure (triangle/carré/polygone) : ").lower()

if figure == "triangle":
    print("Somme des angles :", somme_angles(3))
    dessiner_polygone(3, 100)
elif figure == "carré":
    print("Somme des angles :", somme_angles(4))
    dessiner_polygone(4, 100)
elif figure == "polygone":
    cotes = int(input("Nombre de côtés : "))
    print("Somme des angles :", somme_angles(cotes))
    dessiner_polygone(cotes, 100)
else:
    print("Figure non reconnue.")
```

---

## Résumé et devoir (5 min)

### Résumé :
- Les angles et les figures géométriques sont des concepts fondamentaux en mathématiques.
- Python, avec `turtle`, permet de visualiser ces concepts et d’effectuer des calculs.

### Devoir :
1. Écrire un programme qui :
   - Calcule la somme des angles internes d’un polygone.
   - Dessine le polygone correspondant avec une couleur choisie par l’utilisateur.

#### Exemple attendu :
```python
def dessiner_polygone(cotes, longueur, couleur):
    import turtle
    t = turtle.Turtle()
    t.fillcolor(couleur)
    t.begin_fill()

    angle = 360 / cotes
    for _ in range(cotes):
        t.forward(longueur)
        t.left(angle)

    t.end_fill()
    turtle.done()

cotes = int(input("Nombre de côtés : "))
longueur = int(input("Longueur des côtés : "))
couleur = input("Couleur du polygone : ")

print("Somme des angles :", somme_angles(cotes))
dessiner_polygone(cotes, longueur, couleur)
