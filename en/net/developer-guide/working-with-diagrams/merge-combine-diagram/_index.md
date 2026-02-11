---
title: Merge Combine Diagram
type: docs
weight: 30
url: /net/merge-combine-diagram/
description: This section explains how to combine visio file
---

## **Possible Usage Scenarios**

Aspose.Diagram allows you to combine two visio files to one. 
Aspose.Diagram for .NET API has the [Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) class that represents a Visio drawing.
Using the method [**Combine**](https://reference.aspose.com/diagram/net/aspose.diagram/diagram/methods/combine) in [Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) class to combine diagrams. 

## **Sample Code**

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

