---
title: Aspose.Diagram for Java 17.12 Sürüm Notları
type: docs
weight: 10
url: /tr/java/aspose-diagram-for-java-17-12-release-notes/
---
{{% alert color="primary" %}} 

 Bu sayfa için sürüm notları içerir[Aspose.Diagram for Java 17.12](https://docs.aspose.com/diagram/java/aspose-diagram-for-java-17-12-release-notes/).

{{% /alert %}} 
## **İyileştirmeler ve Değişiklikler**

|**Anahtar**|**Özet**|**Kategori**|
|:- |:- |:- |
|DIAGRAMJAVA-50290|Visio şeklini PDF'ye dönüştürmek için tek API'i sağlayın|Artırma|
|DIAGRAMJAVA-50291|Visio şeklini HTML'ye dönüştürmek için tek API sağlayın|Artırma|
|DIAGRAMJAVA-50572|Shape.connectedShapes yöntemi giden düğümleri almıyor|Artırma|
|DIAGRAMJAVA-50391|Ters çevrilmiş resimler ve oklar, bir VSD'in SVG'ye dönüştürülmesinde oluşturulur.|Böcek|
|DIAGRAMJAVA-50570|VSD'den PDF'ye - ek metin öğeleri eklendi|Böcek|
|DIAGRAMJAVA-50571|VSDX'i içe aktar - şekil öğesinde bir hata oluştu|Böcek|
|DIAGRAMJAVA-50573|VSD'den SVG'ye - bir grup şeklinin satırları eksik|Böcek|
|DIAGRAMJAVA-50575|VSD'den SVG'ye - metin öğeleri eksik|Böcek|
|DIAGRAMJAVA-50576|VDX prosedürünü içe aktar, bir sayfa öğesi hatası veriyor|Böcek|
### **Shape sınıfına Copy üyesi ekler**
Kopyalama üyesi, bu şekli klonlamak için parametre olarak bir hedef şekil örneği alır.

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

Shape newShape = new Shape();

// copy diagram

newShape.copy(diagram.getPages().get(0).getShapes().get(0));

newShape.setID(3);

newShape.getXForm().getPinX().setValue(1);

newShape.getXForm().getPinY().setValue(1);

{{< /highlight >}}
### **Shape sınıfında toPdf üyesi ekler**
toPdf üyesi, bir şekli PDF formatına dönüştürür.

{{< highlight "java" >}}

 String dataDir = "C:\\temp\\";

// import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// save a shape in the PDF format

diagram.getPages().get(0).getShapes().getShape(59).toPdf(dataDir + "out.pdf");

{{< /highlight >}}
### **Shape sınıfındaki toHTML üyesine ekler**
toHTML üyesi, bir şekli PDF formatına dönüştürür.

{{< highlight "java" >}}

 String dataDir = "C:\\temp\\";

// import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

HTMLSaveOptions hs = new HTMLSaveOptions();

// save a shape in the PDF format

diagram.getPages().get(0).getShapes().getShape(59).toHTML(dataDir + "out.pdf", hs);

{{< /highlight >}}
### **Kullanım Örnekleri**
Lütfen Aspose.Diagram Wiki belgelerine eklenen yardım konularının listesini kontrol edin:

1. [Visio Shape'i başka bir Shape örneğine kopyalama](https://docs.aspose.com/diagram/java/working-with-visio-shape-data/#use-connection-indexes-to-connect-shapes-programming-sample)
1. [Visio Shape'i PDF'ye dönüştür](https://docs.aspose.com/diagram/java/convert-a-visio-shape-to-pdf/)
1. [Visio Shape'i HTML'ye dönüştür](https://docs.aspose.com/diagram/java/convert-a-visio-shape-to-html/)


