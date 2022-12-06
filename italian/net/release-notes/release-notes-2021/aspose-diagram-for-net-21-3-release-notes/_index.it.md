---
title: Aspose.Diagram for .NET 21.3 Note di rilascio
type: docs
weight: 10
url: /it/net/aspose-diagram-for-net-21-3-release-notes/
---
{{% alert color="primary" %}} 

Questa pagina contiene informazioni sulle note di rilascio per Aspose.Diagram for .NET 21.3.

{{% /alert %}} 
## **Miglioramenti e modifiche**

|**Chiave**|**Riepilogo**|**Categoria**|
|:- |:- |:- |
|DIAGRAMNET-51967|Riduci e stampa uno Diagram su una singola pagina|Aumento|
|DIAGRAMNET-51995|Problemi con i file Aspose.Diagram e Skyline Dataminer|Aumento|
|DIAGRAMNET-51996|Metodo CenterDrawing rispetto a page|Aumento|
|DIAGRAMNET-52000|IsIntersect non funziona correttamente per diagram|Aumento|
|DIAGRAMNET-52003|Incolla i connettori per modellarli usando le celle EndX e BeginX|Aumento|
|DIAGRAMNET-51565|VSDX to PDF - Shapes and Background Pattern is missing|Insetto|
|DIAGRAMNET-51992|L'esportazione da vsdx a svg produce una visualizzazione errata in IE, Chrome o Firefox|Insetto|
|DIAGRAMNET-51997|L'impostazione della licenza ha esito negativo con l'eccezione per Aspose.Diagram quando si usa la licenza Aspose.Total per tutte le API nella funzione di Azure|Insetto|
|DIAGRAMNET-51998|l'attributo geoms della forma è un elenco vuoto nella versione > 20.3.0|Insetto|
|DIAGRAMNET-51999|Impossibile aggiornare inheritProps|Insetto|
|DIAGRAMNET-52004|Exporting VSDX as SVG some edges are missing|Insetto|
|DIAGRAMNET-52005|Problema di conversione da VSD a VSDX|Insetto|
|DIAGRAMNET-52009|Shapes are missing while converting Visio to HTML|Insetto|

## ` `**Public API e modifiche incompatibili con le versioni precedenti**
` `Di seguito è riportato un elenco di eventuali modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non compatibile con le versioni precedenti apportata a Aspose.Diagram for .NET. il forum di supporto Aspose.Diagram.
### **Aggiunto ConnectShapesViaConnector nella pagina**
- Connect shapes via connector.

{{< highlight "java" >}}

diagram.Pages[pageNumber].ConnectShapesViaConnector(ampShape.ID, "Port7", wssShape.ID, "Port21", lineShape.ID);

{{< /highlight >}}
### **Aggiunge GlueShapeToConnectorBeginX nella pagina**
- Incolla la forma usando BeginX



{{< highlight "java" >}}

diagram.Pages[pageNumber].GlueShapeToConnectorBeginX(ampShape.ID, "Port7", lineShape.ID);

{{< /highlight >}}
### **Aggiunge GlueShapeToConnectorEndX nella pagina**
- Incolla la forma usando BeginX



{{< highlight "java" >}}

diagram.Pages[pageNumber].GlueShapeToConnectorEndX(wssShape.ID, "Port21", lineShape.ID);

{{< /highlight >}}
### **Aggiunge CenterDrawing in Page**
- Centra le forme di una pagina rispetto all'estensione della pagina.



{{< highlight "java" >}}

diagram.Pages[pageNumber].CenterDrawing();

{{< /highlight >}}
### **Aggiunge IsContain in Shape**
- Indica se questa forma contiene un'altra forma.



{{< highlight "java" >}}

OLE_Shape.IsContain(shape)

{{< /highlight >}}



