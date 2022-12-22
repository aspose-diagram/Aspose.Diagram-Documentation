﻿---
title: Faire pivoter, modifier la position et connecter les sous-formes
type: docs
weight: 60
url: /fr/java/rotate-change-the-position-and-connect-sub-shapes/
---
## **Faire pivoter une forme avec un angle approprié**
 Aspose.Diagram for Java vous permet de faire pivoter une forme à n'importe quel angle. La méthode SetAngle exposée par le[Forme](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) La classe peut être utilisée pour faire pivoter une forme à n'importe quel angle souhaité. Il prend un seul paramètre comme angle.
### **Faire pivoter un échantillon de programmation de forme**
Utilisez le code suivant dans votre application Java pour faire pivoter une forme à l'aide de Aspose.Diagram for Java.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-RotateVisioShape-RotateVisioShape.java" >}}
## **Modifier la position d'une forme**
La classe Shape vous permet de modifier la position d'une forme. La ligne de connexion s'ajuste automatiquement lorsque la forme est déplacée vers une position différente.

Les méthodes Move et MoveTo, exposées par la classe Shape, prennent en charge la modification de la position d'une forme en tant que partie d'un groupe ou non.
Les exemples de code de cet article déplacent une forme sur la page.
**Entrée diagram** 

![tâche : image_autre_texte](http://i.imgur.com/cThgWnB.png)


**Le diagram après le déplacement de la forme** 

![tâche : image_autre_texte](http://i.imgur.com/Q3QByqe.png)

Le processus de déplacement d'une forme est le suivant :

1. Charger un diagram.
1. Trouvez une forme particulière.
1. Déplacer la forme vers un autre emplacement
1. Enregistrez le diagram.
### **Exemple de programmation de changement de position**
L'extrait de code ci-dessous montre comment déplacer la forme. Le code récupère une page Visio par nom et forme par ID 16, et déplace sa position.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-MoveVisioShape-MoveVisioShape.java" >}}
## **Connecter les sous-formes des groupes**
Cette rubrique explique comment connecter deux sous-formes de deux formes de groupe différentes dans des diagrammes Microsoft Visio à l'aide de Aspose.Diagram for Java.

 La méthode ConnectShapesViaConnector exposée par le[Page](https://reference.aspose.com/diagram/java/com.aspose.diagram/page) class peut être utilisé pour connecter les formes par leurs identifiants. La méthode AddShape, exposée par le[Diagram](https://reference.aspose.com/diagram/java)class, peut être utilisé pour ajouter une forme.

|<p>**L'entrée diagram** </p><p>![tâche : image_autre_texte](http://i.imgur.com/74rDby5.png)</p>|<p>**Le diagram après la connexion des sous-formes** </p><p>![tâche : image_autre_texte](http://i.imgur.com/c387dZJ.png)</p>|
|:- |:- |
Le code ci-dessous montre comment :

1. Chargez un exemple de fichier.
1. Accéder à une page particulière.
1. Ajouter une forme de connecteur dynamique à la page sélectionnée.
1. Connecter les sous-formes
### **Connecter les sous-formes Exemple de programmation**
Utilisez le code suivant dans votre application Java pour connecter les sous-formes de deux formes de groupe différentes à l'aide de Aspose.Diagram for Java.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-ConnectVisioSubShapes-ConnectVisioSubShapes.java" >}}
## **Obtenir les formes connectées à une forme particulière**
[Ajouter et connecter des formes Visio](/diagram/fr/java/add-and-connect-visio-shapes/) explique comment ajouter une forme et la connecter à d'autres formes dans les diagrammes Microsoft Visio en utilisant Aspose.Diagram for Java. Il est également possible de trouver des formes qui sont connectées à une forme spécifique.

 La méthode ConnectedShapes exposée par le[Forme](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) class peut être utilisé pour obtenir les identifiants des formes connectées à une forme. La méthode GetShape, exposée par le[ShapeCollection](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/shapecollection) class, peut ensuite être utilisé pour trouver une forme par son ID.

Le code ci-dessous montre comment :

1. Chargez un exemple de fichier.
1. Accéder à une forme particulière.
1. Obtenez les noms de toutes les formes connectées à la forme sélectionnée.
### **Obtenir un exemple de programmation de formes**
Utilisez le code suivant dans votre application Java pour trouver toutes les formes connectées à une forme spécifique en utilisant Aspose.Diagram for Java.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-GetAllConnectedShapes-GetAllConnectedShapes.java" >}}
