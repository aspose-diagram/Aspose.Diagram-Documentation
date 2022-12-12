﻿---
title: Aspose.Diagram for .NET 17.10 Note di rilascio
type: docs
weight: 30
url: /it/net/aspose-diagram-for-net-17-10-release-notes/
---
{{% alert color="primary" %}} 

 Questa pagina contiene le note di rilascio per[Aspose.Diagram for .NET 17.10](https://www.nuget.org/packages/Aspose.Diagram/17.10.0).

{{% /alert %}} 
## **Miglioramenti e modifiche**

|**Chiave**|**Riepilogo**|**Categoria**|
|:- |:- |:- |
|DIAGRAMNET-51349|Add support of converting a drawing to image same the area as a PDF|Aumento|
|DIAGRAMNET-51352|Accesso ai file incorporati|Aumento|
|DIAGRAMNET-51085|Le formule vengono perse nella scheda dei controlli di Shapesheet al salvataggio in VSDX|Insetto|
|DIAGRAMNET-51094|Mantieni le impostazioni predefinite nella scheda di controllo sul posizionamento di una forma trapezoidale|Insetto|
|DIAGRAMNET-51355|VSDX to PDF - the text items are misplaced|Insetto|
|DIAGRAMNET-51356|VSDX to HTML - the text items are misplaced|Insetto|
|DIAGRAMNET-51357|Apri e salva la routine di VSDX - data mancante e modifica gli attributi della data delle annotazioni|Insetto|
|` `DIAGRAMNET-51358|Si è verificato un errore di puntatore nullo durante il caricamento del disegno VSDX|Insetto|
|DIAGRAMNET-51359|Errore nell'elenco degli autori dell'elemento dopo il caricamento di un VSDX|Insetto|
|DIAGRAMNET-51361|Da VSDX a VDX - il carattere del testo errato della forma|Insetto|
|DIAGRAMNET-51363|Routine di apertura e salvataggio di VSDX - La sezione delle schede si trasforma in un tag di chiusura automatica|Insetto|
|DIAGRAMNET-51365|VSD to PNG - incorrect layout of the shapes|Insetto|
|DIAGRAMNET-51367|VSD importazione disegno - un errore nell'elemento Master|Insetto|
|DIAGRAMNET-51368|VSD to PNG - an overflow error occurred|Insetto|
|DIAGRAMNET-51369|Da VSD a PDF - voci di testo fuori posto in fondo|Insetto|
|DIAGRAMNET-51371|VSDX a VSDX - vengono aggiunti ulteriori elementi di testo|Insetto|
|DIAGRAMNET-51373|Nella routine di apertura e salvataggio di un disegno VSDX manca un carattere di testo asiatico|Insetto|
## **Pubblico API e modifiche incompatibili con le versioni precedenti**
Di seguito è riportato un elenco di tutte le modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non compatibile con le versioni precedenti apportata a Aspose.Diagram for .NET. In caso di dubbi su qualsiasi modifica elencata, si prega di segnalarli in il[Aspose.Diagram forum di supporto](https://forum.aspose.com/c/diagram/17).
### **Aggiunge SameAsPdfConversionArea in ImageSaveOptions**
It specifies whether to save area in the same way as PDF.

{{< highlight "java" >}}

 string dataDir = @"C:\temp\";

// load a drawing

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// specify image save options

Aspose.Diagram.Saving.ImageSaveOptions opts = new Aspose.Diagram.Saving.ImageSaveOptions(SaveFileFormat.PNG);

opts.SameAsPdfConversionArea = true;

{{< /highlight >}}