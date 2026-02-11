---
title: Slå samman Kombinera Diagram
type: docs
weight: 30
url: /sv/java/merge-combine-diagram/
description: Det här avsnittet förklarar hur man kombinerar visio-filen
---
## **Möjliga användningsscenarier**

 Aspose.Diagram låter dig kombinera två visio-filer till en.
 Aspose.Diagram for Java API har[Diagram](http://www.aspose.com/api/java/diagram/com.aspose.diagram/diagram) klass som representerar en Visio-ritning.
Använder metoden[**Kombinera**](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram#combine(com.aspose.diagram.Diagram) ) i[Diagram](http://www.aspose.com/api/java/diagram/com.aspose.diagram/diagram) klass för att kombinera diagram.

## **Exempelkod**
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
