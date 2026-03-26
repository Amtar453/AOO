# Use Case : Vente en magasin

## Acteurs
- Client
- Caissier
- Système

## Préconditions
- Le caissier ne se trompe pas dans ses identifiants.
- Le client possède une carte de fidélité.
- Le client possède suffisamment de points de fidélité.
- Le client décide d'utiliser ses points de fidélité.
- Le client ne fait pas d'erreur dans le code PIN de sa carte bancaire.
- Le client souhaite obtenir le ticket de caisse imprimé.

## Use case

|Client|Caissier|Système|
|--------------------|--------------------|--------------------|
||Entre son identifiant et son mot de passe||
|||Vérifie l’existence de l'identifiant|
|||Vérifie la validité du mot du passe|
|||Affiche la page d’accueil|
|Récupère les articles souhaité|||
|Présente ses articles au caissier|||
||Scanne le code barre du premier article||
|||Création automatique du ticket déclenché par le scanne du premier article|
||Scanne le code barre pour le reste des articles||
|||Ajoute tous les articles scanné au ticket|
||Demande la carte de fidélité||
|Donne la carte de fidélité|||
||Récupère la carte de fidélité||
||Scanne la carte de fidélité||
|||Lie le compte client au ticket|
|||Affiche le nombre de points du client|
||Demande si il veut utiliser les points de fidélité||
|Répond qu'il veut les utiliser|||
||Sélectionne la réduction des points de fidélité||
|||Applique la réduction|
|||Réduit le nombre de points pour la réduction|
||Sélectionne l'option de payement||
|||Initialise le terminal de payement|
|Insert la carte bancaire dans le terminal|||
|||Demande le code PIN|
|Entre le code PIN|||
|||Valide le code PIN|
|||Appel au service bancaire avec les informations|
|||Confirme le payement|
|||Ajoute les points sur la carte de fidélité|
|Récupère sa carte bancaire|||
|||Clôture le ticket|
||Sélectionne l'impression du ticket de caisse||
|||Imprime le ticket de caisse|
||Récupère le ticket de caisse||
||Donne le ticket de caisse||
|Récupère le ticket de caisse|||
|Range ses articles|||
|Quitte le magasin|||





 