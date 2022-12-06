---
title: Aspose.Diagram for .NET 17.8 Note di rilascio
type: docs
weight: 50
url: /it/net/aspose-diagram-for-net-17-8-release-notes/
---
{{% alert color="primary" %}} 

 Questa pagina contiene le note di rilascio per[Aspose.Diagram for .NET 17.8](https://www.nuget.org/packages/Aspose.Diagram/17.8.0).

{{% /alert %}} 
## **Miglioramenti e modifiche**

|**Chiave**|**Riepilogo**|**Categoria**|
|:- |:- |:- |
|DIAGRAMNET-51295|VSDX a SVG - la bassa qualità dell'output SVG.|Aumento|
|DIAGRAMNET-51298|SVGSaveOptions: aggiunge il supporto per controllare il livello di compressione bitmap.|Aumento|
|DIAGRAMNET-51300|Aggiunto il supporto per la connessione di forme con l'indice di connessione.|Aumento|
|DIAGRAMNET-50577|VSDX alla conversione in PDF, il testo della forma circolare è fuori posto - I.|Insetto|
|DIAGRAMNET-50582|VSDX alla conversione HTML, il testo della forma circolare è fuori luogo - I.|Insetto|
|DIAGRAMNET-50601|VSDX alla conversione in PDF, il testo della forma circolare è fuori posto - II.|Insetto|
|DIAGRAMNET-50606|VSDX alla conversione HTML, il testo della forma circolare è fuori luogo - II.|Insetto|
|DIAGRAMNET-51197|Le forme dei triangoli di avviso non vengono visualizzate correttamente durante il salvataggio di VSDM in SVG.|Insetto|
|DIAGRAMNET-51245|Elementi di testo spostati durante la conversione di un VSD in PDF.|Insetto|
|DIAGRAMNET-51246|Caratteri errati applicati al testo durante la conversione di un VSD in PDF.|Insetto|
|DIAGRAMNET-51296|VSDM in SVG: l'immagine viene troncata.|Insetto|
|DIAGRAMNET-51301|VSDX in PDF: il colore del testo sulle linee di collegamento viene modificato.|Insetto|
|DIAGRAMNET-51302|VSDX in PDF - elementi grafici mancanti.|Insetto|
|DIAGRAMNET-51304|VSDX in PDF - resa incompleta del diagramma di flusso.|Insetto|
|DIAGRAMNET-51305|VSDX in PDF - elementi grafici mancanti.|Insetto|
|DIAGRAMNET-51306|VSDX in PDF: il colore del testo sulle linee di collegamento viene modificato.|Insetto|
|DIAGRAMNET-51307|VSDX in PDF - elementi grafici mancanti.|Insetto|
|DIAGRAMNET-51313|La routine di apertura e salvataggio di un disegno VSDX genera un file di output corrotto.|Insetto|
|DIAGRAMNET-51314|VSDX a SVG - posizionamento errato del testo.|Insetto|
|DIAGRAMNET-51317|VSDX in PDF - manca il testo delle linee di collegamento.|Insetto|
|DIAGRAMNET-51318|VSDX in PDF: manca il testo formattato in grassetto delle forme rettangolari.|Insetto|
|DIAGRAMNET-51319|VSDM a SVG: l'operazione aritmetica ha provocato un errore di overflow.|Insetto|
|DIAGRAMNET-51320|Errore nell'elemento della forma durante il caricamento di un VSDM.|Insetto|
|DIAGRAMNET-51323|VSDM a SVG - mancano tutte le linee di collegamento.|Insetto|
|DIAGRAMNET-51324|VSDM in SVG - stile del bordo errato e colore del bordo di varie forme.|Insetto|
|DIAGRAMNET-51326|Problema dopo l'aggiunta di due commenti alla forma.|Insetto|
|DIAGRAMNET-51327|Problema dopo l'utilizzo del metodo "AddComment" durante l'aggiunta di commenti a varie forme.|Insetto|
|DIAGRAMNET-51328|Aspose Diagram importa erroneamente la forma nel documento.|Insetto|
|DIAGRAMNET-51330|VSDM a SVG: viene aggiunto un ulteriore testo di filigrana.|Insetto|
|DIAGRAMNET-51332|VSDM in SVG - rendering errato di un'icona.|Insetto|
|DIAGRAMNET-51334|VSDM in SVG - testo spostato nell'angolo in alto a destra.|Insetto|
|DIAGRAMNET-51335|VSDM in SVG - resa errata dell'immagine di sfondo.|Insetto|
|DIAGRAMNET-51337|VSD in HTML - formato non valido dell'errore della stringa di input.|Insetto|
## **Pubblico API e modifiche incompatibili con le versioni precedenti**
Di seguito è riportato un elenco di tutte le modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non compatibile con le versioni precedenti apportata a Aspose.Diagram for .NET. In caso di dubbi su qualsiasi modifica elencata, si prega di segnalarli in il[Aspose.Diagram forum di supporto](https://forum.aspose.com/c/diagram/17).
### **Aggiunge un membro Quality nella classe SVGSaveOptions**
Ottiene o imposta un valore che determina la qualità delle immagini generate.

{{< highlight "java" >}}

 string dataDir = @"c:\temp\";

// Load an existing drawing

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// specify SVG export settings

SVGSaveOptions options = new SVGSaveOptions();

// set image quality

options.Quality = 100;

// save drawing in the SVG format

diagram.Save(dataDir + "UseSVGSaveOptions_out.svg", options);

{{< /highlight >}}
### **Aggiunge il metodo ConnectShapesViaConnectorIndex nella classe Page**
Permette di collegare le forme utilizzando gli indici di connessione.

{{< highlight "java" >}}

 string dataDir = @"c:\temp\";

// Load an existing drawing

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// get shapes by ID

Aspose.Diagram.Shape shape1 = diagram.Pages[0].Shapes.GetShape(1);

Aspose.Diagram.Shape shape2 = diagram.Pages[0].Shapes.GetShape(2);

// add connector shapes

Aspose.Diagram.Shape connector1 = new Aspose.Diagram.Shape();

long connecter1Id = diagram.AddShape(connector1, "Dynamic connector", 0);

// connect shapes by index of conneecting points

diagram.Pages[0].ConnectShapesViaConnectorIndex(shape1.ID, 6, shape2.ID, 3, connecter1Id);

// save drawing

diagram.Save(dataDir + "UseSVGSaveOptions_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
### **Esempi di utilizzo**
Si prega di controllare l'elenco degli argomenti della guida aggiunti nei documenti Wiki Aspose.Diagram:

1. [Usa gli indici di connessione per connettere le forme](https://docs.aspose.com/diagram/net/add-retrieve-copy-and-read-visio-shape-data/#use-connection-indexes-to-connect-shapes)
1. [Uso delle opzioni di salvataggio SVG](https://docs.aspose.com/diagram/net/save-visio-document/)
