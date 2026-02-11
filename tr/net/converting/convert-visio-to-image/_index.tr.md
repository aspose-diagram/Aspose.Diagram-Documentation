---
title:  Visio'i Görüntü biçimlerine dönüştür
linktitle: Visio'i Görsellere Dönüştür
type: docs
weight: 20
url: /tr/net/convert-visio-to-image/
description: Bu konuda, Aspose.Diagram'in Visio'i çeşitli resim formatlarına nasıl dönüştürebileceğiniz gösterilmektedir. Visio,VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM görüntülerini birkaç satır kodla PNG, JPEG, BMP'ye dönüştürün.
---
## **Diyagramları Görüntü Dosyası Biçimlerine Aktarın**
 Bu makalede, Microsoft Visio diagram'in kullanılarak bir görüntüye nasıl aktarılacağı açıklanmaktadır.[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) API.[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) diagram dosyalarını okumak için sınıf yapıcısı ve diagram'i desteklenen herhangi bir görüntü formatına dışa aktarmak için Save yöntemi.

diagram'i bir görüntüye dışa aktarmak için:

- Diagram sınıfının bir örneğini oluşturun.
- Diagram sınıfının Save yöntemini çağırın ve dışa aktarmak istediğiniz görüntü formatını ayarlayın. Çıktı görüntü dosyası orijinal dosyaya benziyor.
### **Microsoft Visio Çizimi Resim Dosyasına Aktar**

{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_LoadSaveConvert();

// Call the diagram constructor to load a VSD diagram
Diagram diagram = new Diagram(dataDir + "ExportToImage.vsd");

// Save Image file
diagram.Save(dataDir + "ExportToImage_out.png", SaveFileFormat.PNG);

{{< /highlight >}}


Belgenin tamamı yerine belirli bir sayfayı resme kaydetmek de mümkündür:


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_LoadSaveConvert();
// Load diagram
Diagram diagram = new Diagram(dataDir + "ExportPageToImage.vsd");

// Save diagram as PNG
ImageSaveOptions options = new ImageSaveOptions(SaveFileFormat.PNG);

// Save one page only, by page index
options.PageIndex = 0;

// Save resultant Image file
diagram.Save(dataDir + "ExportPageToImage_out.png", options);

{{< /highlight >}}
