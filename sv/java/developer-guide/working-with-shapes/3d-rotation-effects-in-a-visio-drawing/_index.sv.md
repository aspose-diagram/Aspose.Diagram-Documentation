---
title: 3D-rotationseffekter i en Visio-ritning
type: docs
weight: 90
url: /sv/java/3d-rotation-effects-in-a-visio-drawing/
---
## **Ställ in 3D-rotationsegenskaper i Shapesheet**
Aspose.Diagram for Java API tillåter utvecklare att ändra 3D-rotationsvärden i formarket. Cellvärdena RotationXAngle, RotationYAngle och RotationZAngle styr graden av rotation i var och en av respektive axlar. Rotationstypens enumvärde styr rotationstypen:

1. Parallellrotation, där formen roteras utan att ta hänsyn till linjärt perspektiv.
1. Perspektivrotation, där formen roteras med linjärt perspektiv.
1. Förinställningar för sned rotation (nederst till vänster, längst ner till höger, uppe till vänster och uppe till höger), där formen roteras med sned projektion.

De**KeepTextFlat**cellvärde indikerar om en forms text kommer att ignorera formens rotation i 3D. Det gäller inte för 2D-rotation. De**Avstånd från marken**cellvärdet bestämmer avståndet objektet lyfts från marken i punkterna när det roteras i 3D. De**Perspektiv**cellvärdet bestämmer perspektivvinkeln för en perspektivrotation, i grader (0 till 359,9).
### **Ställ in 3D-rotationsegenskaper**
ThreeDFormat-medlemmen exponerad av[Form](https://reference.aspose.com/diagram/java/com.aspose.diagram/Shape)klass kan användas för att ställa in 3d-rotationsegenskaper.

Koden nedan visar hur man:

1. Ladda en källritning.
1. Hämta en form efter sidnamn och ID-parametrar.
1. Ställ in 3D-rotationsegenskaper.
1. Spara ritningen
#### **3D-rotationsprogrammeringsexempel**
Använd följande kod i din Java-applikation för att ställa in 3D-rotationsegenskaper med Aspose.Diagram for Java API.

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
