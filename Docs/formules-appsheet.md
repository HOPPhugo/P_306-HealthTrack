# Formules AppSheet

## Consigne
Documentez uniquement les formules IMPORTANTES.

## Formule 1
- Nom : Formule de Moyenne Hydratation
- Où : Tableau de bord
- Formule : AVERAGE(SELECT(Journal bien etre[Hydratation], TRUE))
- Explication AVEC VOS MOTS : selectionne et calcule une moyenne des données d'hydrataion.

## Formule 2
- Nom : Formule de Moyenne Sommeil
- Où : Tableau de bord
- Formule : if ([Objectif sommeil] > 0, AVERAGE(
  Journal bien etre[Moyenne Sommeil]
) & "/" & [Objectif sommeil], "")
- Explication AVEC VOS MOTS : selectionne et crée une moyenne par semaine des données de sommeil.

## Formule 3
- Nom : Moyenen séances par semaines
- Où : Tableau de bord
- Formule : AVERAGE(Journal sport[COUNT])
- Explication AVEC VOS MOTS : fait une moyenne du nombre de séances par semaines ("COUNT" est une variable qui contient le nombre de séance pour chaque semaines)

## Formule 4
- Nom : Objectife séance de sport / semaine
- Où : Tableau de bord
- Formule : if ([Objectif Séance] > 0, COUNT(SELECT(Journal sport[ID], [week] = [_THISROW].[Week])) & " / " & [Objectif Séance], "")
- Explication AVEC VOS MOTS : en premier temps, vérifie si ce n'est pas vide, sinon on ne l'affiche pas, si oui compte la selection le nombre de séances où la semaine selectionée sur l'objectif est égale à celles rentrées

## Formule 5
- Nom : Moyenne hydra
- Où : Tableau de bord
- Formule : IF(AVERAGE(Journal Nutrition[Nombre de verre d'eau]) <= 0, "Vous n'avez pas bu, ce n'est pas bien",AVERAGE(Journal Nutrition[Nombre de verre d'eau]) )
- Explication AVEC VOS MOTS : en premier temps, vérifie si l'utilisateur à bien bu et affiche un message selon le resultat, si oui fait une moyenne du nombre de verres d'eau récupéré sur journal nutrition

## Formule 6
- Nom : Tôtal séances
- Où : Tableau de bord
- Formule : COUNT(SELECT(Journal sport[ID], TRUE))
- Explication AVEC VOS MOTS : Selection et compte le nombre d'entrées dans le journal de sport

## Formule 7
- Nom : Statut
- Où : Tableau de bord
- Formule : IF(
  AND(
    COUNT(SELECT(Journal sport[ID], [week] = [_THISROW].[Week])) >= [Objectif Séance],
    
    COUNT(SELECT(Journal sport[ID], [week] = [_THISROW].[Week])) >= [Objectif hydratation],
    
    AVERAGE(Journal bien etre[Moyenne Sommeil]) >= [Objectif sommeil]
  ),
  "GOOD",
  "NOT GOOD"
)
- Explication AVEC VOS MOTS : vérifie chaques objectifs et les compares aux acquis et s'il y a un objetcif non acquis affiche "NOT GOOD" s'ils sont tous acquis, alors affiche "GOOD".

## Formule 8
- Nom : Moyenne humeure
- Où : Tableau de bord
- Formule : if (AVERAGE(SELECT(Journal bien etre[Humeur], TRUE)) <= 1, AVERAGE(SELECT(Journal bien etre[Humeur], TRUE)) & " / 5 : Ta vie est fade, sans goût", AVERAGE(SELECT(Journal bien etre[Humeur], TRUE)) & " / 5 : Ta vie est merveilleuse, incroyable, ravissante, lumineuse, magnifique, banger, peak ! 🔥")
- Explication AVEC VOS MOTS : vérifie l'état de la moyenne de d'humeure puis affiche la moyenne + "Ta vie est fade, sans goût" si pas très heureux, et inversement toujours la moyenne mais le texte deviens : "Ta vie est merveilleuse, incroyable, ravissante, lumineuse, magnifique, banger, peak ! 🔥".

## Formule 9
- Nom : COUNT
- Où : Journal de sport
- Formule : COUNT(
  SELECT(
    Journal sport[ID],
    [week] = [_THISROW].[week]
  )
)
- Explication AVEC VOS MOTS : Compte le nombre de séances de sport où la semaine actuelle est celle qui est enregistrée

## Formule 10
- Nom : Moyenne de sommeil
- Où : Jouranl bien être
- Formule : AVERAGE(
  SELECT(
    Journal bien etre[Sommeil],
    [week] = [_THISROW].[week]
  )
)
- Explication AVEC VOS MOTS : fait une moyenne des nombres d'heures de sommeil où la semaine actuelle est celle qui est enregistrée


## Règle
Vous devez comprendre chaque formule utilisée.
