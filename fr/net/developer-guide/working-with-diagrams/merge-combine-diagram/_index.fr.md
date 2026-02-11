---
title: Fusionner Combiner Diagram
type: docs
weight: 30
url: /fr/net/merge-combine-diagram/
description: Cette section explique comment combiner le fichier visio
---
## **Scénarios d'utilisation possibles**

 Aspose.Diagram vous permet de combiner deux fichiers visio en un seul.
 Aspose.Diagram for .NET API a le[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) classe qui représente un dessin Visio.
En utilisant la méthode[**Combiner**](https://reference.aspose.com/diagram/net/aspose.diagram/diagram/methods/combine) dans[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) classe pour combiner des diagrammes.

## **Exemple de code**

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

