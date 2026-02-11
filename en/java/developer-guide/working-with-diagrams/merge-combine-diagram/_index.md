---
title: Merge Combine Diagram
type: docs
weight: 30
url: /java/merge-combine-diagram/
description: This section explains how to combine visio file
---

## **Possible Usage Scenarios**

Aspose.Diagram allows you to combine two visio files to one. 
Aspose.Diagram for Java API has the [Diagram](http://www.aspose.com/api/java/diagram/com.aspose.diagram/diagram) class that represents a Visio drawing.
Using the method [**Combine**](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram#combine(com.aspose.diagram.Diagram)) in [Diagram](http://www.aspose.com/api/java/diagram/com.aspose.diagram/diagram) class to combine diagrams. 

## **Sample Code**

{{< highlight java >}}
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

