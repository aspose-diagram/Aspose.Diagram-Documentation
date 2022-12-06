---
title: Faire pivoter, modifier la position et connecter les sous-formes
type: docs
weight: 30
url: /fr/net/rotate-change-the-position-and-connect-sub-shapes/
description: Cette section explique comment faire pivoter une forme visio avec Aspose.Diagram.
---
## **Faire pivoter une forme avec un angle approprié**
 Aspose.Diagram for .NET vous permet de faire pivoter une forme à n'importe quel angle. La méthode SetAngle exposée par le[Forme](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) La classe peut être utilisée pour faire pivoter une forme à n'importe quel angle souhaité. Il prend un seul paramètre comme angle.
### **Faire pivoter un échantillon de programmation de forme**
Utilisez le code suivant dans votre application .NET pour faire pivoter une forme à l'aide de Aspose.Diagram for .NET.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-RotateVisioShape-RotateVisioShape.cs" >}}
## **Modifier la position d'une forme**
 La[Forme](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) La classe vous permet de changer la position d'une forme. La ligne de connexion s'ajuste automatiquement lorsque la forme est déplacée vers une position différente. Les méthodes Move et MoveTo, exposées par le[Forme](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) classe, prend en charge la modification de la position d'une forme en tant que partie d'un groupe ou non. Les exemples de code de cet article déplacent une forme sur la page.

Le processus de déplacement d'une forme est le suivant :

1. Charger un diagram.
1. Trouvez une forme particulière.
1. Déplacer la forme vers un autre emplacement
1. Enregistrez le diagram.
### **Exemple de programmation de changement de position**
L'extrait de code ci-dessous montre comment déplacer la forme. Le code récupère une page Visio par nom et forme par ID 16, et déplace sa position.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-MoveVisioShape-MoveVisioShape.cs" >}}
## **Connecter les sous-formes des groupes**
 Cette rubrique explique comment connecter deux sous-formes de deux formes de groupe différentes dans des diagrammes Microsoft Visio à l'aide de Aspose.Diagram for .NET. La méthode ConnectShapesViaConnector exposée par le[Page](http://www.aspose.com/api/net/diagram/aspose.diagram/page) class peut être utilisé pour connecter les formes par leurs identifiants. La méthode AddShape, exposée par le[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram)class, peut être utilisé pour ajouter une forme.

Le code ci-dessous montre comment :

1. Chargez un exemple de fichier.
1. Accéder à une page particulière.
1. Ajouter une forme de connecteur dynamique à la page sélectionnée.
1. Connecter les sous-formes
### **Connecter les sous-formes Exemple de programmation**
Utilisez le code suivant dans votre application .NET pour connecter les sous-formes de deux formes de groupe différentes à l'aide de Aspose.Diagram for .NET.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-ConnectVisioSubShapes-ConnectVisioSubShapes.cs" >}}
## **Obtenir les formes connectées à une forme particulière**
[Ajouter et connecter des formes Visio](https://docs.aspose.com/diagram/net/add-retrieve-copy-and-read-visio-shape-data/) explique comment ajouter une forme et la connecter à d'autres formes dans les diagrammes Microsoft Visio en utilisant Aspose.Diagram for .NET. Il est également possible de trouver des formes qui sont connectées à une forme spécifique.

 La méthode ConnectedShapes exposée par le[Forme](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class peut être utilisé pour obtenir les identifiants des formes connectées à une forme. La méthode GetShape, exposée par le[ShapeCollection](http://www.aspose.com/api/net/diagram/aspose.diagram/shapecollection) class, peut ensuite être utilisé pour trouver une forme par son ID.

Le code ci-dessous montre comment :

1. Chargez un exemple de fichier.
1. Accéder à une forme particulière.
1. Obtenez les noms de toutes les formes connectées à la forme sélectionnée.
### **Obtenir un exemple de programmation de formes**
Utilisez le code suivant dans votre application .NET pour trouver toutes les formes connectées à une forme spécifique en utilisant Aspose.Diagram for .NET.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-GetAllConnectedShapes-GetAllConnectedShapes.cs" >}}
