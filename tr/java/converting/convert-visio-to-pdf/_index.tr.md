---
title:  Visio'i PDF biçimine dönüştür
linktitle: Visio'i PDF'e dönüştür
type: docs
weight: 10
url: /tr/java/convert-visio-to-pdf/
description: Bu konu, Aspose.Diagram'in Visio'i PDF biçimlerine dönüştürmeye nasıl izin verdiğini gösterir. VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM'i birkaç satır kodla PDF'e dönüştürün.
---
## **PDF'e aktarılıyor**
{{% alert color="primary" %}}

Aspose.Diagram for Java, API ve Sürüm Numarası ile ilgili bilgileri doğrudan çıktı belgelerine yazar. Örneğin, PDF'e bir Çizim oluşturulduğunda, Aspose.Diagram for Java doldurulur**Başvuru**'Aspose.Diagram' değerine sahip alan ve**PDF Yapımcı**değeri olan alan, örneğin 'Aspose.Diagram 17.9'.

Lütfen Aspose.Diagram for Java API'e bu bilgileri çıktı Belgelerinden değiştirme veya kaldırma talimatı veremeyeceğinizi unutmayın.

{{% /alert %}}

 Bu makalede, bir Microsoft Visio diagram'in PDF kullanılarak nasıl dışa aktarılacağı açıklanmaktadır.[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) API.

 Kullan[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/Diagram) diagram dosyalarını okumak için 'class' yapıcısı ve diagram'i desteklenen herhangi bir görüntü formatına dışa aktarmak için Save yöntemi.

The image below shows the VSD diagram that the code snippets below export PDF. You can use other diagram formats (VSS, VSSX, VSSM, VDX, VST, VSTX, VSTM, VDX, VTX or VSX) as well.

**Kaynak dosya.**

![yapılacaklar:resim_alternatif_Metin](how-to-convert-a-visio-diagram_1.png)

VSD diagram'i PDF'e dışa aktarmak için:

1. Diagram sınıfının bir örneğini oluşturun.
1. Diagram sınıfı Save yöntemini çağırın ve çıktı formatını PDF olarak ayarlayın.

Aşağıda PDF çıktı dosyasının bir görüntüsü bulunmaktadır.

**Çıktı PDF dosyası.**

![yapılacaklar:resim_alternatif_Metin](how-to-convert-a-visio-diagram_2.png)
### **PDF Programlama Örneğine Aktarma**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ExportToPDF.class);

// Call the diagram constructor to load diagram from a VSD file
Diagram diagram = new Diagram(dataDir + "ExportToPDF.vsd");

// Save as PDF file format
diagram.save(dataDir + "ExportToPDF_Out.pdf", SaveFileFormat.PDF);

{{< /highlight >}}
```
### **Birden Çok Sayfayı Böl**
Aspose.Diagram for Java, Microsoft Visio Diagram'i PDF'e dönüştürürken birden fazla sayfanın bölünmesine izin verir. Aşağıdaki kod parçacığı işlevselliği gösterir.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(UsePDFSaveOptions.class);      
// Call the diagram constructor to load diagram from a VSDX file
Diagram diagram = new Diagram(dataDir + "Network Diagram_start.vsdx");
// Options when saving a diagram into the PDF format
PdfSaveOptions options = new PdfSaveOptions();
// set SplitMultiPages option
options.setSplitMultiPages(true);
// save in PDF format
diagram.save(dataDir + "SplitMultiPages.pdf", options);

{{< /highlight >}}
```
### **Sayfa Kaydetme Geri Aramasını Kullan**
Birden fazla sayfanız olması durumunda, Aspose.Diagram for Java, Microsoft Visio Diagram'i PDF'e dönüştürürken sayfa kaydetme geri aramasının kullanılmasına izin verir. Aşağıdaki kod parçacığı, işlevselliği gösterir.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(DocumentConversionProgress.class);
// load a Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// create an instance PDF save options class
PdfSaveOptions options = new PdfSaveOptions();
          
//set page saving call back
options.setPageSavingCallback( new TestDiagramPageSavingCallback());

// save Visio drawing
diagram.save(dataDir + "Callback_out.pdf", options);

{{< /highlight >}}
```

#### **TestDiagramPageSavingCallback Sınıfı**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
import com.aspose.diagram.IPageSavingCallback;
import com.aspose.diagram.PageEndSavingArgs;
import com.aspose.diagram.PageStartSavingArgs;

public class TestDiagramPageSavingCallback implements IPageSavingCallback
{
    public void pageStartSaving(PageStartSavingArgs args)
    {
    	System.out.println("Start saving page index " + args.getPageIndex() + " of pages " + args.getPageCount());
    }

    public void pageEndSaving(PageEndSavingArgs args)
    {
    	System.out.println("End saving page index " + args.getPageIndex() + " of pages " + args.getPageCount());

        //don't output pages after page index 8.
        if (args.getPageIndex() >= 8)
        {
            args.setHasMorePages(false);
        }
    }
}


{{< /highlight >}}
```
