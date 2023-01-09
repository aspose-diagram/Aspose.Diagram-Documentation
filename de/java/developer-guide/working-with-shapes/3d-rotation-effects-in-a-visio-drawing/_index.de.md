---
title: 3D-Rotationseffekte in einer Visio-Zeichnung
type: docs
weight: 90
url: /de/java/3d-rotation-effects-in-a-visio-drawing/
---
## **Legen Sie die 3D-Rotationseigenschaften in Shapesheet fest**
Aspose.Diagram for Java API ermöglicht es Entwicklern, 3D-Rotationswerte im Shapesheet zu ändern. Die Zellenwerte RotationXAngle, RotationYAngle und RotationZAngle steuern den Rotationsgrad in jeder der entsprechenden Achsen. Der Aufzählungswert von RotationType steuert den Rotationstyp:

1. Parallele Drehung, bei der die Form gedreht wird, ohne die lineare Perspektive zu berücksichtigen.
1. Perspektivische Drehung, bei der die Form mit linearer Perspektive gedreht wird.
1. Voreinstellungen für schräge Rotation (unten links, unten rechts, oben links und oben rechts), bei denen die Form mit schräger Projektion gedreht wird.

Das**KeepTextFlat**Der Zellenwert gibt an, ob der Text einer Form die Drehung der Form in 3D ignoriert. Es gilt nicht für die 2D-Rotation. Das**DistanzVomBoden**Der Zellenwert bestimmt den Abstand, um den das Objekt in den Punkten vom Boden angehoben wird, wenn es in 3D gedreht wird. Das**Perspektive**Der Zellenwert bestimmt den Perspektivenwinkel für eine perspektivische Drehung in Grad (0 bis 359,9).
### **Legen Sie die 3D-Rotationseigenschaften fest**
Das ThreeDFormat-Member, das von der verfügbar gemacht wird[Form](https://reference.aspose.com/diagram/java/com.aspose.diagram/Shape)-Klasse kann zum Festlegen von 3D-Rotationseigenschaften verwendet werden.

Der folgende Code zeigt, wie man:

1. Laden Sie eine Quellzeichnung.
1. Rufen Sie eine Form nach Seitenname und ID-Parametern ab.
1. Legen Sie die 3D-Rotationseigenschaften fest.
1. Zeichnung speichern
#### **Programmierbeispiel für 3D-Rotation**
Verwenden Sie den folgenden Code in Ihrer Java-Anwendung, um 3D-Rotationseigenschaften mit Aspose.Diagram for Java API festzulegen.

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
