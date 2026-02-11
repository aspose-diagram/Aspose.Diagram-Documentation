---
title: Cambia dimensione pagina
type: docs
weight: 10
url: /it/java/change-page-size/
description: Questa sezione spiega come modificare le dimensioni della pagina in un file visio con Aspose.Diagram.
---
## **Cambia dimensione pagina**

 Il[Pagina](https://reference.aspose.com/diagram/java/com.aspose.diagram/page)oggetto rappresenta l'area di disegno di una pagina in primo piano o di una pagina di sfondo. La proprietà Pages esposta da[Diagram](http://www.aspose.com/api/java/diagram/com.aspose.diagram/diagram) class supporta una raccolta di oggetti Aspose.Diagram.Page.
 Il[PageProps](https://reference.aspose.com/diagram/java/com.aspose.diagram/PageProps) L'oggetto rappresenta gli attributi della pagina, come la larghezza, l'altezza e la scala della pagina. Questa proprietà può essere utilizzata per modificare le dimensioni della pagina.

Utilizzare la proprietà PageProps per modificare le dimensioni della pagina.
### **Esempio di programmazione delle dimensioni della pagina**
La seguente parte di codice modifica le dimensioni della pagina da diagram.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ChangeVisioPageSize.class);
      
// Initialize the new visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get Visio page
Page page = diagram.getPages().getPage("Flow 1");
// Set Page Size
page.getPageSheet().getPageProps().getPageHeight().setValue(8);
page.getPageSheet().getPageProps().getPageWidth().setValue(11);

// Save Visio
diagram.save(dataDir + "SetPageSize_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

