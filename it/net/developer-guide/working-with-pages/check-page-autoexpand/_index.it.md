---
title: Controlla l'espansione automatica della pagina
type: docs
weight: 10
url: /it/net/check-page-autoexpand/
description: Questa sezione spiega come controllare o cambiare la pagina è l'espansione automatica in un file visio con Aspose.Diagram.
---
## **Cambia dimensione pagina**

 Il[Pagina](http://www.aspose.com/api/net/diagram/aspose.diagram/page)oggetto rappresenta l'area di disegno di una pagina in primo piano o di una pagina di sfondo. La proprietà Pages esposta da[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) class supporta una raccolta di oggetti Aspose.Diagram.Page.
 Il[PageProps](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/pageprops) L'oggetto rappresenta gli attributi della pagina, come la larghezza, l'altezza e la scala della pagina. Questa proprietà può essere utilizzata per controllare l'espansione automatica della pagina.

Usa la proprietà PageProps per controllare l'espansione automatica della pagina.
### **Esempio di programmazione delle dimensioni della pagina**
La seguente parte di codice controlla l'espansione automatica della pagina da diagram.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();

// Initialize the new visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get Visio page
Aspose.Diagram.Page page = diagram.Pages.GetPage("Flow 1");
// Get Page autoexpand
bool isAutoExpand = page.PageSheet.PageProps.DrawingResizeType.Value == DrawingResizeTypeValue.Automatically ? true : false;
//Set Page autoexpand
page.PageSheet.PageProps.DrawingResizeType.Value = DrawingResizeTypeValue.NotAutomatically;

// Save Visio
diagram.Save(dataDir + "SetAutoExpand_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
