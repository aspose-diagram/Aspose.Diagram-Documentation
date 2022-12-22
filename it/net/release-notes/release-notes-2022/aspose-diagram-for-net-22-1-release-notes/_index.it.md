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
|DIAGRAMNET-50560|Support saving diagrams to HTML with or without embedded resources|Aumento|
|DIAGRAMNET-52499|Aggiunto il supporto per il salvataggio di html in un flusso singolo|Aumento|
|DIAGRAMNET-50562|VSDX to PDF - Shapes are missing from the output|Insetto|
|DIAGRAMNET-50780|The border lines of the tables are not visible on saving a VSDX to PDF|Insetto|
|DIAGRAMNET-50962|The border lines of tables are missing on converting a VSDX to PNG|Insetto|
|DIAGRAMNET-50992|The left border line of the table is not visible on converting a VSDX to PDF|Insetto|
|DIAGRAMNET-51034|The shading of shapes is missing on converting a VSDX to PDF|Insetto|
|DIAGRAMNET-51186|Incorrect layout of meta type shapes on converting a VSD to PDF|Insetto|
|DIAGRAMNET-51226|Aspose.Diagram 17.3.0: Saving to HTML stream do not embed external resources|Insetto|
|DIAGRAMNET-52506|Page.Copy() non copia le modifiche dello sviluppatore|Insetto|

## **Public API e modifiche incompatibili con le versioni precedenti**
Di seguito è riportato un elenco di eventuali modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non compatibile con le versioni precedenti apportata a Aspose.Diagram for .NET. In caso di dubbi su qualsiasi modifica elencata, si prega di segnalarlo su il forum di supporto Aspose.Diagram.


### **Aggiunge SaveAsSingleFile in HTMLSaveOptions**
- Indica se salvare l'html come singolo file.

{{< highlight "java" >}}

    HTMLSaveOptions ho = new HTMLSaveOptions();
    ho.SaveAsSingleFile = true;

{{< /highlight >}}