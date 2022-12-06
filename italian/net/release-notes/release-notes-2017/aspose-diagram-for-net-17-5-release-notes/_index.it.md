---
title: Aspose.Diagram for .NET 17.5 Note di rilascio
type: docs
weight: 80
url: /it/net/aspose-diagram-for-net-17-5-release-notes/
---
{{% alert color="primary" %}} 

 Questa pagina contiene le note di rilascio per[Aspose.Diagram for .NET 17.5](https://www.nuget.org/packages/Aspose.Diagram/17.5.0).

{{% /alert %}} 
## **Miglioramenti e modifiche**

|**Chiave**|**Riepilogo**|**Categoria**|
|:- |:- |:- |
|DIAGRAMNET-51104|Aggiungi il supporto delle proprietà di rotazione 3D della forma|Nuova caratteristica|
|DIAGRAMNET-51229|Il processo di apertura e salvataggio di VSDM rimuove SolutionXML|Aumento|
|DIAGRAMNET-50283|Conversione da VTX a HTML, effetto a doppia linea sugli elementi di testo delle forme|Insetto|
|DIAGRAMNET-51195|Rendering errato dell'icona di una busta durante il salvataggio di un VDX in SVG|Insetto|
|DIAGRAMNET-51196|Allineamento del testo errato durante il salvataggio di un VDX in SVG|Insetto|
|DIAGRAMNET-51225|Recupera un valore di calendario errato dei dati Shape per VSDM|Insetto|
|DIAGRAMNET-51226|Il salvataggio nel flusso HTML non incorpora risorse esterne|Insetto|
|DIAGRAMNET-51227|Impossibile impostare il valore TimeSaved di VSDM|Insetto|
|DIAGRAMNET-51228|Gli elementi di testo vengono spostati durante l'impostazione dei dati della forma in VSDM|Insetto|
|DIAGRAMNET-51234|Impossibile rimuovere e aggiungere un master con lo stesso nome in VSDM|Insetto|
|DIAGRAMNET-51235|Il processo di apertura e salvataggio di VSDM rimuove il file vbaProjectSignature.bin|Insetto|
|DIAGRAMNET-51236|Apri e salva il processo di VSDM cambia il file XML della soluzione|Insetto|
|DIAGRAMNET-51237|Impossibile salvare i valori Del e NoQuickDrag di Geoms in un VSDM|Insetto|
|DIAGRAMNET-51238|Imposta il valore TimeSaved durante il salvataggio di un disegno Visio|Insetto|
|DIAGRAMNET-51239|Il processo di apertura e salvataggio di VSDM rimuove parte della relazione di Solution XML|Insetto|
|DIAGRAMNET-51240|Testo spostato durante la conversione di un VSD in PDF|Insetto|
|DIAGRAMNET-51242|Impossibile aggiungere dati di forma a varie forme in VSDM|Insetto|
|DIAGRAMNET-51243|Valore UFEV cella utente non salvato correttamente in VSDM|Insetto|
|DIAGRAMNET-51244|Errore xml pagina duplicata durante la copia di pagine da due disegni VSDM|Insetto|
|DIAGRAMNET-51247|L'area non stampabile è inclusa anche quando si converte un VSD in PDF|Insetto|
## **Pubblico API e modifiche incompatibili con le versioni precedenti**
Di seguito è riportato un elenco di tutte le modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non compatibile con le versioni precedenti apportata a Aspose.Diagram for .NET. In caso di dubbi su qualsiasi modifica elencata, si prega di segnalarli in il[Aspose.Diagram forum di supporto](https://forum.aspose.com/c/diagram/17).
### **Aggiunge il membro ThreeDFormat nella classe Shape**
La classe ThreeDFormat consente agli sviluppatori di recuperare o impostare le proprietà di rotazione 3D di una forma.

{{< highlight "java" >}}

 // Load diagram

Diagram diagram = new Diagram(@"c:\temp\3DShape_Rotation.vsdx");

// get page by name

Aspose.Diagram.Page page = diagram.Pages.GetPage("Page-1");

// get shape by ID

Aspose.Diagram.Shape shape = page.Shapes.GetShape(1);

// set RotationXAngle property, 

// all other properties are added in ThreeDFormat class

shape.ThreeDFormat.RotationXAngle.Value = 2.61;

// save diagram to VSDX format

diagram.Save(@"c:\temp\3DShape_Rotation_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
### **Esempi di utilizzo**
Si prega di controllare l'elenco degli argomenti della guida aggiunti nei documenti Wiki Aspose.Diagram:

1. [Modifica le proprietà di rotazione 3D in Shapesheet](/diagram/it/net/3d-rotation-effects-in-a-visio-drawing/#id-3drotationeffectsinavisiodrawing-set3drotationpropertiesinshapesheet)
