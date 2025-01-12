# Cours 7 : Simulation de probabilités

## Objectifs pédagogiques :
1. Comprendre les bases des probabilités et leur représentation en Python.
2. Apprendre à utiliser la bibliothèque `random` pour simuler des événements aléatoires.
3. Appliquer les concepts de probabilités simples à travers des simulations interactives.

---

## Plan du cours :

### Partie 1 : Introduction aux probabilités (10 min)

#### Rappel mathématique :
- **Probabilité d’un événement :**
  \[ P(A) = \frac{\text{Nombre de cas favorables}}{\text{Nombre de cas possibles}} \]
- Exemple : La probabilité d’obtenir un 6 en lançant un dé :
  \[ P(6) = \frac{1}{6} \]

#### Exemple simple en Python :
- Simuler un tirage de dé :
  ```python
  import random

  de = random.randint(1, 6)
  print(f"Le dé a affiché : {de}")
  ```

#### Pratique guidée :
1. Simulez 5 tirages d’un dé à 6 faces.
   ```python
   for _ in range(5):
       print(random.randint(1, 6))
   ```
2. Demandez à l’utilisateur combien de tirages il veut effectuer.

#### Exercices supplémentaires :
1. Ajoutez une vérification pour compter combien de fois le 6 apparaît dans les tirages.
2. Simulez un dé à 10 faces en modifiant la plage de valeurs.

---

### Partie 2 : Simulation de tirages et calcul de probabilités (15 min)

#### Simuler plusieurs tirages :
- Enregistrez les résultats dans une liste pour analyser les fréquences :
  ```python
  tirages = []
  for _ in range(100):
      tirages.append(random.randint(1, 6))

  print(tirages)
  print(f"Nombre de 6 : {tirages.count(6)}")
  ```

#### Calculer les probabilités :
- Exemple : Calculer la probabilité d’obtenir un 6 :
  ```python
  nb_6 = tirages.count(6)
  prob_6 = nb_6 / len(tirages)
  print(f"Probabilité d’obtenir un 6 : {prob_6:.2f}")
  ```

#### Pratique guidée :
1. Simulez 100 tirages d’un dé et calculez la probabilité de chaque face.
2. Comparez les probabilités calculées à la probabilité théorique \( \frac{1}{6} \).

#### Exercices supplémentaires :
1. Ajoutez une fonctionnalité pour simuler un lancer de deux dés et calculer la probabilité d’obtenir une somme donnée.
   ```python
   somme_voulue = int(input("Entrez la somme voulue : "))
   total = 0
   essais = 1000

   for _ in range(essais):
       de1 = random.randint(1, 6)
       de2 = random.randint(1, 6)
       if de1 + de2 == somme_voulue:
           total += 1

   print(f"Probabilité estimée : {total / essais:.2f}")
   ```
2. Simulez un jeu où un joueur gagne si un dé affiche 6, sinon il perd.

---

### Partie 3 : Simulation d’une urne (15 min)

#### Rappel mathématique :
- Une urne contient des boules rouges et bleues.
- Probabilité de tirer une boule rouge : \( \frac{\text{Nombre de boules rouges}}{\text{Nombre total de boules}} \).

#### Exemple en Python :
- Simuler un tirage :
  ```python
  urne = ["rouge", "bleu", "rouge", "bleu", "rouge"]
  tirage = random.choice(urne)
  print(f"Tirage : {tirage}")
  ```

#### Pratique guidée :
1. Ajoutez une fonctionnalité pour effectuer plusieurs tirages et compter les boules rouges tirées.
   ```python
   rouge = 0
   for _ in range(20):
       if random.choice(urne) == "rouge":
           rouge += 1

   print(f"Nombre de boules rouges tirées : {rouge}")
   ```
2. Modifiez le programme pour que l’utilisateur puisse personnaliser la composition de l’urne.

#### Exercices supplémentaires :
1. Créez une simulation où chaque boule est retirée après le tirage (sans remise).
2. Ajoutez une option pour réinitialiser l’urne après chaque série de tirages.

---

### Partie 4 : Activité finale (15 min)

#### Objectif :
Créer un programme interactif qui :
1. Simule un tirage d’un dé ou d’une urne.
2. Permet de calculer les probabilités estimées en fonction des résultats obtenus.

#### Exemple attendu :
```python
import random

choix = input("Choisissez : dé ou urne ? ").lower()

if choix == "dé":
    essais = int(input("Nombre de tirages : "))
    tirages = [random.randint(1, 6) for _ in range(essais)]
    for face in range(1, 7):
        print(f"Probabilité d’obtenir {face} : {tirages.count(face) / essais:.2f}")

elif choix == "urne":
    rouge = int(input("Nombre de boules rouges : "))
    bleu = int(input("Nombre de boules bleues : "))
    urne = ["rouge"] * rouge + ["bleu"] * bleu
    essais = int(input("Nombre de tirages : "))

    tirages = [random.choice(urne) for _ in range(essais)]
    print(f"Probabilité d’obtenir une boule rouge : {tirages.count('rouge') / essais:.2f}")
    print(f"Probabilité d’obtenir une boule bleue : {tirages.count('bleu') / essais:.2f}")
else:
    print("Choix invalide.")
```

---

## Résumé et devoir (5 min)

### Résumé :
- Python, avec la bibliothèque `random`, permet de simuler des événements aléatoires comme les tirages de dés ou d’urnes.
- Ces simulations permettent de calculer des probabilités estimées.

### Devoir :
1. Écrire un programme qui :
   - Simule le lancer de deux dés.
   - Affiche la probabilité estimée d’obtenir une somme supérieure à 8 après 1,000 lancers.

#### Exemple attendu :
```python
import random

somme_sup_8 = 0
lancers = 1000

for _ in range(lancers):
    de1 = random.randint(1, 6)
    de2 = random.randint(1, 6)
    if de1 + de2 > 8:
        somme_sup_8 += 1

print(f"Probabilité estimée : {somme_sup_8 / lancers:.2f}")
