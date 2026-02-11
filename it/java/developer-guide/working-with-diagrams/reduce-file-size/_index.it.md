---
title: Riduci dimensione file
type: docs
weight: 50
url: /it/java/reduce-file-size/
description: Questa sezione spiega come ridurre le dimensioni del file da diagram a Aspose.Diagram.
---
## **Riduci dimensione file**
 Aspose.Diagram for Java API consente agli sviluppatori di rimuovere le informazioni nascoste da un diagram per ridurre le dimensioni del file.
 Il[Pagina](https://reference.aspose.com/diagram/java/com.aspose.diagram/Page) oggetto rappresenta l'area di disegno di una pagina in primo piano o di una pagina di sfondo. Per ridurre le dimensioni del file, è possibile utilizzare[RimuoviHiddenInfoItem](https://reference.aspose.com/diagram/java/com.aspose.diagram/RemoveHiddenInfoItem) proprietà in**RimuoviInformazioni Nascoste()** metodo di[Diagram](https://reference.aspose.com/diagram/java)classe. L'esempio di codice seguente mostra come rimuovere le informazioni nascoste da diagram.

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
