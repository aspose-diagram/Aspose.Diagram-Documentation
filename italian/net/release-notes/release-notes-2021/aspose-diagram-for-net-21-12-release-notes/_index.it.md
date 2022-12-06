---
title: Aspose.Diagram for .NET 21.12 Note di rilascio
type: docs
weight: 1
url: /it/net/aspose-diagram-for-net-21-12-release-notes/
---
{{% alert color="primary" %}} 

Questa pagina contiene informazioni sulle note di rilascio per Aspose.Diagram for .NET 21.12.

{{% /alert %}} 
## **Miglioramenti e modifiche**

|**Chiave**|**Riepilogo**|**Categoria**|
|:- |:- |:- |
|DIAGRAMNET-52408|problemi quando usiamo EmfRederSetting EmfPlusPrefer|Aumento|
|DIAGRAMNET-52438|SaveForegroundPagesSolo per la stampa|Aumento|
|DIAGRAMNET-52450|Visio to SVG - Saving raster image separately|Aumento|
|DIAGRAMNET-51171|Partial rendering of the shapes on saving drawing in PDF format|Insetto|
|DIAGRAMNET-51390|L'oggetto incorporato non viene sostituito correttamente|Insetto|
|DIAGRAMNET-51800|Visio to SVG - Background Image Missing (PowerPoint is added in the VISIO)|Insetto|
|DIAGRAMNET-52423|Page.Copy() non copia l'oggetto Excel in diagram|Insetto|
|DIAGRAMNET-52443|Forme mancanti durante l'apertura e il salvataggio di MS Visio Diagram|Insetto|
|DIAGRAMNET-52444|Visio in JPG - Diversi risultati generati da API|Insetto|
|DIAGRAMNET-52445|La conversione dell'esempio in ambiente Linux e Windows ha un risultato diverso|Insetto|

## **Public API e modifiche incompatibili con le versioni precedenti**
Di seguito è riportato un elenco di eventuali modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non compatibile con le versioni precedenti apportata a Aspose.Diagram for .NET. In caso di dubbi su qualsiasi modifica elencata, si prega di segnalarlo su il forum di supporto Aspose.Diagram.


### **Aggiunge IsSavingImageSeparately in SVGSaveOptions**
- Definisce se salvare l'immagine separatamente.

{{< highlight "java" >}}

    SVGSaveOptions o = new SVGSaveOptions();
    o.IsSavingImageSeparately = true;

{{< /highlight >}}


### **Aggiunge CustomImagePath in SVGSaveOptions**
- Il percorso personalizzato dell'utente (URL) salvato nel file svg generato per l'immagine. Se non definito dall'utente, verrà utilizzata la directory corrente.

{{< highlight "java" >}}

  o.CustomImagePath = "d:/output/";

{{< /highlight >}}

### **Aggiunge SaveForegroundPagesOnly in PrintSaveOptions**
- Specifica se verranno stampate tutte le pagine o solo in primo piano.

{{< highlight "java" >}}

 PrintSaveOptions options = new PrintSaveOptions();
 options.SaveForegroundPagesOnly = true;

{{< /highlight >}}
