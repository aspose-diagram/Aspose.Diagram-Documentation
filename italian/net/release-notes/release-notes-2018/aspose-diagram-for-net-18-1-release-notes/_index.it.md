---
title: Aspose.Diagram for .NET 18.1 Note di rilascio
type: docs
weight: 120
url: /it/net/aspose-diagram-for-net-18-1-release-notes/
---
{{% alert color="primary" %}} 

 Questa pagina contiene le note di rilascio per[Aspose.Diagram for .NET 18.1](https://www.nuget.org/packages/Aspose.Diagram/18.1.0).

{{% /alert %}} 
## **Miglioramenti e modifiche**

|**Chiave**|**Riepilogo**|**Categoria**|
|:- |:- |:- |
|DIAGRAMNET-50494|Aggiunto il supporto per duplicare/clonare una pagina diagram|Aumento|
|DIAGRAMNET-51057|Il pulsante di comando non è presente dopo aver rimosso una pagina da VSDM|Aumento|
|DIAGRAMNET-51422|VSDX in PDF: le ombre vengono ignorate sulle forme di elaborazione|Aumento|
|DIAGRAMNET-50467|VSD alla conversione in PDF, il logo aziendale dell'azienda è fuori luogo|Insetto|
|DIAGRAMNET-50469|VSD alla conversione in PDF, il testo della forma radio è leggermente superiore al solito|Insetto|
|DIAGRAMNET-51199|Il testo del titolo non è allineato al salvataggio di un VSDM in SVG|Insetto|
|DIAGRAMNET-51388|Problemi con il caricamento e il salvataggio dei file vsdx|Insetto|
|DIAGRAMNET-51398|VSD in PNG: la posizione del testo non è corretta|Insetto|
|DIAGRAMNET-51407|VSD in JPEG: gli elementi di testo sono fuori posto|Insetto|
|DIAGRAMNET-51419|Le forme non vengono ridimensionate correttamente nel file vsdx|Insetto|
|DIAGRAMNET-51420|VSDX il file viene danneggiato dopo il caricamento e il salvataggio|Insetto|
|DIAGRAMNET-51421|VSDX in PDF - colore del carattere errato del testo|Insetto|
## **Pubblico API e modifiche incompatibili con le versioni precedenti**
Di seguito è riportato un elenco di tutte le modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non compatibile con le versioni precedenti apportata a Aspose.Diagram for .NET. In caso di dubbi su qualsiasi modifica elencata, si prega di segnalarli in il[Aspose.Diagram forum di supporto](https://forum.aspose.com/c/diagram/17).
### **Aggiunge un membro Copy nella classe Page**
Il membro Copy accetta un'istanza della pagina di destinazione, come parametro per clonare questa pagina.

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

Page newPage = new Page(1);

// copy diagram

newPage.Copy(diagram.Pages[0]);

{{< /highlight >}}
### **Esempi di utilizzo**
Si prega di controllare l'elenco degli argomenti della guida aggiunti nei documenti Wiki Aspose.Diagram:

1. [Copia Visio Page in un'altra istanza di Page](https://docs.aspose.com/diagram/net/retrieve-get-copy-and-insert-a-page/#copy-visio-page-to-another-page-instance)
