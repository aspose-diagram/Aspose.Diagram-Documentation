---
title: Aspose.Diagram for .NET 19.2 Note di rilascio
type: docs
weight: 110
url: /it/net/aspose-diagram-for-net-19-2-release-notes/
---
{{% alert color="primary" %}} 

Questa pagina contiene le note di rilascio per[Aspose.Diagram for .NET 19.2](https://www.nuget.org/packages/Aspose.Diagram/19.2.0)

{{% /alert %}} 
## **Miglioramenti e modifiche**

|**Chiave**|**Riepilogo**|**Categoria**|
|:- |:- |:- |
|DIAGRAMNET-50009|La forma del cuore viene confusa durante l'esportazione del disegno VSD in formato file PDF|Aumento|
|DIAGRAMNET-50010|VSD in PDF esporta più linee a zig-zag con un punto simultaneo invece di una singola linea curva|Aumento|
|DIAGRAMNET-51257|Aggiunto il supporto della linea NBRS durante l'esportazione di un disegno|Aumento|
|DIAGRAMNET-51611|Impossibile ottenere correttamente Prop.Prompt.Value|Aumento|
|DIAGRAMNET-50355|Le linee curve vengono esportate come linee rette|Insetto|
|DIAGRAMNET-50702|VSDX in esportazione PDF - i connettori curvi diventano diritti|Insetto|
|DIAGRAMNET-51348|VSDX in PDF - Resa errata delle lettere|Insetto|
|DIAGRAMNET-51399|VSD in PNG: la linea curva viene convertita in linea retta|Insetto|
|DIAGRAMNET-51448|VSD in PNG: manca l'ellisse attorno alla rete di parole|Insetto|
|DIAGRAMNET-51472|VSD in PDF - le linee curve vengono esportate come linee rette|Insetto|
|DIAGRAMNET-51507|VSDX in PNG: nell'output mancano forme ovali riempite|Insetto|
|DIAGRAMNET-51508|VSDX in SVG: nell'output mancano forme ovali riempite|Insetto|
|DIAGRAMNET-51537|Da VSDX a SVG: i connettori curvi diventano connettori diritti quando VSDX viene visualizzato in PDF|Insetto|
|DIAGRAMNET-51540|I bordi della forma sono stati modificati come quadrati dopo la conversione|Insetto|
|DIAGRAMNET-51577|Da VISIO a SVG - l'output non è corretto|Insetto|
|DIAGRAMNET-51592|Le linee curve si trasformano in linee rette durante la conversione|Insetto|
|DIAGRAMNET-51600|Le linee rette diventano punte quando si salva un diagram come un altro formato|Insetto|
|DIAGRAMNET-51604|Errore di conversione da VSDX a PDF - ellissi nere|Insetto|
|DIAGRAMNET-51605|Aggiorna i riferimenti API e aggiungi dettagli sul metodo Shape.SetAngle()|Insetto|
|DIAGRAMNET-51610|VSDX in SVG: il testo non viene visualizzato con il carattere corretto|Insetto|
## **Pubblico API e modifiche incompatibili con le versioni precedenti**
Di seguito è riportato un elenco di tutte le modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non compatibile con le versioni precedenti apportata a Aspose.Diagram for .NET. In caso di dubbi su qualsiasi modifica elencata, segnalarli a il[Aspose.Diagram forum di supporto](https://forum.aspose.com/c/diagram/17).
### **Aggiungi InheritProps in Shape**
Contiene gli oggetti di scena per la forma ereditata dalla forma principale.

{{< highlight "java" >}}

  foreach (Aspose.Diagram.Prop prop in shape.InheritProps)

{

    Console.WriteLine(prop.Name);

    Console.WriteLine(prop.Label.Value);

    Console.WriteLine(prop.Prompt.Value);

    Console.WriteLine(prop.Type.Value.ToString());

    Console.WriteLine(prop.Value.Val);

    Console.WriteLine(prop.Format.Value);

}

{{< /highlight >}}
