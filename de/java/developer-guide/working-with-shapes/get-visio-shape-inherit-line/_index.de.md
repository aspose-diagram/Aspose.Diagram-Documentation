---
title: Holen Sie sich Visio Shape Inherit Line
type: docs
weight: 100
url: /de/java/get-visio-shape-inherit-line/
description: In diesem Abschnitt wird erläutert, wie Sie den Linienstil der visio-Form erhalten, der von seinem übergeordneten Stil geerbt und mit Aspose.Diagram gemastert wird.
---
### **Rufen Sie geerbte Liniendaten einer Visio-Form ab**
 Die Formen Visio können den übergeordneten Stil und die Masterform erben. Entwickler können die Erbliniendaten einer Visio-Form abrufen oder festlegen. Die InheritLine-Eigenschaft, verfügbar gemacht durch die[Form](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) Klasse, enthält die Linienformatierungswerte für die Form, die vom übergeordneten Stil und der Masterform geerbt wird.
#### **Programmierbeispiel für geerbte Leitungsdaten abrufen**
Der folgende Codeausschnitt ruft die geerbten Liniendaten der Form ab. Bitte überprüfen Sie diesen Beispielcode:


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getSharedDataDir(RetrieveInheritedLine.class) + "Shapes/";

// Call the diagram constructor to load a VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get page by ID
Page page = diagram.getPages().getPage("Page-1");
// Get shape by ID
Shape shape = page.getShapes().getShape(1);
//Get Inherit Line from the parent style and master
Line line = shape.getInheritLine();
// Get the line formatting values
System.out.println(line.getBeginArrow().getValue());
System.out.println(line.getBeginArrowSize().getValue());
System.out.println(line.getEndArrow().getValue());
System.out.println(line.getEndArrowSize().getValue());
System.out.println(line.getLineColor().getValue());
System.out.println(line.getLinePattern().getValue());
System.out.println(line.getLineWeight().getValue());
System.out.println(line.getRounding().getValue());

{{< /highlight >}}


