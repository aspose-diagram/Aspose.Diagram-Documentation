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
|DIAGRAMNET-51888|Visio to PDF - API is taking long time for conversion|Aumento|
|DIAGRAMNET-51889|Salvataggio in pdf in loop per più di 20 minuti|Aumento|
|DIAGRAMNET-51893|Missing viewBox attribute after VSDX to SVG conversion|Aumento|
|DIAGRAMNET-51851|VSDX to PDF - some icons are missing and some not rendered correctly|Insetto|
|DIAGRAMNET-51873|VSDX to PDF - Content is out on left in the output PDF|Insetto|
|DIAGRAMNET-51874|VSDX to PDF - content and lines are missing in the output|Insetto|
|DIAGRAMNET-51876|VSDX to PNG - some shapes are incorrect in the output|Insetto|
|DIAGRAMNET-51879|Visio to PDF - output is not correct|Insetto|
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
