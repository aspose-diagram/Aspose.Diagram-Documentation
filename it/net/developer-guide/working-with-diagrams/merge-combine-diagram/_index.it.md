---
title: Unisci Combina Diagram
type: docs
weight: 30
url: /it/net/merge-combine-diagram/
description: Questa sezione spiega come combinare il file visio
---
## **Possibili scenari di utilizzo**

 Aspose.Diagram consente di unire due file visio in uno.
 Aspose.Diagram for .NET API ha il[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) class che rappresenta un disegno Visio.
Usando il metodo[**Combina**](https://reference.aspose.com/diagram/net/aspose.diagram/diagram/methods/combine) in[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) classe per combinare i diagrammi.

## **Codice di esempio**
```
{{< highlight "csharp" >}}
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
```
