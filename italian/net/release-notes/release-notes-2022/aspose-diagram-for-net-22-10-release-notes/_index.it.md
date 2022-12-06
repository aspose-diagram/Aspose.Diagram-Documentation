---
title: Aspose.Diagram for .NET 22.10 Note di rilascio
type: docs
weight: 18
url: /it/net/aspose-diagram-for-net-22-10-release-notes/
---
{{% alert color="primary" %}} 

Questa pagina contiene informazioni sulle note di rilascio per Aspose.Diagram for .NET 22.10.

{{% /alert %}} 
## **Miglioramenti e modifiche**

|**Chiave**|**Riepilogo**|**Categoria**|
|:- |:- |:- |
|DIAGRAMNET-52988|Un elemento grafico viene visualizzato in qualità scadente quando viene esportato in formato SVG|Aumento|
|DIAGRAMNET-53002|Collegamento perso durante l'esportazione in html con Aspose.Diagram|Aumento|
|DIAGRAMNET-52983|Errore in Diagram.Salva|Insetto|
|DIAGRAMNET-52984|Modificare i valori nella classe VentureLicenser|Insetto|
|DIAGRAMNET-52993|La conversazione da vsdx a svg non riesce|Insetto|
|DIAGRAMNET-52995|App: il caricamento di vsd genera un'eccezione|Insetto|

## **Pubblico API e modifiche incompatibili con le versioni precedenti**
Di seguito è riportato un elenco di eventuali modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non compatibile con le versioni precedenti apportata a Aspose.Diagram for .NET. In caso di dubbi su qualsiasi modifica elencata, si prega di segnalarlo su il forum di supporto Aspose.Diagram.

### **Aggiunge GetDisplayText in Shape**
- Ottenere il testo visualizzato sull'interfaccia

{{< highlight "java" >}}
String text = shape.GetDisplayText();
{{< /highlight >}}

### **Aggiunge InheritGeoms in Shape**
- Contiene i valori Geoms per la forma ereditata dalla forma principale.

{{< highlight "java" >}}
int count = shape.InheritGeoms.Count;
{{< /highlight >}}