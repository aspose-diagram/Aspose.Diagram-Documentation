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
VSD to PDF conversion, the right text alignment of the shapes is not preserved

|**Chiave**|**Riepilogo**|**Categoria**|
|:- |:- |:- |
|DIAGRAMNET-51088|Recupera il numero di pagine errato di un numero VSD|Aumento|
|DIAGRAMNET-51731|Determina se una forma interseca un'altra forma in diagram|Aumento|
|DIAGRAMNET-51833|Aspose.Diagram 20.4: Visio La versione del documento non è supportata|Aumento|
|DIAGRAMNET-50361|VSD to PDF conversion, the right text alignment of the shapes is not preserved|Insetto|
|DIAGRAMNET-50955|The text items of diamond shapes are displaced on converting a VSDX to PNG|Insetto|
|DIAGRAMNET-50990|Plus, negative and dollar signs are not properly aligned on converting a VSDX to PNG|Insetto|
|DIAGRAMNET-51815|Una grande quantità di linee di testo in forma potrebbe creare ovviamente uno spostamento nella parte inferiore|Insetto|
|DIAGRAMNET-51820|La filigrana di valutazione non entra in una pagina|Insetto|
|DIAGRAMNET-51821|Visio in Html - problemi relativi a immagini e collegamenti nell'output|Insetto|
|DIAGRAMNET-51823|While convert Visio to SVG. Some images have issue Icon Missing|Insetto|
|DIAGRAMNET-51824|While convert Visio to SVG. Content Alignment wrong|Insetto|
|DIAGRAMNET-51826|While convert Visio to SVG. Icon Missing|Insetto|
|DIAGRAMNET-51827|While convert Visio to SVG - QR Code Missing|Insetto|
|DIAGRAMNET-51828|While convert Visio to SVG - PDF icon Missing|Insetto|
|DIAGRAMNET-51829|While convert Visio to SVG - Icon lost (Missing)|Insetto|
|DIAGRAMNET-51830|While convert Visio to SVG - Image lost (Missing)|Insetto|
|DIAGRAMNET-51831|Visio to HTML - image and links issues in the output|Insetto|
|DIAGRAMNET-51834|Visio save HTML - wrong connectors|Insetto|

## **Pubblico API e modifiche incompatibili con le versioni precedenti**
Di seguito è riportato un elenco di eventuali modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non compatibile con le versioni precedenti apportata a Aspose.Diagram for .NET. In caso di dubbi su qualsiasi modifica elencata, si prega di segnalarlo su il forum di supporto Aspose.Diagram.
### **Aggiunge IsIntersect in Shape**
- Indica se questa forma interseca un'altra forma.

{{< highlight "java" >}}

Shape s1 = diagram.Pages[0].Shapes.GetShape(1);

Shape s2 = diagram.Pages[0].Shapes.GetShape(2);

bool isIntersect = s1.IsIntersect(s2);

{{< /highlight >}}



