---
title: Erhalten Sie Visio Form einschließlich Kind
type: docs
weight: 110
url: /de/net/get-visio-shape-including-child/
description: In diesem Abschnitt wird erläutert, wie Sie die Form visio einschließlich des Kindes mit der ID oder dem Namen der Form mit Aspose.Diagram erhalten.
---
### **Rufen Sie eine Visio-Form einschließlich Kind ab**
Jede Form in einem diagram hat eine ID und einen Namen. Die ID ist beim Programmieren mit Visio wichtig: Sie ist die Hauptmethode für den Zugriff auf eine Form. Jede Form enthält auch Informationen darüber, aus welchem Master (Schablone) sie besteht.

 EIN[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) ist ein Objekt in einer Visio Zeichnung, das möglicherweise einen Vater oder Söhne hat. Die Shapes-Eigenschaft, die von der Page-Klasse verfügbar gemacht wird, unterstützt eine Sammlung von Aspose.Diagram.Shape-Objekten. Die Shapes-Eigenschaft kann verwendet werden, um Informationen zu einer Form abzurufen.
#### **Rufen Sie Visio Shape-Programmierbeispiel ab**
Das folgende Code-Snippet ruft die Form einschließlich des untergeordneten Elements ab. Bitte überprüfen Sie diesen Beispielcode:


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


