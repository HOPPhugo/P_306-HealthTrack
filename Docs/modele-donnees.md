# Modèle de données

## Consigne
Vous devez définir VOUS-MEMES la structure des données.

## Tables

### Table Bien être
| ID | Humeur | Sommeil | Date |Commentaire|Week|Moyenne sommeil|
|----|--------|---------|------|-----------|----|---------------|
|    |        |         |      |           |    |               |

### Table nutrition
| ID | Date | Moment du repas | Categorie | Commentaire | Nombre de verres d'eau |
|---|--------|------|-------------|-------------|---|
|   |        |      |             |             |   |

### Table Sport
| ID | Date | Type de Sport | Duree | Intensitee | Commentaire | week|COUNT|
|---|--------|------|-------------|-------------|-------------|----|-------|
|   |        |      |             |             |             |   |       |

### Tableau de bord
| ID | Objectif Sommeil | Objectif séance | Date |Moyenne sommeil|Week|Moyenne séance par semaine|Objectif seance sport|
|----|--------|---------|------|-----------|----|---------------|---------------------------------|
|    |        |         |      |           |    |               |                                 |
## Questions à vous poser
- Quelles données sont nécessaires ?
  Humeur, Sommeil, Nombre de verres d'eau, Date, Categorie, Type de Sport, Duree, Intensitee,week
  
- Quelles contraintes doivent être respectées ?
  Le sport doit exister et la duree cumulée dans les differentes activités de la journée ne dépasse pas 24h.
  Le nombre de verres d'eau ne dépasse pas 12.
- Comment éviter les erreurs de saisie ?
 en faisant attention
