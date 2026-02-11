---
title: Slå samman Kombinera Diagram
type: docs
weight: 30
url: /sv/net/merge-combine-diagram/
description: Det här avsnittet förklarar hur man kombinerar visio-filen
---
## **Möjliga användningsscenarier**

 Aspose.Diagram låter dig kombinera två visio-filer till en.
 Aspose.Diagram for .NET API har[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) klass som representerar en Visio-ritning.
Använder metoden[**Kombinera**](https://reference.aspose.com/diagram/net/aspose.diagram/diagram/methods/combine) i[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) klass för att kombinera diagram.

## **Exempelkod**

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

