---
title: Obtenga la forma Visio, incluido el niño
type: docs
weight: 110
url: /es/net/get-visio-shape-including-child/
description: Esta sección explica cómo obtener la forma visio, incluido el niño con la identificación o el nombre de la forma con Aspose.Diagram.
---
### **Recuperar una forma Visio que incluye niño**
Cada forma en un diagram tiene una identificación y un nombre. El ID es importante al programar con Visio: es el método principal para acceder a una forma. Cada forma también retiene información sobre de qué maestro (plantilla) está hecha.

 A[Forma](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) es un objeto en un dibujo Visio que posiblemente tenga un padre o hijos. La propiedad Shapes, expuesta por la clase Page, admite una colección de objetos Aspose.Diagram.Shape. La propiedad Shapes se puede utilizar para recuperar información sobre una forma.
#### **Recuperar Visio Muestra de programación de forma**
El siguiente fragmento de código recupera la forma, incluido el niño. Por favor revise este código de muestra:


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load a Visio diagram
Diagram diagram = new Diagram(dataDir + "NetworkConnection.vsdx");

Page page = diagram.Pages[0];

Shape shapeContainerChild = page.Shapes.GetShapeIncludingChild("RectangleChild");

if (shapeContainerChild == null)
    throw new Exception();
    
// Save visio diagram
diagram.Save(dataDir + "GroupShapes_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}


