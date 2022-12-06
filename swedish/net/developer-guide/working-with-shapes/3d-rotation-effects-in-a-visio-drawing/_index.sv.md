---
title: 3D-rotationseffekter i en Visio-ritning
type: docs
weight: 90
url: /sv/net/3d-rotation-effects-in-a-visio-drawing/
description: Det här avsnittet förklarar hur du ställer in 3D-rotationsegenskaper i Shapesheet med Aspose.Diagram.
---
## **Ställ in 3D-rotationsegenskaper i Shapesheet**
Aspose.Diagram API tillåter utvecklare att ändra 3D-rotationsvärden i formbladet. Cellvärdena RotationXAngle, RotationYAngle och RotationZAngle styr graden av rotation i var och en av respektive axlar. Rotationstypens enumvärde styr rotationstypen:

1. Parallellrotation, där formen roteras utan att ta hänsyn till linjärt perspektiv.
1. Perspektivrotation, där formen roteras med linjärt perspektiv.
1. Förinställningar för sned rotation (nederst till vänster, längst ner till höger, uppe till vänster och uppe till höger), där formen roteras med sned projektion.

 De**KeepTextFlat** cellvärde indikerar om en forms text kommer att ignorera formens rotation i 3D. Det gäller inte för 2D-rotation. De**Avstånd från marken** cellvärdet bestämmer avståndet objektet lyfts från marken i punkterna när det roteras i 3D. De**Perspektiv** cellvärdet bestämmer perspektivvinkeln för en perspektivrotation, i grader (0 till 359,9).
### **Ställ in 3D-rotationsegenskaper**
 ThreeDFormat-medlemmen exponerad av[Form](https://reference.aspose.com/diagram/net/aspose.diagram/shape)klass kan användas för att ställa in 3d-rotationsegenskaper.

Koden nedan visar hur man:

1. Ladda en källritning.
1. Hämta en form efter sidnamn och ID-parametrar.
1. Ställ in 3D-rotationsegenskaper.
1. Spara ritningen
#### **3D-rotationsprogrammeringsexempel**
Använd följande kod i din .NET-applikation för att ställa in 3D-rotationsegenskaper med Aspose.Diagram for .NET API.

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
