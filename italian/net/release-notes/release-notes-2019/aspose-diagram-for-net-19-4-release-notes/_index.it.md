---
title: Aspose.Diagram for .NET 19.4 Note di rilascio
type: docs
weight: 90
url: /it/net/aspose-diagram-for-net-19-4-release-notes/
---
{{% alert color="primary" %}} 

Questa pagina contiene le note di rilascio per[Aspose.Diagram for .NET 19.4](https://www.nuget.org/packages/Aspose.Diagram/19.4.0)

{{% /alert %}} 
## **Miglioramenti e modifiche**

|**Chiave**|**Riepilogo**|**Categoria**|
|:- |:- |:- |
|DIAGRAMNET-51602|L'oggetto XSLX incorporato viene danneggiato dopo la manipolazione|Aumento|
|DIAGRAMNET-51625|I dati Excel esterni nei file .vsdx vengono rimossi al nuovo salvataggio di Diagram|Aumento|
|DIAGRAMNET-51626|API non elabora dati excel|Aumento|
|DIAGRAMNET-51627|Estrarre i dati di forma sulla base della formula di Dependson|Aumento|
|DIAGRAMNET-51629|L'ingrandimento di una pagina per adattarla a un disegno non sembra funzionare|Aumento|
|DIAGRAMNET-51176|La barra del titolo del gradiente viene modificata durante la conversione di un VSDM in SVG|Insetto|
|DIAGRAMNET-51404|VSD to Image - Il colore della forma è scuro|Insetto|
|DIAGRAMNET-51473|VDX in PDF - Colore di sfondo errato|Insetto|
|DIAGRAMNET-51475|VSDX in PDF - I gradienti vengono renderizzati al contrario|Insetto|
|DIAGRAMNET-51616|Visio in PDF: il gradiente viene visualizzato capovolto nel PDF di output|Insetto|
|DIAGRAMNET-51630|VSDX in HTML: il colore di sfondo delle forme non è presente nell'output|Insetto|
|DIAGRAMNET-51631|VSDX in PDF - Il colore di sfondo delle forme non è presente nell'output|Insetto|
|DIAGRAMNET-51632|VSD a SVG - Impossibile eseguire il cast dell'oggetto di tipo " " nel tipo " " Si è verificata un'eccezione|Insetto|

## **Pubblico API e modifiche incompatibili con le versioni precedenti**
Di seguito è riportato un elenco di tutte le modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non compatibile con le versioni precedenti apportata a Aspose.Diagram for .NET. In caso di dubbi su qualsiasi modifica elencata, segnalarli a il[Aspose.Diagram forum di supporto](https://forum.aspose.com/c/diagram/17).
### **Aggiunge enum RemoveHiddenInfoItem**
Specifica la rimozione delle informazioni nascoste per diagram.
### **Aggiunge RemoveHiddenInfoItem in Diagram**
Rimuovi le informazioni inutilizzate.

{{< highlight "java" >}}

diagram.RemoveHiddenInformation((int)(RemoveHiddenInfoItem.Shapes | RemoveHiddenInfoItem.Masters));

{{< /highlight >}}
