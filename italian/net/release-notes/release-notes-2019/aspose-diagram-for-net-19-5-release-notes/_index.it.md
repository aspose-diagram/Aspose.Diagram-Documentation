---
title: Aspose.Diagram for .NET 19.5 Note di rilascio
type: docs
weight: 80
url: /it/net/aspose-diagram-for-net-19-5-release-notes/
---
{{% alert color="primary" %}} 

Questa pagina contiene le note di rilascio per[Aspose.Diagram for .NET 19.5](https://www.nuget.org/packages/Aspose.Diagram/19.5.0)

{{% /alert %}} 
## **Miglioramenti e modifiche**

|**Chiave**|**Riepilogo**|**Categoria**|
|:- |:- |:- |
|DIAGRAMNET-51606|Rileva e rimuovi temi, dati grafici e stili inutilizzati dai diagrammi Visio|Aumento|
|DIAGRAMNET-51637|La forma nidificata all'interno di un contenitore raggruppato non viene conservata correttamente|Aumento|
|DIAGRAMNET-51638|Impossibile ottenere Prop.Value.Val quando il valore è un numero intero|Aumento|
|DIAGRAMNET-51640|Determina gli stili inutilizzati in un file Visio|Aumento|
|DIAGRAMNET-50051|Conversione da VSDX a PDF, freccia di connessione mancante insieme a testo fuori posto|Insetto|
|DIAGRAMNET-50052|Conversione da VSDX a PDF, forme con colore del testo del carattere errato|Insetto|
|DIAGRAMNET-51179|Ombreggiatura errata su un pulsante e-mail durante la conversione di un VSDM in SVG|Insetto|
|DIAGRAMNET-51190|Visualizzazione errata della forma con collegamento ipertestuale durante il salvataggio di un VDX in SVG|Insetto|
|DIAGRAMNET-51194|Rendering errato di un'icona durante il salvataggio di un VDX in SVG|Insetto|
|DIAGRAMNET-51254|Ombreggiatura errata nella barra superiore durante la conversione di un VSDM in SVG|Insetto|
|DIAGRAMNET-51618|Visio in PDF - Formato data errato e dati mancanti|Insetto|
|DIAGRAMNET-51628|Valore di testo errato per il testo predefinito eliminato nei diagrammi .vsdx|Insetto|
|DIAGRAMNET-51634|Visio in SVG - Z-index errato di alcune forme nell'output|Insetto|
|DIAGRAMNET-51636|Visio in SVG: non tutti gli elementi del percorso vengono esportati correttamente come elementi rect|Insetto|
|DIAGRAMNET-51641|L'immagine aggiuntiva viene visualizzata quando si salva nuovamente Visio con API|Insetto|
## **Pubblico API e modifiche incompatibili con le versioni precedenti**
Di seguito è riportato un elenco di tutte le modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non compatibile con le versioni precedenti apportata a Aspose.Diagram for .NET. In caso di dubbi su qualsiasi modifica elencata, segnalarli a il[Aspose.Diagram forum di supporto](https://forum.aspose.com/c/diagram/17).
### **Aggiunge GetUnusedStyles in Diagram**
Ottieni stili inutilizzati.

{{< highlight "java" >}}

  StyleSheetCollection unused = diagram.GetUnusedStyles();

{{< /highlight >}}
