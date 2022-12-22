---
title: Aspose.Diagram for .NET Note sulla versione 18.11
type: docs
weight: 20
url: /it/net/aspose-diagram-for-net-18-11-release-notes/
---
{{% alert color="primary" %}} 

Questa pagina contiene le note di rilascio per[Aspose.Diagram for .NET 18.11](https://www.nuget.org/packages/Aspose.Diagram/18.11.0)

{{% /alert %}} 
## **Miglioramenti e modifiche**

|**Chiave**|**Riepilogo**|**Categoria**|
|:- |:- |:- |
|DIAGRAMNET-50410|MilestoneHelper - Aggiunto il supporto del setter del formato della stringa di data personalizzato|Aumento|
|DIAGRAMNET-51568|Add an option to set ViewBox in SaveOptions for SVG|Aumento|
|DIAGRAMNET-51580|Aspose.Diagram creates SVG with guidelines and MS Visio does not|Aumento|
|DIAGRAMNET-51556|Il metodo Shape.ToImage non genera immagini corrette|Insetto|
|DIAGRAMNET-51557|Il metodo Shape.ToImage restituisce immagini vuote in caso di copia della pagina|Insetto|
|DIAGRAMNET-51570|Il metodo Shape.ToImage non genera immagini corrette|Insetto|
|DIAGRAMNET-51576|VSDX to PDF - Missing Text Blocks|Insetto|
|DIAGRAMNET-51578|VSDX all'immagine risulta in StackOverFlowException|Insetto|
## **Pubblico API e modifiche incompatibili con le versioni precedenti**
Di seguito è riportato un elenco di tutte le modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non compatibile con le versioni precedenti apportata a Aspose.Diagram for .NET. In caso di dubbi su qualsiasi modifica elencata, si prega di segnalarli in il[Aspose.Diagram forum di supporto](https://forum.aspose.com/c/diagram/17).
### **Aggiunge SVGFitToViewPort in SVGSaveOptions**
If this property is true, the generated SVG will fit to view port.

{{< highlight "java" >}}

 SVGSaveOptions option = new SVGSaveOptions();

option.SVGFitToViewPort = true;

SVGSaveOptions option = new SVGSaveOptions();

option.SVGFitToViewPort = true;

{{< /highlight >}}
### **Aggiunge ExportGuideShapes in RenderingSaveOptions**
Definisce se è necessario esportare o meno le forme guida.

{{< highlight "java" >}}

 Aspose.Diagram.Saving.SVGSaveOptions o = new SVGSaveOptions();

o.ExportGuideShapes = false;

{{< /highlight >}}
### **Aggiunge DateFormatString in MilestoneHelper**
DateFormat stringa di forma

{{< highlight "java" >}}

 milestoneHelper.DateFormatString = "yyyy/mm/dd";

{{< /highlight >}}
