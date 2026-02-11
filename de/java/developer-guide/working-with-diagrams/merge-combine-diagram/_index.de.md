---
title: Kombinieren Sie Diagram
type: docs
weight: 30
url: /de/java/merge-combine-diagram/
description: In diesem Abschnitt wird erläutert, wie die Datei visio kombiniert wird
---
## **Mögliche Nutzungsszenarien**

 Mit Aspose.Diagram können Sie zwei visio-Dateien zu einer kombinieren.
 Aspose.Diagram for Java API hat die[Diagram](http://www.aspose.com/api/java/diagram/com.aspose.diagram/diagram) Klasse, die eine Visio-Zeichnung darstellt.
Mit der Methode[**Kombinieren**](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram#combine(com.aspose.diagram.Diagram) ) in[Diagram](http://www.aspose.com/api/java/diagram/com.aspose.diagram/diagram) Klasse zum Kombinieren von Diagrammen.

## **Beispielcode**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(CombineDiagram.class);

// Load a Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Load another Visio diagram
Diagram diagram2 = new Diagram(dataDir + Drawing2.vsdx");

diagram2.combine(diagram);

// save in the VSDX format
diagram.save(dataDir + "CombineDiagram_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
