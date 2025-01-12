# Cours 2 : Les nombres et les tables de multiplication

## Objectifs pédagogiques :
1. Apprendre à utiliser des boucles pour effectuer des calculs répétitifs.
2. Générer les tables de multiplication en Python.
3. Réviser les notions de multiplication et de diviseurs.

---

## Plan du cours :

### Partie 1 : Révision des multiplications (10 min)

#### Introduction :
- La multiplication est une addition répétée.
- Exemple :
  - \( 3 \times 4 = 3 + 3 + 3 + 3 = 12 \)

#### Python et la multiplication :
- Exemple simple :
  ```python
  print(3 * 4)  # Affiche 12
  ```

#### Pratique :
- Demandez aux élèves de calculer :
  - \( 6 \times 8 \)
  - \( 9 \times 7 \)
  - \( 12 \times 5 \)

#### Exercices supplémentaires :
- Calculez :
  - \( 15 \times 4 \)
  - \( 11 \times 9 \)
  - \( 7 \times 13 \)

---

### Partie 2 : Générer une table de multiplication avec une boucle (15 min)

#### Utilisation d’une boucle `for` :
- Une boucle permet de répéter une action plusieurs fois.
- Exemple : Générer la table de multiplication de 3 :
  ```python
  for i in range(1, 11):
      print(f"3 x {i} = {3 * i}")
  ```
  - **Explication :**
    - `range(1, 11)` génère les nombres de 1 à 10.
    - Pour chaque valeur de `i`, le produit \( 3 \times i \) est affiché.

#### Pratique guidée :
- Demandez aux élèves d’écrire un programme qui génère la table de multiplication de 5.

#### Exercices supplémentaires :
1. Écrivez un programme pour générer les tables de multiplication de 2 à 5.
   ```python
   for n in range(2, 6):
       print(f"Table de {n}")
       for i in range(1, 11):
           print(f"{n} x {i} = {n * i}")
       print()
   ```
2. Modifiez le programme pour afficher la table de multiplication jusqu’à 12 au lieu de 10.

---

### Partie 3 : Tables de multiplication interactives (15 min)

#### Objectif :
- Permettre à l’utilisateur de choisir la table de multiplication qu’il souhaite afficher.

#### Exemple :
```python
nombre = int(input("Entrez un nombre pour voir sa table de multiplication : "))

for i in range(1, 11):
    print(f"{nombre} x {i} = {nombre * i}")
```

#### Pratique :
- Demandez aux élèves :
  - De modifier le programme pour que l’utilisateur puisse choisir jusqu’où afficher la table (par exemple, jusqu’à 12).

#### Exercices supplémentaires :
1. Demandez à l’utilisateur combien de tables de multiplication il souhaite afficher (par exemple, de 2 à 4).
   ```python
   debut = int(input("Entrez le premier nombre : "))
   fin = int(input("Entrez le dernier nombre : "))

   for n in range(debut, fin + 1):
       print(f"Table de {n}")
       for i in range(1, 11):
           print(f"{n} x {i} = {n * i}")
       print()
   ```
2. Ajoutez une fonctionnalité pour demander si l’utilisateur veut continuer après avoir affiché une table.

---

### Partie 4 : Vérifier si un nombre est un diviseur (10 min)

#### Introduction :
- Un nombre \( a \) est un diviseur de \( b \) si \( b \mod a = 0 \).
- Exemple :
  - 3 est un diviseur de 12 car \( 12 \div 3 = 4 \) (reste 0).
  - 5 n’est pas un diviseur de 12 car \( 12 \div 5 \neq \) entier.

#### Exemple en Python :
```python
nombre = int(input("Entrez un nombre : "))
diviseur = int(input("Entrez un diviseur potentiel : "))

if nombre % diviseur == 0:
    print(f"{diviseur} est un diviseur de {nombre}.")
else:
    print(f"{diviseur} n'est pas un diviseur de {nombre}.")
```

#### Pratique guidée :
- Écrire un programme qui demande un nombre et affiche tous ses diviseurs (en utilisant une boucle).
  ```python
  nombre = int(input("Entrez un nombre : "))
  print("Les diviseurs de", nombre, "sont :")
  for i in range(1, nombre + 1):
      if nombre % i == 0:
          print(i)
  ```

#### Exercices supplémentaires :
1. Modifiez le programme pour afficher le nombre de diviseurs d’un nombre.
   ```python
   nombre = int(input("Entrez un nombre : "))
   compteur = 0

   for i in range(1, nombre + 1):
       if nombre % i == 0:
           print(i)
           compteur += 1

   print(f"Le nombre {nombre} a {compteur} diviseurs.")
   ```
2. Demandez à l’utilisateur de saisir deux nombres et trouvez leurs diviseurs communs.

---

### Partie 5 : Activité finale (15 min)

#### Objectif :
Créer un programme interactif qui permet :
1. De choisir un nombre.
2. D’afficher sa table de multiplication.
3. De vérifier si un autre nombre est un diviseur.

#### Exemple attendu :
```python
# Étape 1 : Générer une table de multiplication
nombre = int(input("Entrez un nombre pour voir sa table de multiplication : "))
for i in range(1, 11):
    print(f"{nombre} x {i} = {nombre * i}")

# Étape 2 : Vérifier les diviseurs
diviseur = int(input("Entrez un diviseur potentiel : "))
if nombre % diviseur == 0:
    print(f"{diviseur} est un diviseur de {nombre}.")
else:
    print(f"{diviseur} n'est pas un diviseur de {nombre}.")
```

#### Exercices supplémentaires :
1. Permettez à l’utilisateur de choisir plusieurs nombres et affichez leurs tables de multiplication respectives.
2. Ajoutez une option pour arrêter le programme en tapant "stop".

---

## Résumé et devoir (5 min)

### Résumé :
- Les boucles permettent de répéter des actions, comme afficher une table de multiplication.
- Un diviseur est un nombre qui divise un autre sans reste.

### Devoir :
1. Écrire un programme qui :
   - Demande un nombre à l’utilisateur.
   - Affiche la somme de tous ses diviseurs.

#### Exemple attendu :
```python
nombre = int(input("Entrez un nombre : "))
somme_diviseurs = 0

for i in range(1, nombre + 1):
    if nombre % i == 0:
        somme_diviseurs += i

print(f"La somme des diviseurs de {nombre} est {somme_diviseurs}.")
```
