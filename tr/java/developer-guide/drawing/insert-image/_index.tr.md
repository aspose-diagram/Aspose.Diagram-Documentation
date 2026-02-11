---
title: Resim ekle
type: docs
weight: 70
url: /tr/java/drawing/insert-image
description: Bu bölüm, visio numaralı sayfaya Aspose.Diagram ile nasıl resim ekleneceğini açıklar. Resim eklemek ve pdf, svg, html, resim, xps ve diğer formatlarda kaydetmek için java kullanımını destekler.
---
 bu[Sayfa](https://reference.aspose.com/diagram/java/com.aspose.diagram/page)nesne, ön plan sayfasının veya arka plan sayfasının çizim alanını temsil eder. Tarafından sunulan Pages özelliği[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) class, Aspose.Diagram.Page nesnelerinin koleksiyonunu destekler.

## **Visio'e Resim Ekle**
JAVA için Aspose.Diagram API, geliştiricilerin bir sayfaya resim şekli eklemesine izin verir. Aşağıdaki kod örneği, bir Visio çizimine nasıl resim ekleneceğini gösterir.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getSharedDataDir(AddImageToPage.class) + "Pages/";

// load an existing Visio
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get a particular page
Page page = diagram.getPages().getPage("Page-1");
double pinX = 3, pinY = 3, width = 4, hieght = 4;
File file = new File("image.png"); 
FileInputStream fis = new FileInputStream(file); 
page.addShape(pinX, pinY, width, hieght, fis);

// Save the Visio diagram
diagram.save(dataDir + "AddImageToPage_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}


## **SVG'e Resim Ekle**
JAVA için Aspose.Diagram API, geliştiricilerin bir sayfaya resim şekli eklemesine izin verir. Aşağıdaki kod örneği, Visio çizimine nasıl resim ekleneceğini ve SVG formatında nasıl kaydedileceğini gösterir.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getSharedDataDir(AddImageToPage.class) + "Pages/";

// load an existing Visio
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get a particular page
Page page = diagram.getPages().getPage("Page-1");
double pinX = 3, pinY = 3, width = 4, hieght = 4;
File file = new File("image.png"); 
FileInputStream fis = new FileInputStream(file); 
page.addShape(pinX, pinY, width, hieght, fis);

// Save the Visio diagram
diagram.save(dataDir + "AddImageToPage_Out.svg", SaveFileFormat.SVG);

{{< /highlight >}}


## **PNG'e Resim Ekle**
JAVA için Aspose.Diagram API, geliştiricilerin bir sayfaya resim şekli eklemesine izin verir. Aşağıdaki kod örneği, Visio çizimine nasıl resim ekleneceğini ve PNG formatında nasıl kaydedileceğini gösterir.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getSharedDataDir(AddImageToPage.class) + "Pages/";

// load an existing Visio
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get a particular page
Page page = diagram.getPages().getPage("Page-1");
double pinX = 3, pinY = 3, width = 4, hieght = 4;
File file = new File("image.png"); 
FileInputStream fis = new FileInputStream(file); 
page.addShape(pinX, pinY, width, hieght, fis);

// Save the Visio diagram
diagram.save(dataDir + "AddImageToPage_Out.png", SaveFileFormat.PNG);

{{< /highlight >}}


## **PDF'e Resim Ekle**
JAVA için Aspose.Diagram API, geliştiricilerin bir sayfaya resim şekli eklemesine izin verir. Aşağıdaki kod örneği, Visio çizimine nasıl resim ekleneceğini ve PDF formatında nasıl kaydedileceğini gösterir.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getSharedDataDir(AddImageToPage.class) + "Pages/";

// load an existing Visio
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get a particular page
Page page = diagram.getPages().getPage("Page-1");
double pinX = 3, pinY = 3, width = 4, hieght = 4;
File file = new File("image.png"); 
FileInputStream fis = new FileInputStream(file); 
page.addShape(pinX, pinY, width, hieght, fis);

// Save the Visio diagram
diagram.save(dataDir + "AddImageToPage_Out.pdf", SaveFileFormat.PDF);

{{< /highlight >}}


## **HTML'e Resim Ekle**
JAVA için Aspose.Diagram API, geliştiricilerin bir sayfaya resim şekli eklemesine izin verir. Aşağıdaki kod örneği, Visio çizimine nasıl resim ekleneceğini ve HTML formatında nasıl kaydedileceğini gösterir.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getSharedDataDir(AddImageToPage.class) + "Pages/";

// load an existing Visio
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get a particular page
Page page = diagram.getPages().getPage("Page-1");
double pinX = 3, pinY = 3, width = 4, hieght = 4;
File file = new File("image.png"); 
FileInputStream fis = new FileInputStream(file); 
page.addShape(pinX, pinY, width, hieght, fis);
// initialize PDF save options
HTMLSaveOptions options = new HTMLSaveOptions();
// Save the Visio diagram
diagram.save(dataDir + "ExportOfHiddenVisioPagesToHTML_Out.html", options);

{{< /highlight >}}

