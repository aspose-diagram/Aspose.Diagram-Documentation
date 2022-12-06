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
|DIAGRAMNET-51527|Le immagini si perdono dopo aver convertito VSDM in SVG|Aumento|
|DIAGRAMNET-51532|VSD in PDF - L'ombreggiatura dell'immagine non è corretta|Aumento|
|DIAGRAMNET-51536|L'ombra della forma è stata rimossa dopo la conversione da VSDX a SVG|Aumento|
|DIAGRAMNET-51544|La sottolineatura viene rimossa dal testo dopo la conversione di VSDM in SVG|Aumento|
|DIAGRAMNET-51558|Implementare Getter per Shape.ConnectorsType|Aumento|
|DIAGRAMNET-51520|VDX in HTML: nell'output vengono visualizzate righe aggiuntive|Insetto|
|DIAGRAMNET-51521|Il carattere in diagram ottiene le modifiche dopo aver salvato VSD come VSDX|Insetto|
|DIAGRAMNET-51523|VSDX to SVG - Mancano le punte delle frecce|Insetto|
|DIAGRAMNET-51524|VSDM in SVG - Le croci blu sono apparse nel file di output|Insetto|
|DIAGRAMNET-51525|La forma della decisione cambia da diamante a quadrato durante la conversione da VSDM a SVG|Insetto|
|DIAGRAMNET-51528|La forma della decisione cambia da diamante a quadrato durante la conversione da VSDM a SVG|Insetto|
|DIAGRAMNET-51529|VSDM in SVG - Linee tratteggiate convertite in linee piene|Insetto|
|DIAGRAMNET-51531|Le forme vengono spostate sul lato destro dopo la conversione di VSDX in SVG|Insetto|
|DIAGRAMNET-51533|Le croci rosse sono apparse dopo la conversione da VISIO a SVG|Insetto|
|DIAGRAMNET-51534|Il punto rosso è apparso nell'angolo in basso a sinistra della forma|Insetto|
|DIAGRAMNET-51538|Le immagini vengono perse dopo la conversione di VSDX in PDF|Insetto|
|DIAGRAMNET-51541|Il testo è invisibile dopo la conversione di VSDX in SVG|Insetto|
|DIAGRAMNET-51542|Il testo è stato eliminato dopo la conversione da VSDX a SVG|Insetto|
|DIAGRAMNET-51543|Il formato di data e ora viene modificato dopo VSDM TO SVG|Insetto|
|DIAGRAMNET-51545|VSDX in SVG: il testo viene inserito nell'output|Insetto|
|DIAGRAMNET-51546|VSDX in SVG: il testo viene inserito nell'output|Insetto|
|DIAGRAMNET-51547|VSDX in SVG: il testo viene inserito nell'output|Insetto|
|DIAGRAMNET-51548|VSDX in SVG: il testo viene inserito nell'output|Insetto|
|DIAGRAMNET-51551|Impossibile ottenere il colore corretto del tema delle forme|Insetto|
|DIAGRAMNET-51552|Punte di freccia invertite mostrate nella conversione SVG|Insetto|
|DIAGRAMNET-51559|Problema di ridimensionamento del testo durante la conversione di VSDM in SVG|Insetto|
|DIAGRAMNET-51560|Le linee di connessione diventano sottili dopo la conversione in SVG|Insetto|
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

