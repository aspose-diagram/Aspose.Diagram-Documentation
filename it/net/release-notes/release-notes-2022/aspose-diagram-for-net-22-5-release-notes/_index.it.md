---
title: Aspose.Diagram for .NET 22.5 Note di rilascio
type: docs
weight: 23
url: /it/net/aspose-diagram-for-net-22-5-release-notes/
---
{{% alert color="primary" %}} 

Questa pagina contiene informazioni sulle note di rilascio per Aspose.Diagram for .NET 22.5.

{{% /alert %}} 
## **Miglioramenti e modifiche**

|**Chiave**|**Riepilogo**|**Categoria**|
|:- |:- |:- |
|DIAGRAMNET-52802|Formula/valore che non aggiorna i campi|Aumento|
|DIAGRAMNET-52803|VSDX to HTML: Output file not saving in Async method until program completely executes|Aumento|
|DIAGRAMNET-52793|API non funziona con una versione di licenza 22.4 valida|Insetto|
|DIAGRAMNET-52806|Shifted indent in PDF from VSDX|Insetto|
|DIAGRAMNET-52807|Il testo presente nella tabella viene rimosso durante la conversione del file .vsdx in pdf [CONT.]|Insetto|
|DIAGRAMNET-52808|Problem converting VSDX to PDF [CONT.]|Insetto|
|DIAGRAMNET-52810|Visio le forme salvate come immagini sono sbagliate|Insetto|
|DIAGRAMNET-52811|Shapes are missing after saving Visio to HTML|Insetto|

## **Pubblico API e modifiche incompatibili con le versioni precedenti**
Di seguito è riportato un elenco di eventuali modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non compatibile con le versioni precedenti apportata a Aspose.Diagram for .NET. In caso di dubbi su qualsiasi modifica elencata, si prega di segnalarlo su il forum di supporto Aspose.Diagram.
### **Aggiunge DisplayValue in Field**
- Ottiene il valore della stringa formattata di questo campo.

{{< highlight "java" >}}
String str = shape.Fields[0].DisplayValue;
{{< /highlight >}}

### **Aggiunge InheritParas in Shape**
- Contiene i paragrafi per la forma ereditata dallo stile genitore e dal master

{{< highlight "java" >}}
ParaCollection paras = shape.InheritParas;
Console.WriteLine(paras[0].HorzAlign.Value);
{{< /highlight >}}