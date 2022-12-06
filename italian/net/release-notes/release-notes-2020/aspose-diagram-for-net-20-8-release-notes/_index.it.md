---
title: Aspose.Diagram for .NET 20.8 Note di rilascio
type: docs
weight: 14
url: /it/net/aspose-diagram-for-net-20-8-release-notes/
---
{{% alert color="primary" %}}

Questa pagina contiene informazioni sulle note di rilascio per Aspose.Diagram for .NET 20.8.

{{% /alert %}}
## **Miglioramenti e modifiche**  ##

|**Chiave**|**Riepilogo**|**Categoria**|
|:- |:- |:- |
|DIAGRAMNET-51886|Crea la possibilità di inserire oggetti Ole come parole, celle, diapositive, ecc. allo Diagram nella singola forma con sia i dati dell'oggetto che l'immagine di anteprima al suo interno.|Aumento|
|DIAGRAMNET-51888|Visio in PDF - API richiede molto tempo per la conversione|Aumento|
|DIAGRAMNET-51889|Salvataggio in pdf in loop per più di 20 minuti|Aumento|
|DIAGRAMNET-51893|Attributo viewBox mancante dopo la conversione da VSDX a SVG|Aumento|
|DIAGRAMNET-51851|VSDX in PDF - alcune icone mancano e alcune non sono visualizzate correttamente|Insetto|
|DIAGRAMNET-51873|VSDX in PDF: il contenuto è a sinistra nel PDF di output|Insetto|
|DIAGRAMNET-51874|VSDX in PDF: nell'output mancano contenuto e righe|Insetto|
|DIAGRAMNET-51876|VSDX in PNG: alcune forme non sono corrette nell'output|Insetto|
|DIAGRAMNET-51879|Visio in PDF - l'output non è corretto|Insetto|
|DIAGRAMNET-51894|System.NullReferenceException durante il caricamento del file diagram|Insetto|
|DIAGRAMNET-51895|Impossibile recuperare i dati della proprietà del gruppo come SelectionModel, DisplayMode|Insetto|

## **Public API e modifiche incompatibili con le versioni precedenti**  ##
Di seguito è riportato un elenco di eventuali modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non compatibile con le versioni precedenti apportata a Aspose.Diagram for .NET. In caso di dubbi su qualsiasi modifica elencata, si prega di segnalarlo su il forum di supporto Aspose.Diagram.

####  Metodo aggiunto AddShape in Page ####
```
Diagram diagram = new Diagram();

// Get page object by index
Aspose.Diagram.Page page0 = diagram.Pages[0];
// set pinX, pinY, width and height
double pinX = 2, pinY = 2, width = 4, hieght = 3;

// Import ole as Visio shape word
page0.AddShape(pinX, pinY, width, hieght, new FileStream( "imageword.emf", FileMode.OpenOrCreate), new FileStream( "wordsource.doc", FileMode.OpenOrCreate));
```
