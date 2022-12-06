---
title: Aspose.Diagram for .NET 20.5 Note di rilascio
type: docs
weight: 30
url: /it/net/aspose-diagram-for-net-20-5-release-notes/
---
{{% alert color="primary" %}} 

Questa pagina contiene informazioni sulle note di rilascio per Aspose.Diagram for .NET 20.5.

{{% /alert %}} 
## **Miglioramenti e modifiche**
VSD alla conversione in PDF, il corretto allineamento del testo delle forme non viene mantenuto

|**Chiave**|**Riepilogo**|**Categoria**|
|:- |:- |:- |
|DIAGRAMNET-51088|Recupera il numero di pagine errato di un numero VSD|Aumento|
|DIAGRAMNET-51731|Determina se una forma interseca un'altra forma in diagram|Aumento|
|DIAGRAMNET-51833|Aspose.Diagram 20.4: Visio La versione del documento non è supportata|Aumento|
|DIAGRAMNET-50361|VSD alla conversione in PDF, il corretto allineamento del testo delle forme non viene mantenuto|Insetto|
|DIAGRAMNET-50955|Gli elementi di testo delle forme a diamante vengono spostati durante la conversione di un VSDX in PNG|Insetto|
|DIAGRAMNET-50990|Inoltre, i segni negativi e del dollaro non sono correttamente allineati durante la conversione di un VSDX in PNG|Insetto|
|DIAGRAMNET-51815|Una grande quantità di linee di testo in forma potrebbe creare ovviamente uno spostamento nella parte inferiore|Insetto|
|DIAGRAMNET-51820|La filigrana di valutazione non entra in una pagina|Insetto|
|DIAGRAMNET-51821|Visio in Html - problemi relativi a immagini e collegamenti nell'output|Insetto|
|DIAGRAMNET-51823|Mentre converti Visio in SVG. Alcune immagini presentano problemi con l'icona mancante|Insetto|
|DIAGRAMNET-51824|Mentre converti Visio in SVG. Allineamento del contenuto errato|Insetto|
|DIAGRAMNET-51826|Mentre converti Visio in SVG. Icona mancante|Insetto|
|DIAGRAMNET-51827|Mentre converti Visio in SVG - Codice QR mancante|Insetto|
|DIAGRAMNET-51828|Durante la conversione di Visio in SVG - icona PDF mancante|Insetto|
|DIAGRAMNET-51829|Durante la conversione di Visio in SVG - Icona persa (mancante)|Insetto|
|DIAGRAMNET-51830|Durante la conversione di Visio in SVG - Immagine persa (mancante)|Insetto|
|DIAGRAMNET-51831|Visio in HTML: problemi con immagini e collegamenti nell'output|Insetto|
|DIAGRAMNET-51834|Visio salva HTML - connettori sbagliati|Insetto|

## **Pubblico API e modifiche incompatibili con le versioni precedenti**
Di seguito è riportato un elenco di eventuali modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non compatibile con le versioni precedenti apportata a Aspose.Diagram for .NET. In caso di dubbi su qualsiasi modifica elencata, si prega di segnalarlo su il forum di supporto Aspose.Diagram.
### **Aggiunge IsIntersect in Shape**
- Indica se questa forma interseca un'altra forma.

{{< highlight "java" >}}

Shape s1 = diagram.Pages[0].Shapes.GetShape(1);

Shape s2 = diagram.Pages[0].Shapes.GetShape(2);

bool isIntersect = s1.IsIntersect(s2);

{{< /highlight >}}



