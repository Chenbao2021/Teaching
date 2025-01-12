# Cours 3 : Les fractions et les divisions

## Objectifs pédagogiques :
1. Apprendre à manipuler des fractions et des divisions en Python.
2. Comprendre les concepts de simplification et d’équivalence des fractions.
3. Relier les fractions et les divisions décimales en Python.

---

## Plan du cours :

### Partie 1 : Révision des divisions (10 min)

#### Notion mathématique :
- La division consiste à partager une quantité en parties égales.
- Exemple :
  - \( 10 \div 2 = 5 \)
  - \( 10 \div 4 = 2,5 \)

#### En Python :
- Division simple :
  ```python
  print(10 / 2)  # Résultat : 5.0
  print(10 / 4)  # Résultat : 2.5
  ```
- Division entière (quotient uniquement) :
  ```python
  print(10 // 3)  # Résultat : 3
  ```
- Reste de la division (modulo) :
  ```python
  print(10 % 3)  # Résultat : 1
  ```

#### Pratique :
- Demandez aux élèves de calculer :
  - \( 15 \div 4 \)
  - \( 25 \div 7 \)
  - Quotient et reste pour \( 37 \div 6 \).

#### Exercices supplémentaires :
1. Écrire un programme qui demande deux nombres et affiche leur quotient entier et leur reste.
2. Modifiez le programme pour vérifier si un nombre est divisible par un autre.

---

### Partie 2 : Travailler avec des fractions (15 min)

#### Introduction aux fractions :
- Une fraction représente une partie d’un tout, par exemple :
  - \( \frac{1}{2} \) (un demi).
  - \( \frac{3}{4} \) (trois quarts).

#### Simplification des fractions :
- Une fraction est simplifiée lorsque le numérateur et le dénominateur n’ont plus de diviseur commun.
- Exemple :
  - \( \frac{6}{9} = \frac{2}{3} \)

#### Exemple en Python :
Utilisation de la bibliothèque `fractions` :
```python
from fractions import Fraction

f = Fraction(6, 9)
print(f)  # Résultat : 2/3
```

#### Pratique guidée :
- Demandez aux élèves :
  - De simplifier les fractions \( \frac{15}{20} \), \( \frac{24}{36} \), et \( \frac{50}{100} \).
  - D’écrire un programme qui demande un numérateur et un dénominateur, puis affiche la fraction simplifiée.
  ```python
  from fractions import Fraction

  num = int(input("Entrez le numérateur : "))
  den = int(input("Entrez le dénominateur : "))

  if den != 0:
      fraction = Fraction(num, den)
      print(f"La fraction simplifiée est : {fraction}")
  else:
      print("Le dénominateur ne peut pas être zéro.")
  ```

---

### Partie 3 : Conversion fractions ↔ décimaux (10 min)

#### Convertir une fraction en décimal :
```python
f = Fraction(1, 3)
print(float(f))  # Résultat : 0.3333333333333333
```

#### Convertir un nombre décimal en fraction :
```python
f = Fraction(0.75)
print(f)  # Résultat : 3/4
```

#### Pratique guidée :
- Écrivez un programme qui :
  - Convertit des fractions en décimaux.
  - Convertit des nombres décimaux en fractions.
  ```python
  from fractions import Fraction

  choix = input("Voulez-vous convertir une fraction ou un décimal ? (fraction/decimal) : ")

  if choix == "fraction":
      num = int(input("Entrez le numérateur : "))
      den = int(input("Entrez le dénominateur : "))
      fraction = Fraction(num, den)
      print(f"Fraction {fraction} = Décimal {float(fraction)}")
  elif choix == "decimal":
      dec = float(input("Entrez un nombre décimal : "))
      fraction = Fraction(dec)
      print(f"Décimal {dec} = Fraction {fraction}")
  else:
      print("Choix invalide.")
  ```

---

### Partie 4 : Activité finale (15 min)

#### Objectif :
Créer un programme interactif qui :
1. Demande deux nombres (numérateur et dénominateur).
2. Vérifie si la fraction est simplifiable.
3. Permet de convertir la fraction en nombre décimal.

#### Exemple attendu :
```python
from fractions import Fraction

num = int(input("Entrez le numérateur : "))
den = int(input("Entrez le dénominateur : "))

if den == 0:
    print("Erreur : le dénominateur ne peut pas être zéro.")
else:
    fraction = Fraction(num, den)
    print(f"Fraction simplifiée : {fraction}")
    print(f"En décimal : {float(fraction)}")
```

#### Exercices supplémentaires :
1. Modifiez le programme pour calculer la somme de deux fractions données par l’utilisateur.
   ```python
   f1 = Fraction(int(input("Numérateur 1 : ")), int(input("Dénominateur 1 : ")))
   f2 = Fraction(int(input("Numérateur 2 : ")), int(input("Dénominateur 2 : ")))
   
   print(f"La somme des fractions est : {f1 + f2}")
   ```
2. Ajoutez une fonctionnalité pour vérifier si deux fractions sont équivalentes.

---

## Résumé et devoir (5 min)

### Résumé :
- Les fractions peuvent être manipulées et simplifiées facilement en Python avec la bibliothèque `fractions`.
- Les divisions décimales et entières sont des outils complémentaires pour travailler avec les nombres rationnels.

### Devoir :
1. Écrire un programme qui :
   - Demande deux fractions.
   - Affiche leur produit et leur différence.

#### Exemple attendu :
```python
from fractions import Fraction

f1 = Fraction(int(input("Numérateur 1 : ")), int(input("Dénominateur 1 : ")))
f2 = Fraction(int(input("Numérateur 2 : ")), int(input("Dénominateur 2 : ")))

print(f"Produit : {f1 * f2}")
print(f"Différence : {f1 - f2}")
