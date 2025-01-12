# Leçon 2 : Conditions et résolution d’équations du premier degré

## Objectifs :
- Comprendre et utiliser les conditions Python (if, elif, else).
- Résoudre des équations du premier degré \( ax + b = 0 \) en Python.
- S’exercer à déboguer la logique conditionnelle et à écrire des équations sous forme de fonctions.

---

### 1. Vocabulaire : Conditions en Python

| Mot-clé  | Signification                                   | Exemple                                   |
|----------|-------------------------------------------------|-------------------------------------------|
| if       | Démarre une condition                           | if x > 0:                                 |
| elif     | Ajoute une autre condition à vérifier           | elif x == 0:                              |
| else     | S’exécute si aucune autre condition n’est vraie | else:                                     |
| True     | Une valeur booléenne représentant la vérité     | if True:                                  |
| False    | Une valeur booléenne représentant le faux       | if False:                                 |

#### Exercice 1 : Faites correspondre le mot-clé à sa description.
1. S’exécute seulement si toutes les autres conditions sont fausses → ________
2. Ajoute une condition supplémentaire → ________
3. Une valeur booléenne qui représente la vérité → ________

---

### 2. Résoudre des équations \( ax + b = 0 \)

#### Étapes de résolution :
1. Réorganiser l’équation : \( x = -\frac{b}{a} \).
2. Gérer les cas particuliers (par ex. \( a = 0 \)).
3. Utiliser des conditions pour traiter ces cas.

#### Exemple de code :

    def solve_equation(a, b):
        if a == 0:
            if b == 0:
                return "Solutions infinies"
            else:
                return "Pas de solution"
        else:
            return -b / a

# Exemple d’utilisation :
# print(solve_equation(2, -4))  # Sortie : 2.0

#### Exercice 2 : Indiquez la sortie pour ces exemples.
1. solve_equation(0, 0) → ________
2. solve_equation(0, 3) → ________
3. solve_equation(5, -10) → ________

---

### 3. Débogage de conditions

#### Erreurs courantes :
1. Oubli de deux-points (:) après if, elif ou else.
2. Utiliser = au lieu de == pour les comparaisons.
3. Mauvaise indentation.

#### Exemples à déboguer :

1. 

        def check_positive(x):
            if x > 0
                return "Positif"
            else:
                return "Pas positif"

2. 

        number = 10
        if number = 10:
            print("Dix")

3. 

        value = -5
        if value > 0:
        print("Positif")
        else:
            print("Négatif")

#### Exercice 3 : Corrigez les erreurs dans les exemples ci-dessus.

---

### 4. Écrire des fonctions pour les équations

#### Exemple : Résoudre des équations

    def solve_linear(a, b, c):
        """Résout des équations de la forme ax + b = c."""
        if a == 0:
            return "Pas de solution ou solutions infinies"
        else:
            return (c - b) / a

    # print(solve_linear(2, 3, 7))  # Sortie : 2.0

#### Exercice 4 : Écrivez ces fonctions.
1. is_positive(x) : Renvoie True si \( x > 0 \), sinon False.
2. find_root(a, b, c) : Résout \( ax + b = c \).
3. check_even(x) : Renvoie True si \( x \) est pair, sinon False.

#### Exercice 5 : Débogage de fonctions

Corrigez les erreurs dans ces fonctions :

1.

        def is_positive(x):
        if x > 0:
            return True
        else
            return False

2.

        def find_root(a, b):
            return -b / a
        print(find_root(0, 5))

3.

        def check_even(x):
            if x % 2 == 0
                print("Pair")

---

### 5. Défi : Implémenter une mini-calculatrice

#### Problème :
Créer un programme qui puisse :
1. Résoudre \( ax + b = c \)
2. Vérifier si un nombre est pair ou impair.
3. Déterminer si un nombre est positif, négatif ou nul.

#### Exemple de code :

    def mini_calculator():
        print("1. Résoudre ax + b = c")
        print("2. Vérifier si un nombre est pair ou impair")
        print("3. Vérifier si un nombre est positif ou négatif")

        choice = int(input("Entrez votre choix : "))

        if choice == 1:
            a = float(input("Entrez a : "))
            b = float(input("Entrez b : "))
            c = float(input("Entrez c : "))
            print("Solution :", (c - b) / a if a != 0 else "Pas de solution")
        elif choice == 2:
            x = int(input("Entrez un nombre : "))
            print("Pair" if x % 2 == 0 else "Impair")
        elif choice == 3:
            x = float(input("Entrez un nombre : "))
            if x > 0:
                print("Positif")
            elif x < 0:
                print("Négatif")
            else:
                print("Zéro")
        else:
            print("Choix invalide")

    # mini_calculator()

#### Exercice 6 : Faites évoluer le programme.
1. Ajoutez une option pour calculer la valeur absolue d’un nombre.
2. Ajoutez une validation de saisie pour vous assurer que les utilisateurs entrent des nombres valides.

---

### Devoir :
1. Écrivez une fonction pour vérifier si un nombre est divisible par un autre.
2. Créez un programme pour résoudre \( ax^2 + bx + c = 0 \) en utilisant le discriminant.
3. Rédigez un script pour déterminer le plus grand de deux nombres saisis par l’utilisateur.

---

À la fin de cette leçon, vous devriez comprendre :
- Comment utiliser efficacement les conditions en Python.
- Comment résoudre des équations du premier degré par programmation.
- Comment déboguer et étendre la logique conditionnelle en Python.
