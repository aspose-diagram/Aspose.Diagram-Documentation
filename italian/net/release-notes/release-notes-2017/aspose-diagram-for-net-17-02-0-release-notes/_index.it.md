---
title: Aspose.Diagram for .NET 17.02.0 Note di rilascio
type: docs
weight: 110
url: /it/net/aspose-diagram-for-net-17-02-0-release-notes/
---
{{% alert color="primary" %}} 

Questa pagina contiene le note di rilascio per[Aspose.Diagram for .NET 17.02.0](https://www.nuget.org/packages/Aspose.Diagram/17.2.0).

{{% /alert %}} 
## **Miglioramenti e modifiche**

|**Chiave**|**Riepilogo**|**Categoria**|
|:- |:- |:- |
|DIAGRAMNET-50018|Aggiunto il supporto della conformità CLS.|Nuova caratteristica|
|DIAGRAMNET-51110|Integrato con il misuratore.|Nuova caratteristica|
|DIAGRAMNET-51143|Capacità di ottenere il gruppo di una data forma.|Nuova caratteristica|
|DIAGRAMNET-51144|Capacità di ottenere il genitore di una data forma.|Nuova caratteristica|
|DIAGRAMNET-50149|VSD alla conversione PDF, la tonalità del colore di sfondo di una forma di gruppo viene modificata.|Insetto|
|DIAGRAMNET-50579|Conversione da VSDX a PDF, colore di sfondo errato della forma.|Insetto|
|DIAGRAMNET-50984|Le linee di confine della tabella mancano durante la conversione di un VSDX in PNG.|Insetto|
|DIAGRAMNET-50985|Gli elementi di testo non sono allineati correttamente durante la conversione di un VSDX in PNG.|Insetto|
|DIAGRAMNET-50999|Rendering del colore errato delle forme durante la conversione di un VSD in PNG.|Insetto|
|DIAGRAMNET-51002|La proprietà HTMLSaveOptions.DefaultFont non funziona come previsto.|Insetto|
|DIAGRAMNET-51049|Il colore delle forme non viene visualizzato correttamente durante la conversione di VSD in HTML.|Insetto|
|DIAGRAMNET-51080|L'errato allineamento del testo delle forme durante il salvataggio in EMF.|Insetto|
|DIAGRAMNET-51132|Gli angoli della forma arrotondata vengono modificati durante la conversione di un VSD in PDF.|Insetto|
|DIAGRAMNET-51133|Il layout del connettore freccia dinamica viene modificato durante la conversione di un VSD in PDF.|Insetto|
|DIAGRAMNET-51135|Le forme Visio vengono spostate durante la conversione di un VSDX in PDF.|Insetto|
|DIAGRAMNET-51136|Il testo verticale appare come testo orizzontale durante la conversione di un VSDX in PDF.|Insetto|
|DIAGRAMNET-51140|La casella di testo verticale sporge dal bordo del nodo durante la conversione di VSDX in PDF.|Insetto|
|DIAGRAMNET-51138|Si è verificato un errore durante il caricamento di un VSDX diagram.|Eccezione|
|DIAGRAMNET-51139|Si è verificato un errore di accesso al file durante la conversione di VSDX in HTML.|Eccezione|
|DIAGRAMNET-51148|NullReferenceException in Diagram. Salva durante la conversione di VSD in HTML.|Eccezione|
|DIAGRAMNET-51149|NullReferenceException in Diagram. Salva quando la proprietà CustomProp.Name non è impostata|Eccezione|
## **Pubblico API e modifiche incompatibili con le versioni precedenti**
 Di seguito è riportato un elenco di tutte le modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non compatibile con le versioni precedenti apportata a Aspose.Diagram for .NET. In caso di dubbi su qualsiasi modifica elencata, segnalarli a il[Aspose.Diagram forum di supporto](https://forum.aspose.com/c/diagram/17).
### **Aggiunge la proprietà Shape.ParentShape**
La proprietà Shape.ParentShape permette di ottenere la forma genitore di una forma recente.

{{< highlight "java" >}}

 // Call a Diagram class constructor to load the VSD diagram

Diagram diagram = new Diagram("Drawing1.vsdx");

// get a sub-shape by page name, group shape ID, and then sub-shape ID

Shape shape = diagram.Pages.GetPage("Page-3").Shapes.GetShape(13).Shapes.GetShape(2);

Shape parentShape = shape.ParentShape;

Console.WriteLine("Parent Shape's Properties:");

Console.WriteLine("Shape ID: " + parentShape.ID);

Console.WriteLine("Shape Name: " + parentShape.Name);

Console.WriteLine("Shape Type: " + parentShape.Type);

{{< /highlight >}}
### **Aggiunge il metodo Shape.IsInGroup**
Il metodo Shape.IsInGroup consente di rilevare se la forma recente fa parte di una qualsiasi forma di gruppo.

{{< highlight "java" >}}

 // Call a Diagram class constructor to load the VSD diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// get a sub-shape by page name, group shape ID, and then sub-shape ID

Shape shape = diagram.Pages.GetPage("Page-3").Shapes.GetShape(13).Shapes.GetShape(2);

Console.WriteLine("Is it in a Group: " + shape.IsInGroup());

{{< /highlight >}}
### **Aggiunge la classe misurata**
Viene aggiunta la classe Metered. Consente agli sviluppatori di sbloccare i limiti di valutazione di Aspose.Diagram API nonché di tenere traccia e mantenere le licenze API. Monitora anche l'uso regolare di Aspose.Diagram API.

{{< highlight "java" >}}

 // Initialize a Metered license class object

Aspose.Diagram.Metered metered = new Aspose.Diagram.Metered();

// apply public and private keys

metered.SetMeteredKey("your-public-key", "your-private-key");

{{< /highlight >}}
### **Esempi di utilizzo**
Si prega di controllare l'elenco degli argomenti della guida aggiunti nei documenti Wiki Aspose.Diagram:

1. [Impostare le chiavi pubbliche e private per applicare la licenza misurata](/diagram/it/net/licensing/#licensing-setpublicandprivatekeystoapplymeteredlicense)
1. [Recupera la forma padre di una forma secondaria](/diagram/it/net/add-retrieve-copy-and-read-visio-shape-data/#add-retrieve-copyandreadvisioshapedata-retrievetheparentshapeofasub-shape)
1. [Verificare se la forma Visio si trova in un gruppo di forme](https://docs.aspose.com/diagram/net/group-convert-and-verify-shapes/)
