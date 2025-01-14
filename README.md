# SequenceToCode

Ce dépôt a été publié à des fins pédagogiques.

## Intention pédagogique

Dans la continuité du laboratoire ["SequenceToCode"](https://github.com/CPNV-ES-UML1/SequenceToCode), il vous est demandé dans cette évaluation de continuer le développement.

## Objectifs opérationnels

Chaque technicien atteindra les objectifs suivants en réalisant ce laboratoire:

- [ ] Analyser un diagramme de séquence connu et identifer les nouveautés à implémenter.
- [ ] Mettre à jour l'architecture (diagramme de classe) minimale pour pouvoir réaliser la séquence.
- [ ] Coder la séquence dans le langage de son choix.
- [ ] Appliquer les pratiques de "git-flow".
- [ ] Réalisez un fork de ce dépôt.
- [ ] Appliquer la structure suivante à votre dépôt:

  ```
  <yourProject>
  ├───docs   [contiendra le diagramme de classes]
  └───src    [contiendra le code produit]
  .gitignore [selon votre langage de programmation]
  README.md  [ne sera pas évalué. Placé simplement un fichier avec le titre de votre dépôt.]
  ```

## Context métier

Actuellement l'entreprise peut attribuer un chauffeur à un véhicule, pour autant que l'un est l'autre existent et que le chauffeur ne soit pas déjà assigné à un véhicule.

Dans cette étape de développement, nous désirons permettre à l'entreprise de réaliser du transport de matières dangereuses par camion.

Les 4 cas suivants doivent être pris en compte:
* le chauffeur dispose d'une licence spéciale pour ce type de transport et le camion est homologué en conséquence.
* puis l

## Point de départ

* Voici le diagramme de séquence à étudier (en deux partie):

![image](https://github.com/user-attachments/assets/b814f79a-4484-43d8-8b39-ebb0c0b59de9)

![image](https://github.com/user-attachments/assets/811afc58-a12d-4ded-9065-45db790623f0)

* Les informations complémentaires à prendre en compte:
   - [ ] La séquence est identique à celle validée en classe avec en plus:
      * la possiblité d'utiliser un TruckDriver et un Truck (Aide : à déclarer "en dure" directement dans "Enterprise")
      * l'exception initialement levée "VehicleAlreadyAssignedException" a été renommée en "DriverNotAvailableException".
   - [ ] La classe TruckDriver:
      * hérite de la classe Driver.
      * TruckDriver implémente en plus une propriété permettant de connaître la date d'expiration de la licence spécifique pour le transport de matières dangereuses.
      * Cette date sera comparée avec la date du jour. Il faut -a minima- que la licence soit encore valable aujourd'hui pour autoriser l'assignation du chauffeur à cette livraison.
   - [ ] La classe Truck:
      * hérite de la classe Vehicle.
      * Truck implémente en plus une propriété permettant de connaître si le camion en question est homologué pour le transport de matières dangereuses.

* Hiérachie des exceptions
  - [ ] En observant le diagramme de séquence, déduisez la hiérachie des exceptions.

## Livraison

* Le livrable final est réalisé **sur votre dépôt forké** sur une branche de type [release 1.1.0](https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow) au sens gitflow (et non github).
* Les commits respectent les bonnes pratiques du [conventional commit](https://www.conventionalcommits.org/en/v1.0.0/).
* Une issue est adressée à votre enseignant (adresse email du cpnv) et contient le commit à étudier.
