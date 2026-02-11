---
title: Holen Sie sich Visio Shape Inherit Fill
type: docs
weight: 100
url: /de/java/get-visio-shape-inherit-fill/
description: In diesem Abschnitt wird erläutert, wie Sie den Füllstil der visio-Form erhalten, der vom übergeordneten Stil geerbt und mit Aspose.Diagram gemastert wird.
---
### **Rufen Sie geerbte Fülldaten einer Visio-Form ab**
Die Formen Visio können den übergeordneten Stil und die Masterform erben. Entwickler erhalten möglicherweise die vererbten Fülldaten einer Visio-Form. Die InheritFill-Eigenschaft, verfügbar gemacht durch die[Form](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) Klasse, enthält die Füllformatierungswerte für die Form, die vom übergeordneten Stil und der Masterform geerbt wird.
#### **Programmierbeispiel für geerbte Fülldaten abrufen**
Der folgende Codeausschnitt ruft die geerbten Fülldaten der Form ab. Bitte überprüfen Sie diesen Beispielcode:

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getSharedDataDir(RetrieveInheritedFillData.class) + "Shapes/";

// Call the diagram constructor to load a VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get page by ID
Page page = diagram.getPages().getPage("Page-1");
// Get shape by ID
Shape shape = page.getShapes().getShape(1);
// Get the fill formatting values
System.out.println(shape.getInheritFill().getFillBkgnd().getValue());
System.out.println(shape.getInheritFill().getFillForegnd().getValue());
System.out.println(shape.getInheritFill().getFillPattern().getValue());
System.out.println(shape.getInheritFill().getShapeShdwObliqueAngle().getValue());
System.out.println(shape.getInheritFill().getShapeShdwOffsetX().getValue());
System.out.println(shape.getInheritFill().getShapeShdwOffsetY().getValue());
System.out.println(shape.getInheritFill().getShapeShdwScaleFactor().getValue());
System.out.println(shape.getInheritFill().getShapeShdwType().getValue());
System.out.println(shape.getInheritFill().getShdwBkgnd().getValue());
System.out.println(shape.getInheritFill().getShdwBkgndTrans().getValue());
System.out.println(shape.getInheritFill().getShdwForegnd().getValue());
System.out.println(shape.getInheritFill().getShdwForegndTrans().getValue());
System.out.println(shape.getInheritFill().getShdwPattern().getValue());

{{< /highlight >}}
```

