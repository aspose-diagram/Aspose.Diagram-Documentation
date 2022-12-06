---
title: Aspose.Diagram for .NET Note sulla versione 22.11
type: docs
weight: 17
url: /it/net/aspose-diagram-for-net-22-11-release-notes/
---
{{% alert color="primary" %}} 

Questa pagina contiene informazioni sulle note di rilascio per Aspose.Diagram for .NET 22.11.

{{% /alert %}} 
## **Miglioramenti e modifiche**

|**Chiave**|**Riepilogo**|**Categoria**|
|:- |:- |:- |
|DIAGRAMNET-53011|Aggiunto il supporto per il salvataggio di xaml come flusso|Aumento|
|DIAGRAMNET-53012|Campo di formula non rinfrescante|Aumento|
|DIAGRAMNET-53024|Campo di formula non rinfrescante|Aumento|
|DIAGRAMNET-53009|Conversazione da vsdx a svg immagine persa|Aumento|
|DIAGRAMNET-53010|App: Salvataggio vsdx in Pdf forme perdute|Insetto|
|DIAGRAMNET-53013|Visio to SVG - Custom line patterns|Insetto|
|DIAGRAMNET-53017|Linked area in HTML of VSD has changed to version 22.10.0.0|Insetto|
|DIAGRAMNET-53018|Bug con Paras.SpLine|Insetto|
|DIAGRAMNET-53019|una linea extra è disegnata in basso a sinistra|Insetto|
|DIAGRAMNET-53033|Valori delle celle non calcolati correttamente|Insetto|
|DIAGRAMNET-53034|Cambiamento di forma PinX fa cambiare l'altezza|Insetto|

## **Pubblico API e modifiche incompatibili con le versioni precedenti**
Di seguito è riportato un elenco di eventuali modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non compatibile con le versioni precedenti apportata a Aspose.Diagram for .NET. In caso di dubbi su qualsiasi modifica elencata, si prega di segnalarlo su il forum di supporto Aspose.Diagram.

### **Aggiunge GetConnectorRule in Shape**
- Restituisce un connectorRule che contiene l'id della forma e il connecton che sono connessi alla forma

{{< highlight "java" >}}
ConnectorRule rule= shape.GetConnectorRule();
{{< /highlight >}}

### **Aggiunge IsSavingCustomLinePattern in SVGSaveOptions**
- Definisce se salvare il modello di linea personalizzato.

{{< highlight "java" >}}
var opt = new SVGSaveOptions()
{
     IsSavingCustomLinePattern = false
};
{{< /highlight >}}

### **Aggiunge StreamProvider in XAMLSaveOptions**
- Ottiene o imposta IStreamProvider per l'esportazione di oggetti

{{< highlight "java" >}}
MemoryStream stream = new MemoryStream();
var saveOptions = new XAMLSaveOptions();
var streamProvider = new XamlExportStreamProvider(".vsdx");
saveOptions.StreamProvider = streamProvider;
diagram.Save(stream, saveOptions);
{{< /highlight >}}