# Formules AppSheet

## Consigne
Documentez uniquement les formules IMPORTANTES.

## Formule 1
- Nom : Formule de Moyenne Hydratation
- Où : Journal Bien Etre
- Formule : AVERAGE(SELECT(Journal bien etre[Hydratation], TRUE))
- Explication AVEC VOS MOTS : selectionne et calcule une moyenne des données d'hydrataion

## Formule 2
- Nom : Formule de Moyenne Sommeil
- Où : Journal Bien Etre
- Formule : 

AVERAGE(
  SELECT(
    Journal bien etre[Sommeil],
    [week] = [_THISROW].[week]
  )
)

- Explication AVEC VOS MOTS : selectionne et crée une moyenne par semaine des données de sommeil.

## Règle
Vous devez comprendre chaque formule utilisée.
