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
|DIAGRAMNET-51264|L'ombra delle forme è nera quando si converte un VSDM in SVG|Aumento|
|DIAGRAMNET-51270|Impossibile vedere una forma di VSDX nel Visualizzatore Visio|Aumento|
|DIAGRAMNET-51273|Visualizzazione errata della forma nel Visualizzatore Visio 2013|Aumento|
|DIAGRAMNET-51249|L'aspetto errato della linea curva che collega in VSDM|Insetto|
|DIAGRAMNET-51250|Un'ulteriore parentesi sinistra viene aggiunta nel testo durante la conversione di un VSD in PDF|Insetto|
|DIAGRAMNET-51251|La dimensione dell'icona viene ridotta durante la conversione di un VSDM in SVG|Insetto|
|DIAGRAMNET-51253|Colore errato del testo e dei bordi nelle forme durante la conversione di un VSDM in SVG|Insetto|
|DIAGRAMNET-51255|Un'immagine in fondo è stata schiacciata durante la conversione di un VSDM in SVG|Insetto|
|DIAGRAMNET-51258|Apri e salva la routine di VSDM - la lunghezza delle pareti viene modificata|Insetto|
|DIAGRAMNET-51259|Apri e salva la routine di VSDM - la lunghezza delle pareti viene modificata|Insetto|
|DIAGRAMNET-51260|Si è verificato un errore di indice fuori intervallo durante la chiamata al metodo di layout della classe Diagram|Insetto|
|DIAGRAMNET-51263|Un ulteriore tag di colore rosso appare durante la conversione di un VSDM in SVG|Insetto|
|DIAGRAMNET-51265|Il carattere del testo del titolo viene modificato durante la conversione di un VSDM in SVG|Insetto|
|DIAGRAMNET-51266|La dimensione dell'immagine di sfondo è ridotta alla conversione di un VSDM in SVG|Insetto|
|DIAGRAMNET-51267|La dimensione di un'icona viene ridotta durante la conversione di un VSDM in SVG|Insetto|
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
