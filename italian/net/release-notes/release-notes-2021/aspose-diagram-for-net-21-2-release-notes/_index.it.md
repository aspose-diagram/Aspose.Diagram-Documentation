---
title: Aspose.Diagram for .NET 21.2 Note di rilascio
type: docs
weight: 11
url: /it/net/aspose-diagram-for-net-21-2-release-notes/
---
{{% alert color="primary" %}} 

Questa pagina contiene informazioni sulle note di rilascio per Aspose.Diagram for .NET 21.2.

{{% /alert %}} 
## **Miglioramenti e modifiche**

|**Chiave**|**Riepilogo**|**Categoria**|
|:- |:- |:- |
|DIAGRAMNET-51986|Aggiungere il metodo centerDrawing presente nella pagina di interoperabilità visio|Aumento|
|DIAGRAMNET-51987|Implementa un metodo per ottenere ActivePage|Aumento|
|DIAGRAMNET-51978|Converti VSD in VSDX - impossibile aprire l'output in MS Visio|Insetto|
|DIAGRAMNET-51980|"Si è verificato un errore generico in GDI+." eccezione durante il rendering nel file HTML VSDX|Insetto|
|DIAGRAMNET-51981|Converti VSDX in PDF - Le forme sono nere nel pdf di output|Insetto|
|DIAGRAMNET-51985|Conversione da VSDX a VSDX/VDX: i colori delle forme cambiano in sfumatura dopo il salvataggio|Insetto|
|DIAGRAMNET-51989|Visio in HTML - Strano bordo nell'output|Insetto|

## ` `**Public API e modifiche incompatibili con le versioni precedenti**
` `Di seguito è riportato un elenco di eventuali modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non compatibile con le versioni precedenti apportata a Aspose.Diagram for .NET. il forum di supporto Aspose.Diagram.
### **Aggiunto ActivePage in Diagram**
- Specifica la pagina attiva

{{< highlight "java" >}}

Page page = diagram.ActivePage;

{{< /highlight >}}
### **Aggiunge CenterDrawing in Shape**
- Centrare la forma rispetto all'estensione della pagina



{{< highlight "java" >}}

shape.CenterDrawing()

{{< /highlight >}}
### **Aggiunge DrawLine nella pagina**
- Il processo di tracciare una singola linea.



{{< highlight "java" >}}

 diagram.Pages[0].DrawLine(0,0,1,1);

{{< /highlight >}}



