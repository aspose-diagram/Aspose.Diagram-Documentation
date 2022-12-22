---
title: Travailler avec des formes
type: docs
weight: 10
url: /fr/java/working-with-shapes-gluing/
---
## **Obtenez les connecteurs collés à une forme particulière**
[Ajouter et connecter des formes Visio](/diagram/fr/java/add-and-connect-visio-shapes/) explique comment ajouter une forme et la relier à d'autres formes dans les schémas Microsoft Visio en utilisant Aspose.Diagram for Java. Il est également possible de trouver des connecteurs qui sont collés à cette forme.
### **Obtenir des formes collées**
 La méthode GluedShapes exposée par le[Forme](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape)peut être utilisée pour obtenir une liste des ID de tous les connecteurs collés à une forme ou, si la forme en question est un connecteur, les ID des formes auxquelles il est connecté. La méthode GetShape, exposée par la[ShapeCollection](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/shapecollection) class, peut ensuite être utilisé pour trouver une forme par son ID.

Le code ci-dessous montre comment :

1. Chargez un exemple de fichier.
1. Accéder à une forme particulière.
1. Obtenez une liste des identifiants de tous les connecteurs collés à cette forme.
#### **Obtenez un exemple de programmation collée sur les connecteurs**
Utilisez le code suivant dans votre application Java pour trouver tous les connecteurs collés à une forme en utilisant Aspose.Diagram for Java.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-Glue-GetGluedConnectors-GetGluedConnectors.java" >}}
## **Collez les formes Visio avec le point de connexion**
Aspose.Diagram for Java permet aux développeurs de coller des formes ensemble à travers les points de connexion.
### **Formes de colle**
 La méthode GlueShapes exposée par le[Page](https://reference.aspose.com/diagram/java/com.aspose.diagram/page) classe peut être utilisée.

|<p>**Entrée diagram** </p><p>![tâche : image_autre_texte](http://i.imgur.com/Z69f4hg.png)</p>|<p>**Le diagram après collage des formes** </p><p>![tâche : image_autre_texte](http://i.imgur.com/5TJpDwc.png)</p>|
|:- |:- |
Le code ci-dessous montre comment :

1. Chargez un exemple de fichier.
1. Formes de colle.
1. Enregistrez le diagram.
#### **Colle Visio Exemple de programmation de formes**
Utilisez le code suivant dans votre application Java pour coller des formes à travers les points de connexion :

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-Glue-GlueVisioShapes-GlueVisioShapes.java" >}}
## **Formes de colle à l'intérieur du conteneur**
Aspose.Diagram for Java permet aux développeurs de coller des formes de groupe à l'intérieur d'un conteneur.
### **Forme du groupe de collage**
La méthode GlueShapesInContainer exposée par la classe Page peut être utilisée.

|<p>**Entrée diagram** </p><p>![tâche : image_autre_texte](http://i.imgur.com/HRRzIEh.png)</p>|<p>**Le diagram après collage des formes de groupe** </p><p>![tâche : image_autre_texte](http://i.imgur.com/YxCiOgU.png)</p>|
|:- |:- |
Le code ci-dessous montre comment :

1. Chargez un exemple de fichier.
1. Formes de groupe de colle.
1. Enregistrez le diagram.
#### **Coller des formes à l'intérieur d'un exemple de programmation**
Utilisez le code suivant dans votre application Java pour coller la forme du groupe à l'intérieur d'un conteneur :

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-Glue-GlueContainerShape-GlueContainerShape.java" >}}
