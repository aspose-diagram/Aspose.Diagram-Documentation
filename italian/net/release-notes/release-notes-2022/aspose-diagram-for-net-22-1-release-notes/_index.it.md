---
title: Aspose.Diagram for .NET 22.1 Note di rilascio
type: docs
weight: 27
url: /it/net/aspose-diagram-for-net-22-1-release-notes/
---
{{% alert color="primary" %}} 

Questa pagina contiene informazioni sulle note di rilascio per Aspose.Diagram for .NET 22.1.

{{% /alert %}} 
## **Miglioramenti e modifiche**

|**Chiave**|**Riepilogo**|**Categoria**|
|:- |:- |:- |
|DIAGRAMNET-50560|Supporta il salvataggio dei diagrammi in HTML con o senza risorse incorporate|Aumento|
|DIAGRAMNET-52499|Aggiunto il supporto per il salvataggio di html in un flusso singolo|Aumento|
|DIAGRAMNET-50562|VSDX in PDF - Mancano forme nell'output|Insetto|
|DIAGRAMNET-50780|Le linee di confine delle tabelle non sono visibili al salvataggio di un VSDX in PDF|Insetto|
|DIAGRAMNET-50962|Le linee di confine delle tabelle mancano durante la conversione di un VSDX in PNG|Insetto|
|DIAGRAMNET-50992|La linea del bordo sinistro della tabella non è visibile durante la conversione di un file VSDX in PDF|Insetto|
|DIAGRAMNET-51034|L'ombreggiatura delle forme manca durante la conversione di un VSDX in PDF|Insetto|
|DIAGRAMNET-51186|Layout errato delle forme meta type durante la conversione di un VSD in PDF|Insetto|
|DIAGRAMNET-51226|Aspose.Diagram 17.3.0: il salvataggio nel flusso HTML non incorpora risorse esterne|Insetto|
|DIAGRAMNET-52506|Page.Copy() non copia le modifiche dello sviluppatore|Insetto|

## **Public API e modifiche incompatibili con le versioni precedenti**
Di seguito è riportato un elenco di eventuali modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non compatibile con le versioni precedenti apportata a Aspose.Diagram for .NET. In caso di dubbi su qualsiasi modifica elencata, si prega di segnalarlo su il forum di supporto Aspose.Diagram.


### **Aggiunge SaveAsSingleFile in HTMLSaveOptions**
- Indica se salvare l'html come singolo file.

{{< highlight "java" >}}

    HTMLSaveOptions ho = new HTMLSaveOptions();
    ho.SaveAsSingleFile = true;

{{< /highlight >}}