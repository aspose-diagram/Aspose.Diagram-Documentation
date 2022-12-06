---
title: Aspose.Diagram for .NET Note sulla versione 18.10
type: docs
weight: 30
url: /it/net/aspose-diagram-for-net-18-10-release-notes/
---
{{% alert color="primary" %}} 

 Questa pagina contiene le note di rilascio per[Aspose.Diagram for .NET 18.10](https://www.nuget.org/packages/Aspose.Diagram/18.10.0).

{{% /alert %}} 
## **Miglioramenti e modifiche**

|**Chiave**|**Riepilogo**|**Categoria**|
|:- |:- |:- |
|DIAGRAMNET-51527|Images get lost after converting VSDM to SVG|Aumento|
|DIAGRAMNET-51532|VSD to PDF - Shadow of the image is not correct|Aumento|
|DIAGRAMNET-51536|Shadow of the shape got removed after VSDX to SVG Conversion|Aumento|
|DIAGRAMNET-51544|Underline is removed from text after converting VSDM to SVG|Aumento|
|DIAGRAMNET-51558|Implementare Getter per Shape.ConnectorsType|Aumento|
|DIAGRAMNET-51520|VDX to HTML - Extra Lines are appearing in the output|Insetto|
|DIAGRAMNET-51521|Il carattere in diagram ottiene le modifiche dopo aver salvato VSD come VSDX|Insetto|
|DIAGRAMNET-51523|VSDX to SVG - Arrow heads are missing|Insetto|
|DIAGRAMNET-51524|VSDM to SVG - Blue Crosses appeared in output file|Insetto|
|DIAGRAMNET-51525|Shape of decision changes from diamond to square while VSDM to SVG conversion|Insetto|
|DIAGRAMNET-51528|Shape of decision changes from diamond to square while VSDM to SVG conversion|Insetto|
|DIAGRAMNET-51529|VSDM to SVG - Dotted lines converted into filled lines|Insetto|
|DIAGRAMNET-51531|Shapes are being shifted to right side after converting VSDX to SVG|Insetto|
|DIAGRAMNET-51533|Red Crosses appeared after VISIO to SVG Conversion|Insetto|
|DIAGRAMNET-51534|Il punto rosso è apparso nell'angolo in basso a sinistra della forma|Insetto|
|DIAGRAMNET-51538|Pictures are lost after converting VSDX to PDF|Insetto|
|DIAGRAMNET-51541|Text is being invisible after converting VSDX to SVG|Insetto|
|DIAGRAMNET-51542|Text got deleted after VSDX to SVG Conversion|Insetto|
|DIAGRAMNET-51543|Time and date format is changed after VSDM TO SVG|Insetto|
|DIAGRAMNET-51545|VSDX to SVG - Text is wrapped in output|Insetto|
|DIAGRAMNET-51546|VSDX to SVG - Text is wrapped in output|Insetto|
|DIAGRAMNET-51547|VSDX to SVG - Text is wrapped in output|Insetto|
|DIAGRAMNET-51548|VSDX to SVG - Text is wrapped in output|Insetto|
|DIAGRAMNET-51551|Impossibile ottenere il colore corretto del tema delle forme|Insetto|
|DIAGRAMNET-51552|Reversed arrowheads showing in SVG conversion|Insetto|
|DIAGRAMNET-51559|Text Resizing issue while converting VSDM to SVG|Insetto|
|DIAGRAMNET-51560|Connector Lines become thin after converting to SVG|Insetto|
## **Pubblico API e modifiche incompatibili con le versioni precedenti**
Di seguito è riportato un elenco di tutte le modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non compatibile con le versioni precedenti apportata a Aspose.Diagram for .NET. In caso di dubbi su qualsiasi modifica elencata, si prega di segnalarli in il[Aspose.Diagram forum di supporto](https://forum.aspose.com/c/diagram/17).
#### **Aggiunta InheritLine in Shape**
Contiene i valori di formattazione della linea per la forma ereditata dallo stile padre e dalla forma principale.

{{< highlight "java" >}}

 		Line line = shape.InheritLine;

{{< /highlight >}}


#### **Aggiunto GetConnectorsType in Shape**
Ottieni il tipo di connettori

{{< highlight "java" >}}

 Shapes.GetShape(1).GetConnectorsType()

{{< /highlight >}}

