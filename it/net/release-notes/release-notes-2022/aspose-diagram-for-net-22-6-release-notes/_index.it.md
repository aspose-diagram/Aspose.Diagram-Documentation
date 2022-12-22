---
title: Aspose.Diagram for .NET 22.6 Note di rilascio
type: docs
weight: 22
url: /it/net/aspose-diagram-for-net-22-6-release-notes/
---
{{% alert color="primary" %}} 

Questa pagina contiene informazioni sulle note di rilascio per Aspose.Diagram for .NET 22.6.

{{% /alert %}} 
## **Miglioramenti e modifiche**

|**Chiave**|**Riepilogo**|**Categoria**|
|:- |:- |:- |
|DIAGRAMNET-52826|Broken link when saving VSDM to PDF|Aumento|
|DIAGRAMNET-52851|Alcune forme perdono la loro curva dopo la conversione in svg|Aumento|
|DIAGRAMNET-52858|Image quality in HTML|Aumento|
|DIAGRAMNET-52825|Export to HTML problem|Insetto|
|DIAGRAMNET-52832|Visio to PDF/SVG - Rotated text position changed|Insetto|
|DIAGRAMNET-52840|Elements in HTML preview blurred|Insetto|
|DIAGRAMNET-52842|La pagina di adattamento automatico non si adatta automaticamente|Insetto|
|DIAGRAMNET-52849|Immagini raster non ridimensionate dopo la conversione|Insetto|
|DIAGRAMNET-52852|VSD Errore di apertura - Aspose.Diagram.DiagramException|Insetto|

## **Pubblico API e modifiche incompatibili con le versioni precedenti**
Di seguito è riportato un elenco di eventuali modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non compatibile con le versioni precedenti apportata a Aspose.Diagram for .NET. In caso di dubbi su qualsiasi modifica elencata, si prega di segnalarlo su il forum di supporto Aspose.Diagram.
### **Aggiunge risoluzione in HTMLSaveOptions**
- Ottiene o imposta la risoluzione per il codice HTML generato, in punti per pollice.

{{< highlight "java" >}}
HTMLSaveOptions option = new HTMLSaveOptions();
option.Resolution = 96;
{{< /highlight >}}
