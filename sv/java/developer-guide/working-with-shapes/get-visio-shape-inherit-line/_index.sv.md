---
title: Skaffa Visio Shape Inherit Line
type: docs
weight: 100
url: /sv/java/get-visio-shape-inherit-line/
description: Det här avsnittet förklarar hur du får visio-formens linjestil ärvd från dess överordnade stil och master med Aspose.Diagram.
---
### **Hämta ärvd linjedata från en Visio-form**
 Visio-formerna kan ärva den överordnade stilen och huvudformen. Utvecklare kan hämta eller ställa in ärvningslinjedata för en Visio-form. Egenskapen InheritLine, exponerad av[Form](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) klass, innehåller linjeformateringsvärdena för formen som ärvs av den överordnade stilen och huvudformen.
#### **Hämta ärvt linjedataprogrammeringsexempel**
Följande kodavsnitt hämtar formens ärvda linjedata. Kontrollera denna exempelkod:

```
{{< highlight "java" >}}
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
```

