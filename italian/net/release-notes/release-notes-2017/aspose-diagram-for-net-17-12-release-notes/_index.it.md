---
title: Aspose.Diagram for .NET Note sulla versione 17.12
type: docs
weight: 10
url: /it/net/aspose-diagram-for-net-17-12-release-notes/
---
{{% alert color="primary" %}} 

 Questa pagina contiene le note di rilascio per[Aspose.Diagram for .NET 17.12](https://www.nuget.org/packages/Aspose.Diagram/17.12.0).

{{% /alert %}} 
## **Miglioramenti e modifiche**

|**Chiave**|**Riepilogo**|**Categoria**|
|:- |:- |:- |
|DIAGRAMNET-50016|Aggiungi il supporto per duplicare/clonare una forma|Aumento|
|DIAGRAMNET-50677|Fornisci il singolo API per convertire una forma Visio in PDF|Aumento|
|DIAGRAMNET-50678|Fornisci il singolo API per convertire una forma Visio in HTML|Aumento|
|DIAGRAMNET-50762|L'errore di analisi del valore degli attributi lunghi si è verificato durante la generazione di un VDX diagram|Insetto|
|DIAGRAMNET-51401|Output VSDX - i controlli in Shapes non funzionano|Insetto|
|DIAGRAMNET-51402|VSDX all'immagine: un oggetto OLE non viene conservato|Insetto|
|DIAGRAMNET-51406|VSD all'immagine - vengono visualizzati i caratteri aggiuntivi|Insetto|
|DIAGRAMNET-51410|VSD in PDF - il numero di pagina rimane 4 in tutte le pagine|Insetto|
|DIAGRAMNET-51411|VSD all'immagine - il numero di pagina rimane 4 in tutte le pagine|Insetto|
|DIAGRAMNET-51414|VSDX in PDF - manca il contenuto delle forme|Insetto|
|DIAGRAMNET-51415|VSDX in PDF - colore di sfondo errato delle forme|Insetto|
|DIAGRAMNET-51416|VSDX in HTML - colore di sfondo errato delle forme|Insetto|
## **Pubblico API e modifiche incompatibili con le versioni precedenti**
Di seguito è riportato un elenco di tutte le modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non compatibile con le versioni precedenti apportata a Aspose.Diagram for .NET. In caso di dubbi su qualsiasi modifica elencata, si prega di segnalarli in il[Aspose.Diagram forum di supporto](https://forum.aspose.com/c/diagram/17).
### **Aggiunge il membro Copy nella classe Shape**
Il membro Copy accetta un'istanza della forma di destinazione come parametro per clonare questa forma.

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

Shape newShape = new Shape();

// copy diagram

newShape.Copy(diagram.Pages[0].Shapes[0]);

newShape.ID = 3;

newShape.XForm.PinX.Value = 1;

newShape.XForm.PinY.Value = 1;

{{< /highlight >}}
### **Aggiunge un membro ToPdf nella classe Shape**
Il membro ToPdf converte una forma nel formato PDF.

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// save a shape in the PDF format

diagram.Pages[0].Shapes.GetShape(59).ToPdf("e:\\out.pdf");

{{< /highlight >}}
### **Aggiunge un membro ToHTML nella classe Shape**
Il membro ToHTML converte una forma nel formato PDF.

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

Aspose.Diagram.Saving.HTMLSaveOptions hs = new Aspose.Diagram.Saving.HTMLSaveOptions();

// save a shape in the PDF format

diagram.Pages[0].Shapes.GetShape(59).ToHTML("e:\\out.pdf", hs);

{{< /highlight >}}
### **Esempi di utilizzo**
Si prega di controllare l'elenco degli argomenti della guida aggiunti nei documenti Wiki Aspose.Diagram:

1. [Copia una forma Visio in un'altra istanza di forma](/diagram/it/net/add-2c-retrieve-2c-copy-and-read-visio-shape-data-html/#add-retrieve-copyandreadvisioshapedata-copyavisioshapetoanothershapeinstance)
1. [Converti Visio Shape in PDF](https://docs.aspose.com/diagram/net/convert-a-visio-shape-to-pdf/)
1. [Converti la forma Visio in HTML](https://docs.aspose.com/diagram/net/convert-a-visio-shape-to-html/)
