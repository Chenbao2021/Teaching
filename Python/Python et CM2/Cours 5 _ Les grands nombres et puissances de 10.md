# Cours 5 : Les grands nombres et puissances de 10

## Objectifs pédagogiques :
1. Comprendre la manipulation des grands nombres en Python.
2. Apprendre à travailler avec les puissances et la notation scientifique.
3. Relier les puissances de 10 à la numération et aux conversions d’unités.

---

## Plan du cours :

### Partie 1 : Les grands nombres en Python (10 min)

#### Rappel mathématique :
- Les grands nombres s’expriment souvent avec des puissances de 10 :
  - \( 1\,000 = 10^3 \)
  - \( 1\,000\,000 = 10^6 \)

#### Python et les grands nombres :
- Python peut gérer facilement les grands nombres :
  ```python
  grand_nombre = 1_000_000  # Utilisation de "_" pour améliorer la lisibilité
  print(grand_nombre)
  ```

#### Pratique guidée :
1. Affichez les grands nombres suivants en Python :
   - \( 10^3 \), \( 10^6 \), \( 10^9 \).
   ```python
   print(10 ** 3)
   print(10 ** 6)
   print(10 ** 9)
   ```
2. Utilisez des variables pour stocker ces valeurs et les afficher.

#### Exercices supplémentaires :
1. Demandez à l’utilisateur de saisir un nombre entier et multipliez-le par \( 10^5 \).
2. Écrivez un programme qui affiche le carré et le cube d’un nombre donné par l’utilisateur.

---

### Partie 2 : Les puissances en Python (15 min)

#### Calculer des puissances :
- Utilisation de l’opérateur `**` :
  ```python
  base = 2
  puissance = 3
  print(base ** puissance)  # Résultat : 8
  ```

#### Notation scientifique :
- Python permet d’utiliser la notation scientifique avec `e` :
  ```python
  grand_nombre = 1e6  # Équivaut à 10^6
  print(grand_nombre)
  ```

#### Pratique guidée :
1. Calculez :
   - \( 2^5 \), \( 5^3 \), \( 10^4 \).
   ```python
   print(2 ** 5)
   print(5 ** 3)
   print(10 ** 4)
   ```
2. Demandez à l’utilisateur d’entrer une base et une puissance, puis calculez le résultat.
   ```python
   base = int(input("Entrez la base : "))
   puissance = int(input("Entrez la puissance : "))
   print(f"Résultat : {base ** puissance}")
   ```

#### Exercices supplémentaires :
1. Modifiez le programme pour limiter la puissance à un maximum de 10 (ajoutez une condition).
2. Ajoutez une option pour convertir le résultat en notation scientifique si la valeur dépasse \( 10^6 \).

---

### Partie 3 : Conversion avec les puissances de 10 (15 min)

#### Conversion des unités :
- Relier les puissances de 10 aux unités courantes :
  - 1 kilomètre = \( 10^3 \) mètres.
  - 1 milligramme = \( 10^{-3} \) grammes.

#### Exemple :
- Convertir des kilomètres en mètres :
  ```python
  km = float(input("Entrez une distance en kilomètres : "))
  metres = km * 10 ** 3
  print(f"{km} kilomètres = {metres} mètres")
  ```

#### Pratique guidée :
1. Convertissez des kilogrammes en grammes.
2. Convertissez des millimètres en mètres.

#### Exercices supplémentaires :
1. Créez un programme qui demande une unité (km, m, cm, mm) et effectue la conversion vers une autre unité.
   ```python
   valeur = float(input("Entrez une valeur : "))
   unite = input("Entrez l’unité (km/m/cm/mm) : ").lower()

   if unite == "km":
       print(f"{valeur} km = {valeur * 1000} m")
   elif unite == "m":
       print(f"{valeur} m = {valeur * 100} cm")
   elif unite == "cm":
       print(f"{valeur} cm = {valeur * 10} mm")
   elif unite == "mm":
       print(f"{valeur} mm = {valeur / 1000} m")
   else:
       print("Unité non reconnue.")
   ```
2. Ajoutez une option pour convertir des mètres en kilomètres avec des résultats arrondis à 2 décimales.

---

### Partie 4 : Activité finale (15 min)

#### Objectif :
Créer un programme interactif qui :
1. Demande une base et une puissance pour calculer un grand nombre.
2. Demande une unité et effectue des conversions entre puissances de 10.

#### Exemple attendu :
```python
# Étape 1 : Calcul d’une puissance
base = int(input("Entrez une base : "))
puissance = int(input("Entrez une puissance : "))
resultat = base ** puissance

print(f"{base} ^ {puissance} = {resultat}")

# Étape 2 : Conversion d’unités
valeur = float(input("Entrez une valeur à convertir : "))
unite = input("Entrez l’unité (km/m/cm/mm) : ").lower()

if unite == "km":
    print(f"{valeur} km = {valeur * 1000} m")
elif unite == "m":
    print(f"{valeur} m = {valeur * 100} cm")
elif unite == "cm":
    print(f"{valeur} cm = {valeur * 10} mm")
elif unite == "mm":
    print(f"{valeur} mm = {valeur / 1000} m")
else:
    print("Unité non reconnue.")
```

---

## Résumé et devoir (5 min)

### Résumé :
- Python permet de travailler avec de très grands nombres et des puissances.
- La notation scientifique simplifie la manipulation des valeurs très grandes ou très petites.
- Les puissances de 10 facilitent les conversions d’unités courantes.

### Devoir :
1. Écrire un programme qui :
   - Calcule la puissance d’un nombre donné par l’utilisateur.
   - Convertit une valeur en kilomètres, mètres, centimètres ou millimètres selon l’unité choisie.

#### Exemple attendu :
```python
base = int(input("Entrez une base : "))
puissance = int(input("Entrez une puissance : "))
print(f"Résultat : {base ** puissance}")

valeur = float(input("Entrez une valeur : "))
unite = input("Entrez l’unité (km/m/cm/mm) : ").lower()

if unite == "km":
    print(f"{valeur} km = {valeur * 1000} m")
elif unite == "m":
    print(f"{valeur} m = {valeur * 100} cm")
elif unite == "cm":
    print(f"{valeur} cm = {valeur * 10} mm")
elif unite == "mm":
    print(f"{valeur} mm = {valeur / 1000} m")
else:
    print("Unité non reconnue.")
