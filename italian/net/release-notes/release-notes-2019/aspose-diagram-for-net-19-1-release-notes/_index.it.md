---
title: Aspose.Diagram for .NET 19.1 Note di rilascio
type: docs
weight: 120
url: /it/net/aspose-diagram-for-net-19-1-release-notes/
---
{{% alert color="primary" %}} 

Questa pagina contiene le note di rilascio per[Aspose.Diagram for .NET 19.1](https://www.nuget.org/packages/Aspose.Diagram/19.1.0)

{{% /alert %}} 
## **Miglioramenti e modifiche**

|**Chiave**|**Riepilogo**|**Categoria**|
|:- |:- |:- |
|DIAGRAMNET-51082|Aggiunto il supporto del disegno della polilinea|Aumento|
|DIAGRAMNET-51084|Aggiunto il supporto per il disegno di forme Bezier|Aumento|
|DIAGRAMNET-51231|Renderizza i commenti durante il salvataggio come immagine o HTML|Aumento|
|DIAGRAMNET-51597| Da VISIO a SVG - Utilizzo di elementi rettangolari<path> tag invece di<Rect>|Aumento|
|DIAGRAMNET-50764|VSDX lettura manca il valore del colore di varie forme|Insetto|
|DIAGRAMNET-51336|Risoluzione dei problemi nella versione Aspose.Diagram for .NET/Java|Insetto|
|DIAGRAMNET-51343|Output VSDX - la dimensione della forma non viene modificata|Insetto|
|DIAGRAMNET-51579|Blocco di lettura presente dopo la chiamata al metodo Save()|Insetto|
## **Pubblico API e modifiche incompatibili con le versioni precedenti**
Di seguito è riportato un elenco di tutte le modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non compatibile con le versioni precedenti apportata a Aspose.Diagram for .NET. In caso di dubbi su qualsiasi modifica elencata, si prega di segnalarli in il[Aspose.Diagram forum di supporto](https://forum.aspose.com/c/diagram/17).
### **Aggiunge DrawPolyline in Page**
Il processo di disegno della polilinea.

{{< highlight "java" >}}

 PointF[]ps = new PointF[]{new PointF(1, 1), new PointF(2, 2), new PointF(3.79949292203676f, 0) };

diagram.Pages[0].DrawPolyline(1, 1, 2, 2, ps);

{{< /highlight >}}
### **Aggiunge DrawBezier in Page**
Il processo di disegno bezier.

{{< highlight "java" >}}

 PointF[]ps = new PointF[]{new PointF(1, 1), new PointF(2, 2)};

diagram.Pages[0].DrawBezier(1, 1, 2, 2, ps);

{{< /highlight >}}
### **Aggiunge IsExportComments in ImageSaveOptions e HTMLSaveOptions**
Definisce se è necessario esportare o meno i commenti.

{{< highlight "java" >}}

 Aspose.Diagram.Saving.ImageSaveOptions io = new Aspose.Diagram.Saving.ImageSaveOptions(SaveFileFormat.PNG);

io.IsExportComments = true;

Aspose.Diagram.Saving.HTMLSaveOptions htmlo = new Aspose.Diagram.Saving.HTMLSaveOptions();

htmlo.IsExportComments = false;

{{< /highlight >}}
### **Aggiunge ExportElementAsRectTag in SVGSaveOptions**
Definisce se è necessario esportare gli elementi rettangolo come tag rect o meno.

{{< highlight "java" >}}

 var SVGso = new Aspose.Diagram.Saving.SVGSaveOptions();

SVGso.ExportGuideShapes = false;

SVGso.SaveFormat = Aspose.Diagram.SaveFileFormat.SVG;

SVGso.SVGFitToViewPort = true;

SVGso.ExportElementAsRectTag = true;

{{< /highlight >}}
