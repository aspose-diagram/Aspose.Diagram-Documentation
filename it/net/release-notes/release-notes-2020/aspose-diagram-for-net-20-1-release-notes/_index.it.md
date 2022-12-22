---
title: Aspose.Diagram for .NET 20.1 Note di rilascio
type: docs
weight: 70
url: /it/net/aspose-diagram-for-net-20-1-release-notes/
---
{{% alert color="primary" %}} 

Questa pagina contiene informazioni sulle note di rilascio per Aspose.Diagram for .NET 20.1.

{{% /alert %}} 
## **Miglioramenti e modifiche**

|**Chiave**|**Riepilogo**|**Categoria**|
|:- |:- |:- |
|DIAGRAMNET-51198|Shade on hyperlink button is not rendered correctly on saving VSDM to SVG|Aumento|
|DIAGRAMNET-51526|VSDX to PDF - Gradient fill for arrowheads lost in resultant PDF|Aumento|
|DIAGRAMNET-51539|The gradient in shapes has lost in output SVG|Aumento|
|DIAGRAMNET-50705|VSD to SVG export - Meta type shapes turn into messy symbols|Insetto|
|DIAGRAMNET-51664|Il file viene danneggiato dopo aver rimosso il tema inutilizzato|Insetto|
|DIAGRAMNET-51665|Le immagini vengono mostrate come X dopo aver rimosso i temi inutilizzati|Insetto|
|DIAGRAMNET-51684|Durante la rimozione di forme e stili principali inutilizzati, solo l'immagine presenta un problema|Insetto|
|DIAGRAMNET-51726|Immagine di sfondo mancante (PowerPoint viene aggiunto in VISIO) durante la rimozione di forme e stili principali inutilizzati|Insetto|
|DIAGRAMNET-51737|Visio in Html - Problema relativo alle dimensioni dell'immagine|Insetto|
|DIAGRAMNET-51743|Rimozione di informazioni private da Visio - il problema relativo alle dimensioni del documento Visio|Insetto|
|DIAGRAMNET-51745|Strano errore si verifica nell'applicazione WPF durante la conversione da VSD a VSDX|Insetto|

## **Public API e modifiche incompatibili con le versioni precedenti**
- Pagine aggiunte a LoadOptions: specifica l'indice delle pagine da caricare.



{{< highlight "java" >}}

Aspose.Diagram.LoadOptions options = new Aspose.Diagram.LoadOptions(LoadFileFormat.VSDX);

options.Pages = new ArrayList();

options.Pages.Add(0);

{{< /highlight >}}

- Aggiunto SetFontSources in FontConfigs - Imposta le origini dei caratteri

{{< highlight "java" >}}

Aspose.Diagram.MemoryFontSource sc1 = new Aspose.Diagram.MemoryFontSource(b);

Aspose.Diagram.MemoryFontSource sc2 = new Aspose.Diagram.MemoryFontSource(b);

Aspose.Diagram.MemoryFontSource[]sc = new Aspose.Diagram.MemoryFontSource[]{ sc1, sc2 };

Aspose.Diagram.FontConfigs.SetFontSources(sc); 

{{< /highlight >}}
