---
title: Minska filstorleken
type: docs
weight: 50
url: /sv/java/reduce-file-size/
description: Det här avsnittet förklarar hur du minskar filstorleken från en diagram med Aspose.Diagram.
---
## **Minska filstorleken**
 Aspose.Diagram for Java API tillåter utvecklare att ta bort dold information från en diagram för att minska filstorleken.
 De[Sida](https://reference.aspose.com/diagram/java/com.aspose.diagram/Page) objekt representerar ritytan på en förgrundssida eller en bakgrundssida. För att minska filstorleken kan du använda[RemoveHiddenInfoItem](https://reference.aspose.com/diagram/java/com.aspose.diagram/RemoveHiddenInfoItem) fastigheter i**RemoveHiddenInformation()** metod av[Diagram](https://reference.aspose.com/diagram/java)klass. Kodexemplet nedan visar hur man tar bort dold information från diagram.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ReduceFileSize.class);

// Load a Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Remove hidden information from diagram
diagram.removeHiddenInformation((int)(RemoveHiddenInfoItem.SHAPES | RemoveHiddenInfoItem.MASTERS));
{{< /highlight >}}
```
