# Use Case : Préparation des plats

## Acteurs

- Cuisinier
- Chef Traiteur
- Gestionnaire de stock
- Responsable des ventes
- Systèmes

## Préconditions

Nous partirons du principe que tous les acteurs sont connecté sur la fenètre principal de l'application

Il existe un groupe reprenant tous les acteurs pour le partage de fichier entre les intervenants

Lors de la vérifications, les différents acteurs ne trouverons aucune erreur ou raison de changer les choses. 

## Use case

| Cuisnier | Chef Traiteur | Gestionnaire de stock | Responsable des ventes | Système |
|-----------|-----------|-----------|-----------|-----------|
|  |  |  | Demander l'accès aux recettes |  | Planifier les plats à préparer (Responsable Stock) 
|  |  |  |  | Vérifier les droits d'accès de l'utilisateur |
|  |  |  |  | Aller chercher la ressource sur le serveur |
|  |  |  |  | Renvoyer les recettes |
|  |  |  | Trouver les recettes que l'on souhaite faire en plat préparé |  |
|  |  |  | Créer un nouveau fichier "Ordre de préparation des plats" |  |
|  |  |  |  | Créer un fichier sur le serveur |
|  |  |  | Changer les droits d'accès pour le groupe "plat préparé" |  |
|  |  |  |  | Changer les droits d'accès pour que les acteurs suivants aient accès: Cuisinier, Chef Traiteur, Gestionnaire de stock et Responsable des ventes |
|  |  |  | Ajouter le(s) plat(s) à préparé(s) dans le fichier |  |
|  |  |  |  | Sauvegarder les modifications |
|  |  |  | Informer le "chef traiteur" qu'il doit compléter l'ordre de préparation |  |
|  | Consulter la liste du/des plat(s) à préparé(s) |  |  |  |
|  |  |  |  | Renvoyer la liste des plat(s) préparé(s) |
|  | Pour chaque plat ajouté: faire la liste des ingrédients, ajouter la recette et remarques, définir la date de production |  |  |  |
|  | Sauvegarder les modifications |  |  |  |
|  |  |  |  | Sauvegarder les modifications du fichier |
|  | Informer le gestionnaire de stock qu'il doit regarder à la disponibilité des ingrédients |  |  |  |
|  |  | Consulter la liste des plats à préparer |  |  |
|  |  |  |  | Renvoyer la liste des plat(s) préparé(s) |
|  |  | Faire la liste des ingrédients et leurs quantitées |  |  |
|  |  |  |  | Renvoyer la liste des ingrédients avec leurs quantité |
|  |  | Ouvrir les stocks |  |  |
|  |  |  |  | Vérifier les droits d'accès |
|  |  |  |  | Envoyer la liste des produits en stock avec leurs quantitées |
|  |  | Envoyer les stocks du magasin et la liste des ingrédients |  |  |
|  |  |  |  | Comparer les stocks du magasin et les ingrédients requis |
|  |  |  |  | Envoyer un résumé de la comparaison |
|  |  |  |  | Changer le status des produit présent à "Réservé préparation des plats" |
|  |  | Créer le fichier "Fiche des disponibilité" |  |  |
|  |  |  |  | Ajouter le fichier en mémoire |
|  |  | Modifier les droits d'accès en ajoutant: Responsable de vente et Chef traiteur |  |  |
|  |  |  |  | Sauvegarder les changements de droits d'accès |
|  |  | Faire la liste des ingrédients indisponible pour l'ensemble des plats prévu |  |  |
|  |  |  |  | Sauvegarder les modifications du fichier |
|  |  | Informer le Responsable de vente et Chef traiteur des ingrédients disponible et indisponible |  |  |
| Rencontrer le Chef traiteur et se mettre d'accord sur les nouvelles dates ou plats si besoin en fonction de la disponibilité des ingrédients |  |  |  |  |
| Informer le Responsable des stocks que tous est finalisé et les produits indisponible sont attendu à la date fixé pour la préparation des plats |  |  |  |  | 
| ***Lorsque la date de la préparation d'un des plats du fichier "Ordre de préparation"*** |
| Consulter les plats du jours à préparer |  |  |  |  |
|  |  |  |  | Renvoyer la liste des "plats préparer" |
| Consulter la liste des ingrédients nécéssaire |  |  |  |  |
| Aller chercher les ingrédients dans les stocks |  |  |  |  | 
|  |  | Modifier l'état des stock avec les ingrédients retiré |  |  |
|  |  |  |  | Modifier le contenu de la BD pour MàJ les stocks |
| Cuisiner les différents plats préparer et emballé |  |  |  |  | 
| MàJ l'état des stocks avec les plats préparé |  |  |  |  |
|  |  |  |  | Récupérer les nouvelles entrées avec les plats préparé |
|  |  |  |  | Imprimer les étiquettes des nouvelles entrée | 
| Placer les étiquettes sur les plats préparé |  |  |  |  |
| Déposer dans les stocks les plats préparé |  |  |  |  |
|  |  | Modifier l'état des stocks pour ajouter les plats préparé |  |  |
|  |  |  |  | Modifier l'état des stocks pour ajouter les plats préparé |

### Dates mises à jours

- V1 Vendredi 6 février 2026 (création)
- V2 Mercredi 25 février 2026 (Continuation et finision)
- V3 Vendredi 13 mars 2026 (Modificaiton par rapport aux retours du prof)

<!-- 

**Éléments clés :**
- Utiliser des `|` pour séparer les colonnes
- La deuxième ligne doit contenir des tirets `---` pour chaque colonne
- Vous pouvez ajouter `:` pour l'alignement (`:---` gauche, `:---:` centre, `---:` droite)

Exemple avec alignement :
```markdown
| Gauche | Centre | Droite | Normal |
|:-------|:------:|-------:|--------|
| A      | B      | C      | D      |
```
|  |  |  |  |  |

-->