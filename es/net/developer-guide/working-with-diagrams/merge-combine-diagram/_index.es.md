---
title: Combinar combinar Diagram
type: docs
weight: 30
url: /es/net/merge-combine-diagram/
description: Esta sección explica cómo combinar el archivo visio
---
## **Posibles escenarios de uso**

 Aspose.Diagram le permite combinar dos archivos visio en uno.
 Aspose.Diagram for .NET API tiene el[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) clase que representa un dibujo Visio.
Usando el método[**Combinar**](https://reference.aspose.com/diagram/net/aspose.diagram/diagram/methods/combine) en[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) clase para combinar diagramas.

## **Código de muestra**
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
