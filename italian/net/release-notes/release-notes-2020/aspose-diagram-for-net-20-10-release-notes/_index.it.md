---
title: Aspose.Diagram for .NET 20.10 Note di rilascio
type: docs
weight: 10
url: /it/net/aspose-diagram-for-net-20-10-release-notes/
---
{{% alert color="primary" %}}

Questa pagina contiene informazioni sulle note di rilascio per Aspose.Diagram for .NET 20.10.

{{% /alert %}}
## **Miglioramenti e modifiche**  ##

|**Chiave**|**Riepilogo**|**Categoria**|
|:- |:- |:- |
|DIAGRAMNET-51891|Visio in JPG - API richiede molto tempo per la conversione|Aumento|
|DIAGRAMNET-51902|Visio i file con versioni inferiori a 11 non sono supportati ad eccezione dell'apertura di VSS|Aumento|
|DIAGRAMNET-51906|Esporta VSDX in PDF: problemi con la larghezza della linea, l'immagine e il dimensionamento|Aumento|
|DIAGRAMNET-51929|Conversione da VSD a SVG: trasformazioni della matrice nel file SVG di output|Aumento|
|DIAGRAMNET-51931|Visio in PDF - API sta consumando una grande quantità di memoria e richiede molto tempo|Aumento|
|DIAGRAMNET-51936|[Cont.]da Visio a PDF - API sta consumando una grande quantità di memoria e richiede molto tempo|Aumento|
|DIAGRAMNET-51881|La posizione di 2 etichette non è corretta|Insetto|
|DIAGRAMNET-51907|Si è verificato un errore generico nell'eccezione GDI+ durante il rendering del file VSDX|Insetto|
|DIAGRAMMA-51926-|Aspose.Diagram 20.9: NullReferenceException durante la conversione di VDX in PNG|Insetto|
|DIAGRAMNET-51928|Conversione da VSD a SVG: Mancano del testo e delle frecce alla fine delle righe|Insetto|
|DIAGRAMNET-51932|Stili di forma persi dopo la conversione vsd –> vsdx|Insetto|
|DIAGRAMNET-51933|Il gradiente arresta il formato non conforme allo standard svg|Insetto|
|DIAGRAMNET-51934|Il riferimento non impostato su un'istanza di un oggetto.' quando si salvano forme VSS per file specifici|Insetto|
|DIAGRAMNET-51940|La posizione di 2 etichette non è corretta|Insetto|

## **Public API e modifiche incompatibili con le versioni precedenti**  ##
Di seguito è riportato un elenco di eventuali modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non compatibile con le versioni precedenti apportata a Aspose.Diagram for .NET. In caso di dubbi su qualsiasi modifica elencata, si prega di segnalarlo su il forum di supporto Aspose.Diagram.

 * Aggiunto IsExportScaleInMatrix in SVGSaveOptions - Definisce se è necessario esportare la scala nella matrice o meno.
```
Aspose.Diagram.Saving.SVGSaveOptions o = new Aspose.Diagram.Saving.SVGSaveOptions();
o.IsExportScaleInMatrix = false;
```
