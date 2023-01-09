---
title: Effets de rotation 3D dans un dessin Visio
type: docs
weight: 90
url: /fr/net/3d-rotation-effects-in-a-visio-drawing/
description: Cette section explique comment définir les propriétés de rotation 3D dans Shapesheet avec Aspose.Diagram.
---
## **Définir les propriétés de rotation 3D dans Shapesheet**
Aspose.Diagram API permet aux développeurs de modifier les valeurs de rotation 3D dans la feuille de formes. Les valeurs des cellules RotationXAngle, RotationYAngle et RotationZAngle contrôlent le degré de rotation de chacun des axes respectifs. La valeur enum de RotationType contrôle le type de rotation :

1. Rotation parallèle, où la forme est tournée sans tenir compte de la perspective linéaire.
1. Rotation de perspective, où la forme est pivotée avec une perspective linéaire.
1. Préréglages de rotation oblique (en bas à gauche, en bas à droite, en haut à gauche et en haut à droite), où la forme est tournée avec une projection oblique.

 La**KeepTextFlat** La valeur de la cellule indique si le texte d'une forme ignorera la rotation de la forme en 3D. Elle ne s'applique pas à la rotation 2D. La**DistanceFromGround** la valeur de la cellule détermine la distance à laquelle l'objet est soulevé du sol dans les points lors de la rotation en 3D. La**Perspective** La valeur de la cellule détermine l'angle de perspective pour une rotation de perspective, en degrés (0 à 359,9).
### **Définir les propriétés de rotation 3D**
 Le membre ThreeDFormat exposé par le[Forme](https://reference.aspose.com/diagram/net/aspose.diagram/shape)La classe peut être utilisée pour définir les propriétés de rotation 3D.

Le code ci-dessous montre comment :

1. Charger un dessin source.
1. Récupérer une forme par nom de page et paramètres d'ID.
1. Définissez les propriétés de rotation 3D.
1. Enregistrer le dessin
#### **Exemple de programmation de rotation 3D**
Utilisez le code suivant dans votre application .NET pour définir les propriétés de rotation 3D à l'aide de Aspose.Diagram for .NET API.

**.NET, C#**

{{< highlight "java" >}}

 // load diagram

Diagram diagram = new Diagram(@"c:\temp\TestTemplate.vsdx");

// get shape by ID and page name

Shape shape = diagram.Pages.GetPage("Page-1").Shapes.GetShape(0);



// set 3D rotation properties

shape.ThreeDFormat.RotationXAngle.Value = 2.61;

shape.ThreeDFormat.RotationYAngle.Value = 2.61;

shape.ThreeDFormat.RotationZAngle.Value = 3;

shape.ThreeDFormat.RotationType.Value = RotationTypeValue.ObliqueFromBottomLeft;

shape.ThreeDFormat.Perspective.Value = 0;

shape.ThreeDFormat.DistanceFromGround.Value = 0;

shape.ThreeDFormat.KeepTextFlat.Value = BOOL.True;

// save drawing

diagram.Save(@"c:\temp\TestTemplate.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
