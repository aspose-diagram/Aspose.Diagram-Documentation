---
title: Controlla l'espansione automatica della pagina
type: docs
weight: 10
url: /it/java/check-page-autoexpand/
description: Questa sezione spiega come controllare o cambiare la pagina è l'espansione automatica in un file visio con Aspose.Diagram.
---
## **Controlla la pagina AutoExpand**

 Il[Pagina](https://reference.aspose.com/diagram/java/com.aspose.diagram/page)oggetto rappresenta l'area di disegno di una pagina in primo piano o di una pagina di sfondo. La proprietà Pages esposta da[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) class supporta una raccolta di oggetti Aspose.Diagram.Page.
 Il[PageProps](https://reference.aspose.com/diagram/java/com.aspose.diagram/PageProps) L'oggetto rappresenta gli attributi della pagina, come la larghezza, l'altezza e la scala della pagina. Questa proprietà può essere utilizzata per controllare l'espansione automatica della pagina.

Usa la proprietà PageProps per controllare l'espansione automatica della pagina.
### **Esempio di programmazione per l'espansione automatica della pagina di controllo**
La seguente parte di codice controlla l'espansione automatica della pagina da diagram.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(CheckChangeAutoExpand.class);
      
// Initialize the new visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get Visio page
Page page = diagram.getPages().getPage("Page-2");
// Get Page autoexpand
boolean isAutoExpand = page.getPageSheet().getPageProps().getDrawingResizeType().getValue() == DrawingResizeTypeValue.AUTOMATICALLY ? true : false;
//Set Page autoexpand
page.getPageSheet().getPageProps().getDrawingResizeType().setValue(DrawingResizeTypeValue.NOT_AUTOMATICALLY);

// Save Visio
diagram.save(dataDir + "SetAutoExpand_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
