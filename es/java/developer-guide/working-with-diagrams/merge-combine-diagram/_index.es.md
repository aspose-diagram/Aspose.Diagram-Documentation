---
title: Combinar combinar Diagram
type: docs
weight: 30
url: /es/java/merge-combine-diagram/
description: Esta sección explica cómo combinar el archivo visio
---
## **Posibles escenarios de uso**

 Aspose.Diagram le permite combinar dos archivos visio en uno.
 Aspose.Diagram for Java API tiene el[Diagram](http://www.aspose.com/api/java/diagram/com.aspose.diagram/diagram) clase que representa un dibujo Visio.
Usando el método[**Combinar**](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram#combine(com.aspose.diagram.Diagram) ) en[Diagram](http://www.aspose.com/api/java/diagram/com.aspose.diagram/diagram) clase para combinar diagramas.

## **Código de muestra**
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
