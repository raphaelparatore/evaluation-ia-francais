# Évaluer une réponse d'IA en français — protocole, méthode de vérification, résultats

**Raphaël Paratore** · novembre 2026 · document reproductible, toute critique est bienvenue.

## Ce que ce dépôt contient, en une phrase

Un protocole en neuf étapes pour noter une réponse d'IA en français, la méthode que j'utilise pour vérifier ce qu'une IA affirme, et les résultats chiffrés de cette vérification sur cinq corpus.

## Pourquoi c'est public

Je ne suis pas diplômé en linguistique. Ce que je peux montrer, c'est un travail écrit, daté, et refaisable par n'importe qui. Ce dépôt est ma preuve de travail, pas un CV.

## 1. Le protocole en neuf étapes

Fichier : [`PROTOCOLE.md`](PROTOCOLE.md)

Neuf gestes ordonnés, environ 10 à 12 minutes par réponse : lire la consigne, lire la réponse sans rien noter, relever les affirmations vérifiables, vérifier les trois plus importantes, sentir le ton et le naturel, remplir une grille de six dimensions notées de 0 à 3 avec des repères écrits, appliquer les plafonds, poser la note globale en dernier, et rédiger une justification d'une phrase adossée à une preuve.

Les étiquettes sont tenues tout du long : **CONSTATÉ / SOURCÉ / NON VÉRIFIÉ** pour les faits, **FAIT / INFÉRENCE / JUGEMENT** pour mes propres énoncés.

Règle de plafond, la plus importante : **un fait inventé dans une réponse plafonne la note globale à 1 sur 5**, quelle que soit la qualité du reste.

## 2. La méthode de vérification, et son résultat

Fichier : [`VERIFICATION.md`](VERIFICATION.md)

J'ai fait lire des corpus de référence à une IA, avec une consigne stricte : citer mot pour mot, et écrire « rien dans les sources » quand la source est muette. Puis j'ai vérifié **chaque citation dans le texte original**, par recherche d'ancres et comparaison locale, en neutralisant les pièges de l'extraction : césures, ligatures, numéros de page, renvois.

| Corpus | Citations | Exactes | Écartées |
|---|---|---|---|
| Négociation (5 ouvrages) | 197 | 159 | 38 |
| Entretien (4 ouvrages) | 105 | 69 | 36 |
| Influence (3 ouvrages) | 202 | 149 | 53 |
| Jugement et décision (34 sources) | 125 | 109 | 16 |
| Métier d'évaluateur (5 documents publics) | 90 | 65 | 25 |
| **Total** | **719** | **551 (77 %)** | **168 (23 %)** |

**Ce que ça veut dire :** sur les 719 citations contrôlées de ces cinq corpus, **168 (23 %) étaient introuvables ou déformées dans le texte original** — et l'IA les présentait avec le ton de la certitude. La méthode les a repérées avant qu'elles servent.

Ce chiffre décrit **ce corpus-là**, pas un taux d'erreur général des IA : il dépend des sources, des consignes et de la langue. Ce qui se généralise, c'est la méthode, pas le pourcentage.

## 3. Un cas travaillé de bout en bout

Fichier : [`CAS-01.md`](CAS-01.md)

Un cas fictif : une réponse d'IA qui contient quatre défauts — un conseil contraire à l'Académie française, une loi datée de 1996 au lieu de 1994, une amende inventée, et de la flatterie. Le protocole appliqué geste par geste, la grille remplie, la note finale et la bonne réponse modèle.

## 4. Le registre des preuves
Fichier : [`REGISTRE-DES-PREUVES.md`](REGISTRE-DES-PREUVES.md)

Une citation exacte prouve que l'auteur a écrit la phrase, pas que l'affirmation est vraie. Le registre force, pour chaque étude : population, méthode, taille d'effet, financement, statut de publication, réplications et rétractations — et ce que la preuve **ne** permet pas de conclure.

## 5. Ce que cette méthode ne fait pas
Fichier : [`LIMITES.md`](LIMITES.md)

Courte liste assumée : elle ne rend pas un débutant expert, elle dépend de la qualité des sources, elle ne remplace pas la grille d'un client, et ses évaluations de tonalité sont subjectives — c'est précisément pour ça qu'elle les sépare de la mécanique.

## Contact

Raphaël Paratore — raphael.gparatore@gmail.com

*Si vous évaluez des réponses d'IA en français et que ce document vous paraît faux, incomplet ou naïf, dites-le-moi : c'est la meilleure façon de le corriger.*
