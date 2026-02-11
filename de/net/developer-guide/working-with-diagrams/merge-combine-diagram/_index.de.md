---
title: Kombinieren Sie Diagram
type: docs
weight: 30
url: /de/net/merge-combine-diagram/
description: In diesem Abschnitt wird erläutert, wie die Datei visio kombiniert wird
---
## **Mögliche Nutzungsszenarien**

 Mit Aspose.Diagram können Sie zwei visio-Dateien zu einer kombinieren.
 Aspose.Diagram for .NET API hat die[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) Klasse, die eine Visio-Zeichnung darstellt.
Mit der Methode[**Kombinieren**](https://reference.aspose.com/diagram/net/aspose.diagram/diagram/methods/combine) in[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) Klasse zum Kombinieren von Diagrammen.

## **Beispielcode**

{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load a Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Load another Visio diagram
Diagram diagram2 = new Diagram(Drawing2.vsdx");
diagram2.Combine(diagram);

// Save the new Visio
newDiagram.Save(dataDir + "out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

