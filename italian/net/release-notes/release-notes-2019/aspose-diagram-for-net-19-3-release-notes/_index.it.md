---
title: Aspose.Diagram for .NET 19.3 Note di rilascio
type: docs
weight: 100
url: /it/net/aspose-diagram-for-net-19-3-release-notes/
---
{{% alert color="primary" %}} 

Questa pagina contiene le note di rilascio per[Aspose.Diagram for .NET 19.3](https://www.nuget.org/packages/Aspose.Diagram/19.3.0)

{{% /alert %}} 
## **Miglioramenti e modifiche**

|**Chiave**|**Riepilogo**|**Categoria**|
|:- |:- |:- |
|DIAGRAMNET-50930|Aggiunto il supporto per il recupero delle directory dei font comuni sui sistemi operativi|Aumento|
|DIAGRAMNET-51614|Ottieni il valore di tutti gli oggetti di scena per una forma|Aumento|
|DIAGRAMNET-50214|VSD to PDF conversion - Curved lines become a straight line|Insetto|
|DIAGRAMNET-50240|VSD to PDF conversion - Wrong layout of dynamic connectors|Insetto|
|DIAGRAMNET-50703|VSDX to PDF export - Missing a dynamic connector|Insetto|
|DIAGRAMNET-50704|VSD to PDF export - Meta type shapes turn into messy symbols|Insetto|
|DIAGRAMNET-51535|VSDM to SVG - Font changes from Sans to Serif in SVG|Insetto|
|DIAGRAMNET-51574|VSDX to PNG - Some shapes are rendered incorrect in output PNG|Insetto|
|DIAGRAMNET-51608|A capo automatico non funziona come previsto|Insetto|
|DIAGRAMNET-51609|Le forme vengono spostate sul lato sinistro quando Diagram viene copiato in PowerPoint Slide|Insetto|
|DIAGRAMNET-51617|Visio to PDF - External Data Driven values are not showing correctly|Insetto|
|DIAGRAMNET-51619|Visio to PDF - Incorrect Date/Time/Distance in PDF|Insetto|
|DIAGRAMNET-51621|Visio to PDF - Background image is distorted and the extra page is present in PDF|Insetto|
## **Pubblico API e modifiche incompatibili con le versioni precedenti**
Di seguito è riportato un elenco di tutte le modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non compatibile con le versioni precedenti apportata a Aspose.Diagram for .NET. In caso di dubbi su qualsiasi modifica elencata, segnalarli a il[Aspose.Diagram forum di supporto](https://forum.aspose.com/c/diagram/17).
### **Aggiunge GetDefaultFontDir in Diagram**
Ottieni il percorso della cartella Font predefiniti

{{< highlight "java" >}}

  string str =  diagram.GetDefaultFontDir();

{{< /highlight >}}
