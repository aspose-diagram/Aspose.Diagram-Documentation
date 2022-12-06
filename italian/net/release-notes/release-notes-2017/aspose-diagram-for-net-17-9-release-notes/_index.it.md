---
title: Aspose.Diagram for .NET 17.9 Note di rilascio
type: docs
weight: 40
url: /it/net/aspose-diagram-for-net-17-9-release-notes/
---
{{% alert color="primary" %}} 

 Questa pagina contiene le note di rilascio per[Aspose.Diagram for .NET 17.9](https://www.nuget.org/packages/Aspose.Diagram/17.9.0).

{{% /alert %}} 
## **Miglioramenti e modifiche**

|**Chiave**|**Riepilogo**|**Categoria**|
|:- |:- |:- |
|DIAGRAMNET-51261|Aggiungi il supporto per convertire l'area specifica di un disegno in immagine|Aumento|
|DIAGRAMNET-51350|Aggiungi il supporto per recuperare la forma per nome|Aumento|
|DIAGRAMNET-51351|Aggiunto il supporto per il recupero della forma da Annotazione|Aumento|
|DIAGRAMNET-51295|VSDX a SVG - la bassa qualità dell'output SVG|Insetto|
|DIAGRAMNET-51309|DiagramException si verifica durante il salvataggio del file VSDX|Insetto|
|DIAGRAMNET-51331|VSDM in SVG: gli elementi di testo vengono spostati verso l'alto|Insetto|
|DIAGRAMNET-51333|VSDM a SVG - resa errata delle icone circolari|Insetto|
|DIAGRAMNET-51339|VSDX in SVG - il troncamento del testo dal lato destro di ciascuna immagine|Insetto|
|DIAGRAMNET-51340|Ordine dei commenti errato|Insetto|
|` `DIAGRAMNET-51342|Errore di memoria insufficiente dopo aver utilizzato il metodo "AddComment" e aver salvato il file su Steam|Insetto|
|DIAGRAMNET-51344|VSDX in PDF: si è verificato un errore di argomento fuori intervallo|Insetto|
|DIAGRAMNET-51345|Il commento non viene eliminato insieme alla forma|Insetto|
|DIAGRAMNET-51346|VSDM in SVG: la qualità del logo viene ridotta|Insetto|
|DIAGRAMNET-51347|VSDM in SVG: la qualità del logo viene ridotta|Insetto|
|DIAGRAMNET-51353|Impossibile aggiungere un altro commento nella pagina Visio|Insetto|
|DIAGRAMNET-51354|Impossibile modificare i commenti nella pagina Visio|Insetto|
## **Pubblico API e modifiche incompatibili con le versioni precedenti**
Di seguito è riportato un elenco di tutte le modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non compatibile con le versioni precedenti apportata a Aspose.Diagram for .NET. In caso di dubbi su qualsiasi modifica elencata, si prega di segnalarli in il[Aspose.Diagram forum di supporto](https://forum.aspose.com/c/diagram/17).
### **Aggiunge il membro GetShape in ShapeCollection**
Permette di recuperare una forma per nome.

{{< highlight "java" >}}

 string dataDir = @"C:\temp\";

// load a drawing

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// retrieve page by name

Page page = diagram.Pages.GetPage("Page-1");

// retrieve shape by name

Shape shape = page.Shapes.GetShape("name");

{{< /highlight >}}
### **Aggiunge il membro ShapeID in Annotation**
Permette di tracciare la forma del commento.

{{< highlight "java" >}}

 string dataDir = @"C:\temp\";

// load a drawing

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// get the annotation by index

Annotation annotation = diagram.Pages.GetPage("Page-1").PageSheet.Annotations[1];

// get shape Id

Console.WriteLine(annotation.ShapeID);

{{< /highlight >}}
### **Aggiunge Area in RenderingSaveOptions**
Permette di convertire la regione specifica del rettangolo del disegno Visio.

{{< highlight "java" >}}

 // load a Visio drawing

Diagram diagram = new Diagram(@"c:\\test.vsdx");

ImageSaveOptions Options = new ImageSaveOptions(SaveFileFormat.PNG);

// specify region

Options.Area = new RectangleF(0, 0, 1, 1);

// save into the image format

diagram.Save("e:\\area.png", Options);

{{< /highlight >}}
### **Esempi di utilizzo**
Si prega di controllare l'elenco degli argomenti della guida aggiunti nei documenti Wiki Aspose.Diagram:

1. [Converti l'area specificata della pagina Visio in un'immagine](https://docs.aspose.com/diagram/net/working-with-images/#convert-specified-area-of-the-visio-page-to-an-image)
1. [Spaziatura automatica una raccolta di forme nella pagina Visio](/diagram/it/net/auto-space-a-collection-of-shapes-in-the-visio-page/)
