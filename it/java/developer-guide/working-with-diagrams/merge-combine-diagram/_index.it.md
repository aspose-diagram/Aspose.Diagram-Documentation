---
title: Unisci Combina Diagram
type: docs
weight: 30
url: /it/java/merge-combine-diagram/
description: Questa sezione spiega come combinare il file visio
---
## **Possibili scenari di utilizzo**

 Aspose.Diagram consente di unire due file visio in uno.
 Aspose.Diagram for Java API ha il[Diagram](http://www.aspose.com/api/java/diagram/com.aspose.diagram/diagram) class che rappresenta un disegno Visio.
Usando il metodo[**Combina**](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram#combine(com.aspose.diagram.Diagram) ) in[Diagram](http://www.aspose.com/api/java/diagram/com.aspose.diagram/diagram) classe per combinare i diagrammi.

## **Codice di esempio**

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

