# La méthode de vérification, et ce qu'elle a trouvé

## Le problème

Une IA interrogée sur des documents répond avec assurance. Elle cite. Parfois elle invente — pas seulement des sources, mais des phrases précises entre guillemets, attribuées à un auteur qui ne les a jamais écrites. Une paraphrase devient une citation, un mot change, une anecdote est prêtée au mauvais auteur.

Si vous construisez une fiche, un protocole, un argumentaire sur ces citations, **vous construisez sur du faux**, et vous ne le saurez jamais.

## La méthode, en quatre étapes

1. **Consigne stricte.** Dans chaque interrogation : « réponds uniquement à partir des sources ; pour chaque affirmation importante, cite le passage entre guillemets avec le titre de la source ; si les sources ne disent rien, écris *rien dans les sources* ».
2. **Extraction du texte des sources**, avec des repères de page, pour disposer de l'original.
3. **Vérification automatique.** On relève chaque passage entre « ... » dans la réponse de l'IA, on le normalise (césures, ligatures, numéros de page, renvois de note supprimés), puis on le cherche dans la source par ancres de 5 mots et comparaison locale. Trois verdicts : **EXACT**, **APPROCHE** (la formulation existe presque, avec des mots sensibles modifiés), **REJET** (introuvable).
4. **Vérification manuelle** des cas APPROCHE : on ouvre le livre et on tranche.

## Les résultats, corpus par corpus

| Corpus | Sources | Citations | Exactes | Écartées |
|---|---|---|---|---|
| Négociation (Voss, Malhotra & Bazerman, Fisher & Ury…) | 5 | 197 | 159 | 38 |
| Entretien (Abrahams, Voss, Crucial Conversations, Culture Map) | 4 | 105 | 69 | 36 |
| Influence (Cialdini, Pre-Suasion…) | 3 | 202 | 149 | 53 |
| Jugement et décision (Kahneman, Sibony, Agrawal-Gans-Goldfarb…) | 34 | 125 | 109 | 16 |
| Métier d'évaluateur (MT-Bench, G-Eval, InstructGPT, LLMs not fair evaluators, Google Rater Guidelines) | 5 | 90 | 65 | 25 |
| **Total** | **51** | **719** | **551 (77 %)** | **168 (23 %)** |

## Trois exemples de ce qui a été attrapé

- **Une anecdote prêtée au mauvais auteur.** Une histoire attribuée à Cialdini sur un recrutement sans qualification, absente du livre. Remplacée par l'étude réellement décrite dans le texte, citation vérifiée à la main.
- **Une citation inventée de toutes pièces** attribuée à Malhotra et Bazerman sur le premier prix annoncé dans une négociation — introuvable dans l'ouvrage.
- **Une paraphrase présentée entre guillemets**, avec un mot changé, ce qui en inversait le sens.

## Pourquoi c'est le cœur du métier

Ce n'est pas un détail technique. Un évaluateur qui ne vérifie pas ses sources reproduit à l'échelle d'un rapport ce que l'IA fait à l'échelle d'une phrase. La règle que j'en tire, et que j'applique :

> **Aucune citation ne sort avant d'avoir été retrouvée dans le texte. Et quand la source est muette, on l'écrit : « rien dans les sources ».**

## Ce que ce chiffre ne dit pas

Ce 23 % décrit **les citations contrôlées dans ces cinq corpus**, pas un taux d'erreur général. Il dépend des sources, de la langue et des consignes. Deux réserves, et elles sont importantes :

- **Les défauts d'extraction ne sont pas des mensonges.** Une citation rejetée peut venir d'un PDF mal extrait, d'une ligature non normalisée ou d'une césure. Le comptage distingue les deux, mais la frontière est parfois floue.
- **Une citation exacte ne prouve rien sur la vérité de l'affirmation.** Elle prouve que l'auteur a écrit cette phrase. Savoir si l'auteur a raison est un autre travail — celui du registre des preuves (`REGISTRE-DES-PREUVES.md`).

## Trois règles ajoutées après revue

1. **Aucune conclusion importante sans recherche contradictoire documentée**, et sans contrôle de l'adéquation entre la preuve et l'affirmation.
2. **Dédupliquer les preuves par étude originale** : cinq livres et interviews qui reprennent la même expérience ne sont pas cinq confirmations indépendantes.
3. **« Aucune réplication trouvée » n'est pas « résultat non répliqué ».** On écrit laquelle des deux on a constatée.

## Les limites de la méthode

- Elle vérifie des citations, pas des raisonnements : une phrase exacte peut être utilisée pour dire le contraire de ce que l'auteur voulait dire. C'est l'étape manuelle qui rattrape ça.
- Elle dépend de la qualité de l'extraction : un PDF scanné sans OCR ne donnera rien.
- Elle ne dit rien de la représentativité : dix citations exactes ne prouvent pas qu'une thèse est juste.
