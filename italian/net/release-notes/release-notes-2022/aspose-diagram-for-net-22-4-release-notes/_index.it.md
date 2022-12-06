---
title: Aspose.Diagram for .NET 22.4 Note di rilascio
type: docs
weight: 24
url: /it/net/aspose-diagram-for-net-22-4-release-notes/
---
{{% alert color="primary" %}} 

Questa pagina contiene informazioni sulle note di rilascio per Aspose.Diagram for .NET 22.4.

{{% /alert %}} 
## **Miglioramenti e modifiche**

|**Chiave**|**Riepilogo**|**Categoria**|
|:- |:- |:- |
|DIAGRAMNET-52015|Ticket di continuazione di #DIAGRAMNET-51995 - Problemi con i file Aspose.Diagram e Skyline Datamine|Aumento|
|DIAGRAMNET-52707|Le modifiche alla formula/valore del foglio di forma non attivano modifiche nelle celle dipendenti|Aumento|
|DIAGRAMNET-50345|Conversione da VSDX a PDF, colore di sfondo errato delle forme|Insetto|
|DIAGRAMNET-50954|Problemi di formattazione nel rendering di una tabella e di un pulsante di opzione durante la conversione di un file VSDX in PNG|Insetto|
|DIAGRAMNET-52708|Conversione della posizione del testo in svg|Insetto|
|DIAGRAMNET-52739|Formato dei punti sensibili alla cultura|Insetto|
|DIAGRAMNET-52759|Il testo presente nella tabella viene rimosso durante la conversione del file .vsdx in pdf|Insetto|
|DIAGRAMNET-52762|VSDX in PDF - Immagine non convertita|Insetto|
|DIAGRAMNET-52779|Le ellissi non vengono ridimensionate durante la conversione di Visio in SVG|Insetto|

## **Pubblico API e modifiche incompatibili con le versioni precedenti**
Di seguito è riportato un elenco di eventuali modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non compatibile con le versioni precedenti apportata a Aspose.Diagram for .NET. In caso di dubbi su qualsiasi modifica elencata, si prega di segnalarlo su il forum di supporto Aspose.Diagram.
### **Aggiunge GetPureText in Shape**
- Ottieni la stringa di testo di una forma.

{{< highlight "java" >}}
String text = shape.GetPureText();
{{< /highlight >}}

