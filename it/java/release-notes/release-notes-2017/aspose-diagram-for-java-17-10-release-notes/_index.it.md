---
title: Aspose.Diagram for Java 17.10 Note di rilascio
type: docs
weight: 30
url: /it/java/aspose-diagram-for-java-17-10-release-notes/
---
{{% alert color="primary" %}} 

 Questa pagina contiene le note di rilascio per[Aspose.Diagram for Java 17.10](https://docs.aspose.com/diagram/java/aspose-diagram-for-java-17-10-release-notes/).

{{% /alert %}} 
## **Miglioramenti e modifiche**

|**Chiave**|**Riepilogo**|**Categoria**|
|:- |:- |:- |
|DIAGRAMJAVA-50560|JpegQuality non ha alcun effetto sul documento di output|Aumento|
|DIAGRAMJAVA-50548|Output VSDX - la linea di collegamento che passa attraverso il confine della forma|Insetto|
|DIAGRAMJAVA-50550|La sezione Trasformazione forma non conserva le formule|Insetto|
|DIAGRAMJAVA-50551|VSDX to PNG - incorrect rendering of the shape corners|Insetto|
|DIAGRAMJAVA-50552|The fill colors are not being preserved on saving a Visio drawing to SVG|Insetto|
|DIAGRAMJAVA-50553|Incorrect rendering of lines when saving a Visio drawing to SVG|Insetto|
|DIAGRAMJAVA-50554|The fill colors are not being preserved on saving a Visio drawing to SVG|Insetto|
|DIAGRAMJAVA-50555|Incorrect rendering of lines when saving a Visio drawing to SVG|Insetto|
|DIAGRAMJAVA-50559|da VSDM a VDX - le linee di collegamento non sono collegate alle forme|Insetto|
|DIAGRAMJAVA-50561|Il disegno VSDX è danneggiato dopo l'aggiunta dell'elemento SolutionXML|Insetto|
### **Aggiunge SameAsPdfConversionArea in ImageSaveOptions**
It specifies whether to save area in the same way as PDF.

{{< highlight "java" >}}

 String dataDir = "C:\\temp\\";

// load a drawing

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// specify image save options

ImageSaveOptions opts = new ImageSaveOptions(SaveFileFormat.PNG);

opts.setSameAsPdfConversionArea(true);

{{< /highlight >}}
