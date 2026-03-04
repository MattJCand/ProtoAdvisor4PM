#  ProtoAdvisor

> Arrête de sur-ingéniérer tes prototypes. Construis le bon, vite.

---

## Le problème

La plupart des PMs perdent du temps à construire le mauvais prototype.

Ils passent un sprint sur un prototype Figma alors qu'une interview de 30 minutes aurait répondu à la question. Ou ils font des interviews utilisateurs alors que ce dont ils ont besoin c'est une landing page pour mesurer l'intention réelle.

**Le résultat :** des décisions retardées, des cycles de dev gaspillés, et des hypothèses qui restent des hypothèses.

## Ce que ça fait

ProtoAdvisor est un outil de décision léger qui prend ton hypothèse et recommande la bonne méthode de prototype en moins de 2 minutes.

3 questions. 1 recommandation. Des étapes concrètes.

```
Hypothèse → Type de risque → Besoin de validation → Prototype recommandé
```

## La logique de décision

Le moteur de recommandation repose sur une matrice simple :

| Risque | Besoin de validation | Prototype recommandé |
|--------|---------------------|----------------------|
| Désirabilité | Comportement réel | Landing Page |
| Désirabilité | Retour qualitatif | Script d'interview |
| Désirabilité | Preuve technique | Wizard of Oz |
| Désirabilité | Intention d'achat | Fake Door |
| Faisabilité | Comportement réel | Spike technique |
| Faisabilité | Retour qualitatif | Discussion technique |
| Faisabilité | Preuve technique | POC |
| Faisabilité | Intention d'achat | Chiffrage rapide |
| Viabilité | Comportement réel | Wizard of Oz |
| Viabilité | Retour qualitatif | Entretien économique |
| Viabilité | Preuve technique | Business case chiffré |
| Viabilité | Intention d'achat | Landing Page + Pricing |
| Utilisabilité | Comportement réel | Test Figma |
| Utilisabilité | Retour qualitatif | Test 5 secondes |
| Utilisabilité | Preuve technique | Prototype no-code |
| Utilisabilité | Intention d'achat | Tri de cartes |

## Pourquoi cette approche

**Le choix que j'ai fait :** un arbre de décision statique plutôt qu'un agent IA.

La logique est explicite, traçable et rapide. Pas d'appels API, pas de latence, pas d'hallucinations. Chaque recommandation peut être rattachée à un raisonnement clair — ce qui compte quand tu dois convaincre une équipe de changer sa façon de travailler.

La limite : ça gère mal la nuance. Une hypothèse peut porter plusieurs types de risques à la fois. Une version future pourrait pondérer plusieurs dimensions plutôt que de forcer un choix unique.

## Ce que j'améliorerais

- [ ] Permettre la sélection multiple sur le type de risque (la plupart des hypothèses en portent 2+)
- [ ] Ajouter une dimension "temps disponible" (1 jour vs 1 sprint change tout)
- [ ] Sauvegarder et comparer les hypothèses sur un cycle de discovery
- [ ] Exporter la recommandation en one-pager à partager avec l'équipe
- [ ] Enrichir la matrice à partir de vraies décisions PM

## Stack

HTML / CSS / JS pur. Aucune dépendance, aucune étape de build, aucun framework.

Ouvre `index.html` dans un navigateur, ça tourne.

## Contexte

Construit par un PM qui en avait marre de voir des équipes passer deux semaines sur des prototypes qu'une conversation de cinq minutes aurait pu remplacer.

Le meilleur prototype c'est celui qui répond à ta question le plus vite — pas le plus soigné.
