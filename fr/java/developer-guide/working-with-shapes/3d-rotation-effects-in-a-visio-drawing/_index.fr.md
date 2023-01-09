---
title: Effets de rotation 3D dans un dessin Visio
type: docs
weight: 90
url: /fr/java/3d-rotation-effects-in-a-visio-drawing/
---
## **Définir les propriétés de rotation 3D dans Shapesheet**
Aspose.Diagram for Java API permet aux développeurs de modifier les valeurs de rotation 3D dans la feuille de formes. Les valeurs des cellules RotationXAngle, RotationYAngle et RotationZAngle contrôlent le degré de rotation de chacun des axes respectifs. La valeur enum de RotationType contrôle le type de rotation :

1. Rotation parallèle, où la forme est tournée sans tenir compte de la perspective linéaire.
1. Rotation de perspective, où la forme est pivotée avec une perspective linéaire.
1. Préréglages de rotation oblique (en bas à gauche, en bas à droite, en haut à gauche et en haut à droite), où la forme est tournée avec une projection oblique.

La**KeepTextFlat**La valeur de la cellule indique si le texte d'une forme ignorera la rotation de la forme en 3D. Elle ne s'applique pas à la rotation 2D. La**DistanceFromGround**la valeur de la cellule détermine la distance à laquelle l'objet est soulevé du sol dans les points lors de la rotation en 3D. La**Perspective**La valeur de la cellule détermine l'angle de perspective pour une rotation de perspective, en degrés (0 à 359,9).
### **Définir les propriétés de rotation 3D**
Le membre ThreeDFormat exposé par le[Forme](https://reference.aspose.com/diagram/java/com.aspose.diagram/Shape)La classe peut être utilisée pour définir les propriétés de rotation 3D.

Le code ci-dessous montre comment :

1. Charger un dessin source.
1. Récupérer une forme par nom de page et paramètres d'ID.
1. Définissez les propriétés de rotation 3D.
1. Enregistrer le dessin
#### **Exemple de programmation de rotation 3D**
Utilisez le code suivant dans votre application Java pour définir les propriétés de rotation 3D à l'aide de Aspose.Diagram for Java API.

**Java**

{{< highlight "java" >}}

 // load diagram

Diagram diagram = new Diagram("c:\\temp\\TestTemplate.vsdx");

// get shape by ID and page name

Shape shape = diagram.getPages().getPage("Page-1").getShapes().getShape(0);



// set 3D rotation properties

shape.getThreeDFormat().getRotationXAngle().setValue(2.61);

shape.getThreeDFormat().getRotationYAngle().setValue(2.61);

shape.getThreeDFormat().getRotationZAngle().setValue(3);

shape.getThreeDFormat().getRotationType().setValue(RotationTypeValue.PARALLEL);

shape.getThreeDFormat().getPerspective().setValue(0);

shape.getThreeDFormat().getDistanceFromGround().setValue(0);

shape.getThreeDFormat().getKeepTextFlat().setValue(BOOL.TRUE);

// save drawing

diagram.save("c:\\temp\\TestTemplate.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
