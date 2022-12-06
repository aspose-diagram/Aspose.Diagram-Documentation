---
title: Aspose.Diagram for Java 17.10 Sürüm Notları
type: docs
weight: 30
url: /tr/java/aspose-diagram-for-java-17-10-release-notes/
---
{{% alert color="primary" %}} 

 Bu sayfa için sürüm notları içerir[Aspose.Diagram for Java 17.10](https://docs.aspose.com/diagram/java/aspose-diagram-for-java-17-10-release-notes/).

{{% /alert %}} 
## **İyileştirmeler ve Değişiklikler**

|**Anahtar**|**Özet**|**Kategori**|
|:- |:- |:- |
|DIAGRAMJAVA-50560|JpegQuality çıktı belgesi üzerinde herhangi bir etki yapmaz|Artırma|
|DIAGRAMJAVA-50548|Çıktı VSDX - şeklin sınırından geçen bağlantı hattı|Böcek|
|DIAGRAMJAVA-50550|Şekil Dönüştürme bölümü formülleri korumaz|Böcek|
|DIAGRAMJAVA-50551|VSDX'den PNG'ye - şekil köşelerinin yanlış oluşturulması|Böcek|
|DIAGRAMJAVA-50552|Visio çizimi SVG'ye kaydedilirken dolgu renkleri korunmuyor|Böcek|
|DIAGRAMJAVA-50553|Visio çizimini SVG'ye kaydederken çizgilerin yanlış oluşturulması|Böcek|
|DIAGRAMJAVA-50554|Visio çizimi SVG'ye kaydedilirken dolgu renkleri korunmuyor|Böcek|
|DIAGRAMJAVA-50555|Visio çizimini SVG'ye kaydederken çizgilerin yanlış oluşturulması|Böcek|
|DIAGRAMJAVA-50559|VSDM ila VDX - bağlantı hatları şekillere bağlı değil|Böcek|
|DIAGRAMJAVA-50561|VSDX çizimi, SolutionXML öğesi eklendikten sonra bozuk|Böcek|
### **ImageSaveOptions'a SameAsPdfConversionArea ekler**
Alanın PDF ile aynı şekilde kaydedilip kaydedilmeyeceğini belirtir.

{{< highlight "java" >}}

 String dataDir = "C:\\temp\\";

// load a drawing

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// specify image save options

ImageSaveOptions opts = new ImageSaveOptions(SaveFileFormat.PNG);

opts.setSameAsPdfConversionArea(true);

{{< /highlight >}}
