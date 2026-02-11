---
title:  Visio'i diğer formatlara dönüştürün
linktitle:  Visio'i diğer formatlara dönüştürün
type: docs
weight: 40
url: /tr/net/convert-visio-to-other-files/
description: Bu konu, Aspose.Diagram'in Visio'i SVG,XPS,XML,XAML biçimlerine dönüştürmeye nasıl izin verdiğini gösterir. VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM'i SVG,XPS,15,0761,XML'ye dönüştürün.
---
## **XML'e Aktar**
### **İhracat Microsoft Visio Çizimi PDF'e**
Kod örnekleri, Microsoft Visio Çiziminin C# kullanılarak PDF'e nasıl aktarılacağını gösterir.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_LoadSaveConvert();

// Call the diagram constructor to load a VSD diagram
Diagram diagram = new Diagram(dataDir + "ExportToPDF.vsd");

MemoryStream pdfStream = new MemoryStream();
// Save diagram
diagram.Save(pdfStream, SaveFileFormat.PDF);

// Create a PDF file
FileStream pdfFileStream = new FileStream(dataDir + "ExportToPDF_out.pdf", FileMode.Create, FileAccess.Write);
pdfStream.WriteTo(pdfFileStream);
pdfFileStream.Close();

pdfStream.Close();

// Display Status.
System.Console.WriteLine("Conversion from vsd to pdf performed successfully.");

{{< /highlight >}}
```

 Bu makalede, bir Microsoft Visio diagram kullanarak XML'e nasıl dışa aktarılacağı açıklanmaktadır.[Aspose.Diagram for .NET](http://www.aspose.com/.net/diagram-component.aspx) API.

- VDX, bir XML diagram tanımlar.
- VTX, bir XML şablonu tanımlar.
- VSX, bir XML şablonunu tanımlar.

 bu[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) class' yapıcıları bir diagram'i okur ve Save yöntemi, bir diagram'i farklı bir dosya biçiminde kaydetmek veya dışa aktarmak için kullanılır. Bu makaledeki kod parçacıkları, bir Visio dosyasını şuraya kaydetmek için Kaydet yönteminin nasıl kullanılacağını gösterir:[VDX](https://docs.aspose.com/diagram/net/save-visio-document/), [VTX](https://docs.aspose.com/diagram/net/save-visio-document/) ve[VSX](https://docs.aspose.com/diagram/net/save-visio-document/).

Aşağıdaki resim, aşağıdaki kod parçacıklarında dışa aktarılan diagram'i göstermektedir. Dışa aktarılan dosya, her kod parçacığından önce gösterilir.

|**A Microsoft Visio diagram ihraç edilmek üzere.**|
|:- |
|![yapılacaklar:resim_alternatif_Metin](how-to-convert-a-visio-diagram_3.png)|

### **VSD'i VDX'e aktar**
VDX, diyagramları Microsoft Visio dışındaki ürünlerin okuyabileceği bir biçimde kaydetmenizi sağlayan şema tabanlı bir XML dosya biçimidir. Yazılım uygulamaları arasında diyagramları aktarmak ve düzenlenebilir verileri tutmak için kullanışlı bir formattır.

Bir VSD diagram'i VDX'e aktarmak için:

1. Diagram sınıfının bir örneğini oluşturun.
1. Visio çizim dosyasını VDX'e yazmak için Diagram sınıfının Save yöntemini çağırın.

|**Dışa aktarılan VDX dosyası.**|
|:- |
|![yapılacaklar:resim_alternatif_Metin](how-to-convert-a-visio-diagram_4.png)|

### **VSD'den VSX'e dışa aktarma**
VSX, diagram'in oluşturulduğu temel nesneler olan şablonları tanımlamak için bir XML formatıdır. Visio dosyası VSX'e dönüştürüldüğünde, yalnızca şablonlar dışa aktarılır.

Bir VSD diagram'i VSX'e aktarmak için:

- Diagram sınıfının bir örneğini oluşturun.
- Visio çizim dosyasını VSX'e yazmak için Diagram sınıfının Save yöntemini çağırın.
### **VSD'i VTX'e aktar**
TVX, bir şablon dosyasının XML temsilidir ve belgenin ayarlarını saklar.

Bir VSD diagram'i VTX'e aktarmak için:

1. Diagram sınıfının bir örneğini oluşturun.
1. Visio çizim dosyasını VTX biçiminde yazmak için diagram sınıfının Save yöntemini çağırın.
### **Microsoft Visio Çizimi XML'e Aktar**
Kod örnekleri, Microsoft Visio Çiziminin C# kullanılarak XML'e nasıl aktarılacağını gösterir.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_LoadSaveConvert();
            
/* 1. Exporting VSDX to VDX */
// Call the diagram constructor to load diagram from a VSD file
Diagram diagram = new Diagram(dataDir + "ExportToXML.vsd");

// Save input VSD as VDX
diagram.Save(dataDir + "ExportToXML_out.vdx", SaveFileFormat.VDX);

/* 2. Exporting from VSD to VSX */
// Call the diagram constructor to load diagram from a VSD file
            
// Save input VSD as VSX
diagram.Save(dataDir + "ExportToXML_out.vsx", SaveFileFormat.VSX);
            
/* 3. Export VSD to VTX */
// Save input VSD as VTX
diagram.Save(dataDir + "ExportToXML_out.vtx", SaveFileFormat.VTX);

{{< /highlight >}}
```

## **XPS'e aktar**
 Bu makalede, bir Microsoft Visio diagram'in XPS kullanılarak nasıl dışa aktarılacağı açıklanmaktadır.[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) API.
 Kullan[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) diagram dosyalarını okumak için 'class' yapıcısı ve diagram'i desteklenen herhangi bir görüntü formatına dışa aktarmak için Save yöntemi.

Bu makaledeki kod parçacıkları aşağıdaki diagram'i girdi olarak alır. Diğer diagram formatlarını da (VSS, VSSX, VSSM, VDX, VST, VSTX, VDX, VTX veya VSX) kullanabilirsiniz.

|**Kaynak belge.**|
|:- |
|![yapılacaklar:resim_alternatif_Metin](how-to-convert-a-visio-diagram_5.png)|


VSD diagram'i XPS'e dışa aktarmak için:

1. Diagram sınıfının bir örneğini oluşturun.
1. Diagram sınıfının Save yöntemini çağırın ve çıkış formatı olarak XPS'i ayarlayın.
### **İhracat Microsoft Visio Çizimi XPS'e**
Kod örnekleri, Microsoft Visio Çiziminin C# kullanılarak XPS'e nasıl aktarılacağını gösterir.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Diagrams();

// Open a VSD file
Diagram diagram = new Diagram(dataDir + "LayOutShapesInCompactTreeStyle.vdx");

// Save diagram to an XPS format
diagram.Save(dataDir + "ExportToXPS_out.xps", SaveFileFormat.XPS);

{{< /highlight >}}
```

## **Diagram'i SVG'e dışa aktarın**
 Bu makalede, bir Microsoft Visio diagram'in SVG'e (Ölçeklenebilir Vektör Grafikleri) kullanılarak nasıl dışa aktarılacağı açıklanmaktadır.[Aspose.Diagram for .NET](http://www.aspose.com/.net/diagram-component.aspx) API.

 Kullan[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) diagram dosyalarını okumak için 'class' yapıcısı ve diagram'i desteklenen herhangi bir görüntü formatına dışa aktarmak için Save yöntemi.

VSD diagram'i SVG'e aktarmak için aşağıdaki adımları gerçekleştirin:

1. Diagram sınıfının bir örneğini oluşturun.
1. Sınıfın Save yöntemini çağırın ve dışa aktarma formatı olarak SVG'i ayarlayın.
### **İhracat Microsoft Visio Çizimi SVG'e**
Kod örnekleri, C# kullanarak bir diagram'in SVG'e nasıl aktarılacağını gösterir.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_LoadSaveConvert();

// Call the diagram constructor to load a VSD diagram
Diagram diagram = new Diagram(dataDir + "ExportToSVG.vsd");

// Save SVG Output file
diagram.Save(dataDir + "Output.svg", SaveFileFormat.SVG);

{{< /highlight >}}
```
## **SWF'e aktar**
 Bu makalede, bir Microsoft Visio diagram'in SWF kullanılarak nasıl dışa aktarılacağı açıklanmaktadır.[Aspose.Diagram for .NET](http://www.aspose.com/.net/diagram-component.aspx) API.

 Kullan[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) diagram dosyalarını okumak için class' yapıcıları ve ardından diagram'i SWF biçimine dışa aktarmak için Diagram sınıfının Save yöntemi. The image below shows the input VSD file that the code renders to SWF. You can use other diagram formats (VSS, VSSX, VSSM, VDW, VDX, VST, VSTX, VSTM, VDX, VTX or VSX) as well.

|**diagram'i girin.**|
|:- |
|![yapılacaklar:resim_alternatif_Metin](how-to-convert-a-visio-diagram_7.png)|

Koddan sonra, çıktının bir görüntüsü var.

VSD diagram'i SWF'e dışa aktarmak için::

- Diagram sınıfının bir örneğini oluşturun.
- Diagram sınıfının Save yöntemini çağırın ve diagram'inizi SWF'e dışa aktarmak için SWF biçimini sağlayın.
### **Katıştırılmış Görüntüleyici Programlama Örneği**
```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Diagrams();
// Load diagram
Diagram diagram = new Diagram(dataDir + "ActvDir.vsd");
// Save diagram
diagram.Save(dataDir + "Output_out.swf", SaveFileFormat.SWF);

{{< /highlight >}}
```
### **Görüntüleyici Programlama Örneği Olmadan**
Bu kod parçacıkları tarafından oluşturulan SWF dosyası, bir SWF görüntüleyici içerir. Aşağıdaki kodu kullanarak SWF görüntüleyiciyi dosyadan hariç tutun.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Diagrams();

// Instantiate Diagram Object and open VSD file
Diagram diagram = new Diagram(dataDir + "ExportToSWFWithoutViewer.vsd");

// Instantiate the Save Options
SWFSaveOptions options = new SWFSaveOptions();

// Set Save format as SWF
options.SaveFormat = SaveFileFormat.SWF;

// Exclude the embedded viewer
options.ViewerIncluded = false;

// Save the resultant SWF file
diagram.Save(dataDir + "ExportToSWFWithoutViewer_out.swf", SaveFileFormat.SWF);

{{< /highlight >}}
```
## **Diagram'i XAML'e dışa aktarın**
Bu makalede, bir Microsoft Visio diagram'in XAML'e (Genişletilebilir Uygulama İşaretleme Dili) kullanılarak nasıl dışa aktarılacağı açıklanmaktadır.[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) API.

 Kullan[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) diagram dosyalarını okumak için 'class' yapıcısı ve diagram'i desteklenen herhangi bir görüntü formatına dışa aktarmak için Save yöntemi.

Bir VSD diagram'i XAML'e aktarmak için:

1. Diagram sınıfının bir örneğini oluşturun.
1. Sınıfın Save yöntemini çağırın ve dışa aktarma formatı olarak XAML'i ayarlayın.
### **İhracat Microsoft Visio Çizimi XAML'e**
Kod örneği, C# kullanarak bir diagram'in XAML'e nasıl aktarılacağını gösterir.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_LoadSaveConvert();
// Load diagram
Diagram diagram = new Diagram(dataDir + "ExportToXAML.vsd");
// Save diagram
diagram.Save(dataDir + "ExportToXAML_out.xaml", SaveFileFormat.XAML);

{{< /highlight >}}
```
## **Dönüştür Visio Seçici Şekillerle Çizim**
Aspose.Diagram API'i kullanan geliştiriciler, bir Visio çizimini desteklenen herhangi bir formata dönüştürmek için bir grup şekil seçebilirler. RenderingSaveOptions sınıfı, şekil grubunu korumak için bir Shapes üyesi sunar. Her kaydetme seçeneği sınıfı, RenderingSaveOptions sınıfının genişletilmiş biçimidir.

Bir Visio çizimini seçici şekillerle dışa aktarmak için:

1. Diagram sınıfının bir örneğini oluşturun.
1. Ayarları burada anlatıldığı gibi belirtmek için herhangi bir SaveOption sınıfının bir örneğini oluşturun:[Visio Kaydetme Seçeneklerini Belirtin](https://docs.aspose.com/diagram/net/save-visio-document/#specifying-visio-save-options)
1. Diagram sınıf nesnesinin Kaydetme yöntemini çağırın ve kaydetme seçeneği sınıf nesnesini parametre olarak iletin.
### **Dönüştür Visio Seçici Şekillerle Çizim Programlama Örneği**
Kod örneği, bir çizimin seçici Visio şekillerle nasıl dışa aktarılacağını gösterir.

```
{{< highlight "csharp" >}}
// the path to the documents directory.
string dataDir = RunExamples.GetDataDir_LoadSaveConvert();

// call the diagram constructor to load diagram from a VSD file
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// create an instance SVG save options class
SVGSaveOptions options = new SVGSaveOptions();
ShapeCollection shapes = options.Shapes;

// get shapes by page index and shape ID, and then add in the shape collection object
shapes.Add(diagram.Pages[0].Shapes.GetShape(1));
shapes.Add(diagram.Pages[0].Shapes.GetShape(2));

// save Visio drawing
diagram.Save(dataDir + "SelectiveShapes_out.svg", options);
{{< /highlight >}}
```