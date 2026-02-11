---
title: Visio'e Filigran Ekle
type: docs
weight: 10
url: /tr/java/add-watermark-to-visio/
keywords: watermark, visi
description: Java Diagram API kullanarak visio'e filigran nasıl eklenir.
---
## **Diagram oluşturma**
 Aspose.Diagram for Java, Microsoft Office Otomasyon olmadan kendi uygulamalarınız içinden Microsoft Visio diyagramlarını okumanızı ve oluşturmanızı sağlar. Yeni belgeler oluştururken ilk adım, bir diagram oluşturmaktır. Ardından[şekiller ve bağlayıcılar ekleyin](https://docs.aspose.com/diagram/java/add-retrieve-copy-and-read-visio-shape-data/)diagram'i oluşturmak için.[Diagram](http://www.aspose.com/api/java/diagram/com.aspose.diagram/diagram) yeni bir diagram oluşturmak için sınıf.
### **Programlama Örneği**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(CreateDiagram.class);
// Create directory if it is not already present.
File file = new File(dataDir);
if (!file.exists())
	file.mkdir();
// initialize a new Diagram
Diagram diagram = new Diagram();
// save in the VSDX format
diagram.save(dataDir + "CreateDiagram_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```

Bu örnek şu şekilde çalışır:

1. Diagram sınıfından bir nesne oluşturun.
1. Sayfada visio'e filigran ekleyin
1. Diagram sınıf nesnesinin Kaydetme yöntemini çağırın ve ayrıca tam dosya yolunu ve DiagramSaveOptions nesnesini iletin.
### **Filigran ekle Programlama Örneği**
Aşağıdaki örnek kod, Visio diagram'de filigranın nasıl ekleneceğini gösterir.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(AddWatermarkToVisio.class);   
        
// load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get page by name
Page page = diagram.getPages().getPage("Page-1");

double pinx = page.getPageSheet().getPageProps().getPageWidth().getValue() / 2;
double piny = page.getPageSheet().getPageProps().getPageHeight().getValue() / 2;
double width = page.getPageSheet().getPageProps().getPageWidth().getValue();
double height =page.getPageSheet().getPageProps().getPageHeight().getValue();
    
//Add watermark
Shape shape = page.addText(pinx, piny, width, height, "Test text","Calibri","#a5a5a5",0.25);

// save diagram
diagram.save(dataDir + "ApplyFontOnText_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
