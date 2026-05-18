# Utilisation de l'IA

## Outils utilisés
-  ChatGPT

## Ce que vous avez demandé
- ORDERBY(SELECT(Journal sport[ID], TRUE), Journal sport[week]) j'aimerai que ça me ressorte une liste du nombre de "Journal sport[ID]" par semaine, pour linstant ça me sort tous les id par semaine
- Comprendre comment créer un progrès de type "X/Y" (ex: 2/2 séances sport par semaine)
- Corriger des formules CONCATENATE, COUNT + FILTER qui ne fonctionnaient pas
- Résoudre l’erreur « DATE function is used incorrectly »
- Créer des Actions rapides (+1 verre d’eau, Séance rapide, Dupliquer repas)
- Concevoir le Dashboard et les virtual columns (Progrès Sport, Score du Jour, Message motivationnel)
- Mettre en place des Valid_If (ex: empêcher doublons même jour, hydratation entre 0 et 12)
- Structurer le projet GitHub (README, sprint-backlog, formules-appsheet, etc.)
- Proposer de nouvelles fonctionnalités (Streak, Score du Jour, Badges, etc.)

## Ce que vous avez compris
- que je ne pouvais pas simpement utiliser une commande qui me permet de trier les sorties des selectes
- Comment fonctionne le FILTER() combiné avec TODAY() et WEEKDAY() pour calculer les statistiques de la semaine en cours.
- La bonne utilisation de CONCATENATE() pour afficher du texte du type "2 / 3".
- Différence entre colonne normale et Virtual Column.
- Comment créer des Actions de type "Data: edit a row" et "Data: add a new row".
- Importance de bien nommer les tables et colonnes pour que les formules marchent.
- Structure recommandée pour documenter un projet AppSheet sur GitHub.

## Ce que vous avez modifié
- J'ai crée des variables dans journal de sport qui compte le nombre de séances pour chaques semaines et une autre qui stock la semaine choisie pour l'objectif et à l'entrée de séance. ce qui me permet après de récupérer et de faire des moyennes et des totaux.
- J’ai pris les formules proposées par l’IA et je les ai testées dans AppSheet.
- J’ai adapté les formules selon les vrais noms de mes tables et colonnes (Journal sport, Tableau de bord, [Objectif compelt], etc.).
- J’ai corrigé moi-même certaines erreurs (noms de colonnes, fautes de frappe).
- J’ai choisi les formules les plus simples et lisibles.

## Vérification
Comment avez-vous vérifié que la réponse est correcte ?
- En testant ce qui me dit sur appsheet et en modifiant par mes connaissances et mes besoins
- Toutes les formules ont été testées dans l’application AppSheet.
- J’ai vérifié que les compteurs de séances sport se mettent bien à jour selon la semaine.
- Les actions rapides fonctionnent correctement.
- Les validations (doublons, plages de valeurs) bloquent bien les saisies incorrectes.

## Règle
Vous restez responsables de votre travail.
