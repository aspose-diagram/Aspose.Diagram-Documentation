---
title: Aspose.Diagram for .NET 19.8 Note di rilascio
type: docs
weight: 50
url: /it/net/aspose-diagram-for-net-19-8-release-notes/
---
{{% alert color="primary" %}} 

Questa pagina contiene le note di rilascio per[Aspose.Diagram for .NET 19.8](https://www.nuget.org/packages/Aspose.Diagram/19.8.0)

{{% /alert %}} 
## **Miglioramenti e modifiche**

|**Chiave**|**Riepilogo**|**Categoria**|
|:- |:- |:- |
|DIAGRAMNET-50334|Aggiungi il supporto di codici VBA / macro (aggiungi - modifica - elimina)|Aumento|
|DIAGRAMNET-51083|Aggiunto il supporto del disegno Spline|Aumento|
|DIAGRAMNET-51676|Visio to HTML - output contains filename in it|Aumento|
|DIAGRAMNET-50263|Impossibile impostare la posizione del testo del connettore come formule|Insetto|
|DIAGRAMNET-50284|VTX to HTML conversion, shapes fill color is not preserved|Insetto|
|DIAGRAMNET-50432|VDX to PDF conversion, Diagram.setFontDirs method use only first font over the whole diagram|Insetto|
|DIAGRAMNET-50463|VSDX to PDF conversion, missing or incomplete shapes rendering|Insetto|
|DIAGRAMNET-51033|The network shapes are not being preserved on converting a VSDX to PDF|Insetto|
|DIAGRAMNET-51303|VSDX to PDF - the color of text on connecting lines is changed|Insetto|
|DIAGRAMNET-51663|Si verifica un'eccezione non gestita durante la conversione da VSD a VSDX|Insetto|
|DIAGRAMNET-51664|Il file viene danneggiato dopo aver rimosso un tema inutilizzato|Insetto|
|DIAGRAMNET-51665|Le immagini vengono mostrate come X dopo aver rimosso i temi inutilizzati|Insetto|
|DIAGRAMNET-51667|Durante la rimozione degli stili solo un'immagine ha un problema|Insetto|
|DIAGRAMNET-51668|Da VISIO a JPG - l'immagine di output non è nel formato corretto|Insetto|
|DIAGRAMNET-51671|Durante la rimozione di forme e stili principali inutilizzati, solo l'immagine presenta un problema|Insetto|
|DIAGRAMNET-51672|Immagini perse durante il caricamento e il salvataggio|Insetto|
|DIAGRAMNET-51677|Visio to HTML - Link in generated HTML does not work|Insetto|
|DIAGRAMNET-51678|Visio to HTML - Date Format incorrect when saving as HTML|Insetto|
|DIAGRAMNET-51679|Visio to PDF - Several formatting errors in PDF|Insetto|
## **Pubblico API e modifiche incompatibili con le versioni precedenti**
Di seguito è riportato un elenco di tutte le modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non compatibile con le versioni precedenti apportata a Aspose.Diagram for .NET. In caso di dubbi su qualsiasi modifica elencata, segnalarli a il[Aspose.Diagram forum di supporto](https://forum.aspose.com/c/diagram/17).
### **Aggiunge DrawSpline in Page**
Il seguente frammento di codice mostra come disegnare spline:

{{< highlight "java" >}}

 PointF[]ps = new PointF[]{ new PointF(0, 0.3270758925347308f), 

                             new PointF(0.2926845121364643f, 0.3581517392187368f), 

                             new PointF(0.6526026522346893f, 0.4640748257705201f), 

                             new PointF(1f, 0.327075892534732f) };

                             diagram.Pages[0].DrawSpline(1, 1, 2, 2, ps);

{{< /highlight >}}
### **Aggiunge SaveTitle in HTMLSaveOptions**
Il seguente frammento di codice definisce se si desidera salvare o meno il titolo:

{{< highlight "java" >}}

 Aspose.Diagram.Saving.HTMLSaveOptions options = new Aspose.Diagram.Saving.HTMLSaveOptions();

options.SaveTitle = false;

{{< /highlight >}}




