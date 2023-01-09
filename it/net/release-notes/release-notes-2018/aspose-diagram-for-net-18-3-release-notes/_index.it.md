---
title: Aspose.Diagram for .NET 18.3 Note di rilascio
type: docs
weight: 100
url: /it/net/aspose-diagram-for-net-18-3-release-notes/
---
{{% alert color="primary" %}} 

 Questa pagina contiene le note di rilascio per[Aspose.Diagram for .NET 18.3](https://www.nuget.org/packages/Aspose.Diagram/18.3.0).

{{% /alert %}} 
## **Miglioramenti e modifiche**

|**Chiave**|**Riepilogo**|**Categoria**|
|:- |:- |:- |
|DIAGRAMNET-50147|VSD to XPS conversion, the empty pages are created having red cross images|Aumento|
|DIAGRAMNET-51431|Aggiunto il metodo MoveTo per la raccolta Pages|Aumento|
|DIAGRAMNET-50424  |VSDX to PDF conversion, the icon is overlying the text|Insetto|
|DIAGRAMNET-50459|VSDX to PDF conversion, shape icon is misplaced from its original position|Insetto|
|DIAGRAMNET-50460|VSDX to PDF conversion, shape icon is misplaced from its original position|Insetto|
|DIAGRAMNET-50674|All HTML resources are not saved at the custom path|Insetto|
|DIAGRAMNET-51403|VSD all'immagine - le punte delle frecce sono fuori posto|Insetto|
|DIAGRAMNET-51427|Output VSDX - i controlli in Shapes non funzionano|Insetto|
|DIAGRAMNET-51429|Correggi l'URL della pagina del prodotto sulla galleria NuGet|Insetto|
|DIAGRAMNET-51432|La routine di apertura e salvataggio di VSDX non conserva la cella del carattere|Insetto|
|DIAGRAMNET-51433|Impossibile recuperare tutti i nomi delle forme da un disegno VSDX|Insetto|
## **Pubblico API e modifiche incompatibili con le versioni precedenti**
Di seguito è riportato un elenco di tutte le modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non compatibile con le versioni precedenti apportata a Aspose.Diagram for .NET. In caso di dubbi su qualsiasi modifica elencata, si prega di segnalarli in il[Aspose.Diagram forum di supporto](https://forum.aspose.com/c/diagram/17).
### **Aggiunge il membro MoveTo nella classe Page**
Il membro MoveTo utilizza l'indice della pagina di destinazione come parametro per spostare la posizione della pagina nel disegno Visio.

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

Page newPage = new Page(1);

// move page in the diagram

newPage.MoveTo(2);

{{< /highlight >}}
### **Esempi di utilizzo**
Si prega di controllare l'elenco degli argomenti della guida aggiunti nei documenti Wiki Aspose.Diagram:

1. [Sposta la posizione della pagina nel disegno Visio](https://docs.aspose.com/diagram/net/retrieve-get-copy-and-insert-a-page/#move-page-position-in-the-visio-drawing)
