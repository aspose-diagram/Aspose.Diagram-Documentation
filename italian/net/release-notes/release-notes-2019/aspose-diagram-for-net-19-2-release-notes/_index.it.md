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
|DIAGRAMNET-50009|The heart shape is mixed-up when exporting VSD drawing in PDF file format|Aumento|
|DIAGRAMNET-50010|VSD to PDF exports multiple zigzag lines with a concurrent point instead of a single curve line|Aumento|
|DIAGRAMNET-51257|Aggiunto il supporto della linea NBRS durante l'esportazione di un disegno|Aumento|
|DIAGRAMNET-51611|Impossibile ottenere correttamente Prop.Prompt.Value|Aumento|
|DIAGRAMNET-50355|Le linee curve vengono esportate come linee rette|Insetto|
|DIAGRAMNET-50702|VSDX to PDF export - the curved connectors turn into straight|Insetto|
|DIAGRAMNET-51348|VSDX to PDF - Incorrect rendering of letters|Insetto|
|DIAGRAMNET-51399|VSD to PNG - the curved line is converted to straight line|Insetto|
|DIAGRAMNET-51448|VSD to PNG - the ellipse is missing around the word network|Insetto|
|DIAGRAMNET-51472|VSD to PDF - the curved lines are being exported as straight lines|Insetto|
|DIAGRAMNET-51507|VSDX to PNG - filled oval shapes are missing in the output|Insetto|
|DIAGRAMNET-51508|VSDX to SVG - filled oval shapes are missing in the output|Insetto|
|DIAGRAMNET-51537|VSDX to SVG - curved connectors become straight connectors when VSDX is rendered to PDF|Insetto|
|DIAGRAMNET-51540|I bordi della forma sono stati modificati come quadrati dopo la conversione|Insetto|
|DIAGRAMNET-51577|VISIO to SVG - output is not correct|Insetto|
|DIAGRAMNET-51592|Le linee curve si trasformano in linee rette durante la conversione|Insetto|
|DIAGRAMNET-51600|Le linee rette diventano punte quando si salva un diagram come un altro formato|Insetto|
|DIAGRAMNET-51604|VSDX to PDF conversion error - black ellipses|Insetto|
|DIAGRAMNET-51605|Aggiorna i riferimenti API e aggiungi dettagli sul metodo Shape.SetAngle()|Insetto|
|DIAGRAMNET-51610|VSDX to SVG - text is not rendering in the correct font|Insetto|
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
