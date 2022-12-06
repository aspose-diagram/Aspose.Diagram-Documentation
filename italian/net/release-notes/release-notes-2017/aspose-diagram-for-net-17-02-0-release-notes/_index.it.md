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
|DIAGRAMNET-50149|VSD to PDF conversion, the background color shade of a group shape is getting changed.|Insetto|
|DIAGRAMNET-50579|VSDX to PDF conversion, incorrect background color of the shape.|Insetto|
|DIAGRAMNET-50984|The border lines of the table are missing on converting a VSDX to PNG.|Insetto|
|DIAGRAMNET-50985|The text items are not aligned properly on converting a VSDX to PNG.|Insetto|
|DIAGRAMNET-50999|Rendering incorrect color of shapes on converting a VSD to PNG.|Insetto|
|DIAGRAMNET-51002|La proprietà HTMLSaveOptions.DefaultFont non funziona come previsto.|Insetto|
|DIAGRAMNET-51049|The color of shapes is not being rendered correctly on converting a VSD to HTML.|Insetto|
|DIAGRAMNET-51080|The wrong text alignment of shapes on saving in EMF.|Insetto|
|DIAGRAMNET-51132|The rounded shape corners are being changed on converting a VSD to PDF.|Insetto|
|DIAGRAMNET-51133|The layout of dynamic arrow connector is changed on converting a VSD to PDF.|Insetto|
|DIAGRAMNET-51135|The Visio shapes are displaced on converting a VSDX to PDF.|Insetto|
|DIAGRAMNET-51136|The vertical text appears as horizontal text on converting a VSDX to PDF.|Insetto|
|DIAGRAMNET-51140|Vertical text box is overhanging the edge of the node while converting VSDX to PDF.|Insetto|
|DIAGRAMNET-51138|Si è verificato un errore durante il caricamento di un VSDX diagram.|Eccezione|
|DIAGRAMNET-51139|Can't access file error occurred on converting a VSDX to HTML.|Eccezione|
|DIAGRAMNET-51148|NullReferenceException at Diagram.Save while converting VSD to HTML.|Eccezione|
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
