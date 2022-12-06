---
title: Travailler avec des formes
type: docs
weight: 40
url: /fr/net/working-with-shapes-gluing/
description: Cette section explique comment obtenir des formes collées à une forme particulière avec Aspose.Diagram.
---
## **Obtenez les connecteurs collés à une forme particulière**
[Ajouter et connecter des formes Visio](https://docs.aspose.com/diagram/net/add-retrieve-copy-and-read-visio-shape-data/) explique comment ajouter une forme et la relier à d'autres formes dans les schémas Microsoft Visio en utilisant Aspose.Diagram for .NET. Il est également possible de trouver des connecteurs qui sont collés à cette forme.
### **Obtenir des formes collées**
 La méthode GluedShapes exposée par le[Forme](http://www.aspose.com/api/net/diagram/aspose.diagram/shape)peut être utilisée pour obtenir une liste des ID de tous les connecteurs collés à une forme ou, si la forme en question est un connecteur, les ID des formes auxquelles il est connecté. La méthode GetShape, exposée par la[ShapeCollection](http://www.aspose.com/api/net/diagram/aspose.diagram/shapecollection) class, peut ensuite être utilisé pour trouver une forme par son ID.

Le code ci-dessous montre comment :

1. Chargez un exemple de fichier.
1. Accéder à une forme particulière.
1. Obtenez une liste des identifiants de tous les connecteurs collés à cette forme.
#### **Obtenez un exemple de programmation collée sur les connecteurs**
Utilisez le code suivant dans votre application .NET pour trouver tous les connecteurs collés à une forme en utilisant Aspose.Diagram for .NET.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-Working-with-Shapes-Gluing-GetGluedConnectors-GetGluedConnectors.cs" >}}
## **Collez les formes Visio avec le point de connexion**
Aspose.Diagram for .NET permet aux développeurs de coller des formes ensemble à travers les points de connexion.
### **Formes de colle**
 La méthode GlueShapes exposée par le[Page](http://www.aspose.com/api/net/diagram/aspose.diagram/page) classe peut être utilisée.

|<p>**Entrée diagram** </p><p>![tâche : image_autre_texte](working-with-shapes-gluing_1.png)</p>|<p>**Le diagram après collage des formes** </p><p>![tâche : image_autre_texte](working-with-shapes-gluing_2.png)</p>|
|:- |:- |
Le code ci-dessous montre comment :

1. Chargez un exemple de fichier.
1. Formes de colle.
1. Enregistrez le diagram.
#### **Colle Visio Exemple de programmation de formes**
Utilisez le code suivant dans votre application .NET pour coller des formes à travers les points de connexion :

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-Working-with-Shapes-Gluing-GlueVisioShapes-GlueVisioShapes.cs" >}}
## **Formes de colle à l'intérieur du conteneur**
Aspose.Diagram for .NET permet aux développeurs de coller des formes de groupe à l'intérieur d'un conteneur.
### **Forme du groupe de collage**
 La méthode GlueShapesInContainer exposée par le[Page](http://www.aspose.com/api/net/diagram/aspose.diagram/page) classe peut être utilisée.

|<p>**Entrée diagram** </p><p>![tâche : image_autre_texte](working-with-shapes-gluing_3.png)</p>|<p>**Le diagram après collage des formes de groupe** </p><p>![tâche : image_autre_texte](working-with-shapes-gluing_4.png)</p>|
|:- |:- |
Le code ci-dessous montre comment :

1. Chargez un exemple de fichier.
1. Formes de groupe de colle.
1. Enregistrez le diagram.
#### **Coller des formes à l'intérieur d'un exemple de programmation**
Utilisez le code suivant dans votre application .NET pour coller la forme du groupe à l'intérieur d'un conteneur :

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-Working-with-Shapes-Gluing-GlueContainerShape-GlueContainerShape.cs" >}}
