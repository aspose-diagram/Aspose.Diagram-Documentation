---
title: Aspose.Diagram for .NET 17.6 Note di rilascio
type: docs
weight: 70
url: /it/net/aspose-diagram-for-net-17-6-release-notes/
---
{{% alert color="primary" %}} 

 Questa pagina contiene le note di rilascio per[Aspose.Diagram for .NET 17.6](https://www.nuget.org/packages/Aspose.Diagram/17.6.0).

{{% /alert %}} 
## **Miglioramenti e modifiche**

|**Chiave**|**Riepilogo**|**Categoria**|
|:- |:- |:- |
|DIAGRAMNET-51264|The shadow of shapes is black on converting a VSDM to SVG|Aumento|
|DIAGRAMNET-51270|Impossibile vedere una forma di VSDX nel Visualizzatore Visio|Aumento|
|DIAGRAMNET-51273|Visualizzazione errata della forma nel Visualizzatore Visio 2013|Aumento|
|DIAGRAMNET-51249|L'aspetto errato della linea curva che collega in VSDM|Insetto|
|DIAGRAMNET-51250|An additional left parenthesis is added in text on converting a VSD to PDF|Insetto|
|DIAGRAMNET-51251|The size of the icon is downgraded on converting a VSDM to SVG|Insetto|
|DIAGRAMNET-51253|Incorrect color of text and borders in shapes when converting a VSDM to SVG|Insetto|
|DIAGRAMNET-51255|An image at the bottom has been squashed on converting a VSDM to SVG|Insetto|
|DIAGRAMNET-51258|Apri e salva la routine di VSDM - la lunghezza delle pareti viene modificata|Insetto|
|DIAGRAMNET-51259|Apri e salva la routine di VSDM - la lunghezza delle pareti viene modificata|Insetto|
|DIAGRAMNET-51260|Si è verificato un errore di indice fuori intervallo durante la chiamata al metodo di layout della classe Diagram|Insetto|
|DIAGRAMNET-51263|An additional red color tag appears on converting a VSDM to SVG|Insetto|
|DIAGRAMNET-51265|The font of title text is changed on converting a VSDM to SVG|Insetto|
|DIAGRAMNET-51266|The size of background image is reduced to converting a VSDM to SVG|Insetto|
|DIAGRAMNET-51267|An icon size is downgraded on converting a VSDM to SVG|Insetto|
|DIAGRAMNET-51268|Recupera il valore di trasparenza errato di un'immagine dal disegno VSDM|Insetto|
|DIAGRAMNET-51269|Aggiungi la protezione della virtualizzazione|Insetto|
## **Pubblico API e modifiche incompatibili con le versioni precedenti**
Di seguito è riportato un elenco di tutte le modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non compatibile con le versioni precedenti apportata a Aspose.Diagram for .NET. In caso di dubbi su qualsiasi modifica elencata, si prega di segnalarli in il[Aspose.Diagram forum di supporto](https://forum.aspose.com/c/diagram/17).
### **Aggiunge il membro RefreshData nella classe Shape**
Il metodo RefreshData dell'istanza della classe Shape aggiorna i dati della forma, inclusi XForm, TextXForm, Connection e Geom, dopo aver modificato il testo della forma o altro.

{{< highlight "java" >}}

 // Load diagram

Diagram diagram = new Diagram(@"c:\temp\3DShape_Rotation.vsdx");

// get page by name

Aspose.Diagram.Page page = diagram.Pages.GetPage("Page-1");

// get shape by ID

Aspose.Diagram.Shape shape = page.Shapes.GetShape(1);

// set PinX and PinY values

shape.XForm.PinX.Value = 5;

shape.XForm.PinY.Value = 5;

// save diagram to VSDX format

diagram.Save(@"c:\temp\3DShape_Rotation_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
