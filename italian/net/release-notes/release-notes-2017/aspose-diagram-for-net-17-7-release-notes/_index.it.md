---
title: Aspose.Diagram for .NET 17.7 Note di rilascio
type: docs
weight: 60
url: /it/net/aspose-diagram-for-net-17-7-release-notes/
---
{{% alert color="primary" %}} 

 Questa pagina contiene le note di rilascio per[Aspose.Diagram for .NET 17.7](https://www.nuget.org/packages/Aspose.Diagram/17.7.0).

{{% /alert %}} 
## **Miglioramenti e modifiche**

|**Chiave**|**Riepilogo**|**Categoria**|
|:- |:- |:- |
|DIAGRAMNET-51204|Il formato della carta della stampante viene modificato dopo il salvataggio di diagram.|Aumento|
|DIAGRAMNET-51230|Valori errati dei margini della pagina.|Aumento|
|DIAGRAMNET-51274|Aggiunto il supporto per l'inserimento di commenti a livello di forma.|Aumento|
|DIAGRAMNET-51297|Input VDX - lettura errata di SolutionXML.|Aumento|
|DIAGRAMNET-51061|Forme mancanti nella conversione di un VST in PNG.|Insetto|
|DIAGRAMNET-51262|Elementi di testo spostati durante la conversione di VSDM in SVG.|Insetto|
|DIAGRAMNET-51276|VSD in SVG - tutte le icone non sono visibili correttamente.|Insetto|
|DIAGRAMNET-51277|VSDM to SVG - Manca l'ombra delle forme.|Insetto|
|DIAGRAMNET-51279|Un carattere mancante nella conversione di VSD in PDF.|Insetto|
|DIAGRAMNET-51282|Alcuni file vdx sono danneggiati dopo il salvataggio.|Insetto|
|DIAGRAMNET-51284-|DiagramException si verifica durante il caricamento del file vsdx.|Insetto|
|DIAGRAMNET-51285|VSD in PNG: mancano tutti gli elementi di testo.|Insetto|
|DIAGRAMNET-51286|VSD in PNG - il rendering parziale di una forma.|Insetto|
|DIAGRAMNET-51288|Errore di valore del colore non valido durante la conversione di un VSDX in PNG.|Insetto|
|DIAGRAMNET-51289|L'icona dei commenti a livello di pagina non visualizza il testo.|Insetto|
|DIAGRAMNET-51290|Aspose.Diagram bug nel metodo SetWidth.|Insetto|
|DIAGRAMNET-51291|Uscita VSDX - disposizione errata durante l'impostazione diritta delle linee di collegamento.|Insetto|
|DIAGRAMNET-51292|Output VSDX - l'elemento di testo delle linee di collegamento è fuori posto.|Insetto|
|DIAGRAMNET-51293|VSDX in SVG: viene visualizzato un segno aggiuntivo insieme alle forme.|Insetto|
|DIAGRAMNET-51294|VSDM in SVG: viene visualizzato un segno aggiuntivo insieme alle forme.|Insetto|
## **Pubblico API e modifiche incompatibili con le versioni precedenti**
Di seguito è riportato un elenco di tutte le modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non compatibile con le versioni precedenti apportata a Aspose.Diagram for .NET. In caso di dubbi su qualsiasi modifica elencata, si prega di segnalarli in il[Aspose.Diagram forum di supporto](https://forum.aspose.com/c/diagram/17).
### **Il metodo AddComment viene aggiunto nella classe Page**
Un metodo AddComment sottoposto a overload, esposto dalla classe Page accetta un'istanza della classe Shape e una stringa di testo del commento.

{{< highlight "java" >}}

 // load diagram

Diagram diagram = new Diagram(@"c:\temp\Drawing1.vsdx");

// retrieve page by name

Aspose.Diagram.Page page = diagram.Pages.GetPage("Page-1");

// retrieve shape by ID

Aspose.Diagram.Shape shape = page.Shapes.GetShape(12);

page.AddComment(shape, "Hello");

// save diagram

diagram.Save(@"c:\temp\Drawing1.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
### **Esempi di utilizzo**
Si prega di controllare l'elenco degli argomenti della guida aggiunti nei documenti Wiki Aspose.Diagram:

1. [Aggiungere un commento a livello di forma nel disegno Visio](/diagram/it/net/working-with-comments/#workingwithcomments-addashape-levelcommentinvisiodrawing)
