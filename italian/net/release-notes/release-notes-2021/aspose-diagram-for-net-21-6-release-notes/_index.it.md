---
title: Aspose.Diagram for .NET 21.6 Note di rilascio
type: docs
weight: 7
url: /it/net/aspose-diagram-for-net-21-6-release-notes/
---
{{% alert color="primary" %}} 

Questa pagina contiene informazioni sulle note di rilascio per Aspose.Diagram for .NET 21.6.

{{% /alert %}} 
## **Miglioramenti e modifiche**

|**Chiave**|**Riepilogo**|**Categoria**|
|:- |:- |:- |
|DIAGRAMNET-52007|Prestazioni durante l'inizializzazione di un oggetto diagram|Aumento|
|DIAGRAMNET-52008|Prestazioni durante l'inizializzazione di un oggetto diagram|Aumento|
|DIAGRAMNET-52027|La qualità delle forme non è buona nel file SVG esportato|Aumento|
|DIAGRAMNET-52033|Problema di salvataggio delle forme in HTML|Insetto|
|DIAGRAMNET-52035|"Senza eccezioni." eccezione quando si apre il file VSDX|Insetto|
|DIAGRAMNET-52041|Impossibile salvare alcune forme dal file VSS|Insetto|
|DIAGRAMNET-52042|"Parametro non valido." eccezione durante il rendering del file VSD in HTML|Insetto|
|DIAGRAMNET-52043|"Il riferimento non impostato su un'istanza di un oggetto." eccezione durante il salvataggio della forma dal file VSSX|Insetto|

## **Public API e modifiche incompatibili con le versioni precedenti**
Di seguito è riportato un elenco di eventuali modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non compatibile con le versioni precedenti apportata a Aspose.Diagram for .NET. In caso di dubbi su qualsiasi modifica elencata, si prega di segnalarlo su il forum di supporto Aspose.Diagram.
### **Aggiunto EmfRenderSetting in SVGSaveOptions**
- Impostazione per il rendering del metafile EMF

{{< highlight "java" >}}

SVGSaveOptions o = new SVGSaveOptions();
o.EmfRenderSetting = Aspose.Diagram.EmfRenderSetting.EmfPlusPrefer;

{{< /highlight >}}
### **Aggiunge InheritTextBlock in Shape**
- Contiene i valori del blocco di testo per la forma ereditata dallo stile padre e dalla forma principale.



{{< highlight "java" >}}

shape.InheritTextBlock

{{< /highlight >}}





