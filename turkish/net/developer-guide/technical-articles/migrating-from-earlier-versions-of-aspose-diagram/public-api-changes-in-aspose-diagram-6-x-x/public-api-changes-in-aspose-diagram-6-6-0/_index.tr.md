---
title: Genel API Aspose.Diagram 6.6.0'daki değişiklikler
type: docs
weight: 20
url: /tr/net/public-api-changes-in-aspose-diagram-6-6-0/
---
{{% alert color="primary" %}} 

Bu belge, Aspose.Diagram API sürümünde 6.3.0'dan 6.6.0'a modül/uygulama geliştiricilerinin ilgisini çekebilecek değişiklikleri açıklamaktadır. Yalnızca yeni ve güncellenmiş genel yöntemleri değil, aynı zamanda Aspose.Diagram'deki perde arkasındaki davranışlardaki değişikliklerin açıklamasını da içerir.

{{% /alert %}} 
## **LoadFileFormat sınıfına VSDM, VSSM ve VSTM formatlarını ekler**
Bu sürüm, makro özellikli Visio formatlarını okuma desteği ekler.
## **SaveFileFormat sınıfına VSDM, VSSM ve VSTM formatlarını ekler**
Bu sürüm, makro etkin Visio biçimlerini yazma desteği ekler.
## **Visio Diagram'de VBA Modül Kodunu değiştirin**
VbaModule, VbaModuleCollection, VbaProject, VbaProjectReference ve VbaProjectReferenceCollection sınıflarını ekledik. Bu sınıflar, VBA projesi üzerinde kontrol sahibi olmanıza yardımcı olur. Geliştiriciler, bu yeni sürüm 6.6.0 veya üzerini kullanarak VBA modül kodunu çıkarabilir ve değiştirebilir. Lütfen bu kod örneğini kontrol edin:

**C#**

{{< highlight "csharp" >}}

 // load an existing Visio diagram

Diagram diagram = new Diagram(@"c:\temp\macro.vsdm", LoadFileFormat.VSDM);

// extract VBA project

Aspose.Diagram.Vba.VbaProject v = diagram.VbaProject;

// Iterate through the modules and modify VBA module code

foreach (VbaModule module in diagram.VbaProject.Modules)

{

    string code = module.Codes;

    if (code.Contains("This is test message."))

        code = code.Replace("This is test message.", "This is Aspose.Diagram message.");

    module.Codes = code;

}

// save the Visio diagram

diagram.Save(@"c:\temp\out.vssm", SaveFileFormat.VSSM);

{{< /highlight >}}

Makro 'kodu' oluşturulurken hata oluştu: Parametre dili için geçersiz değer belirtildi
## **ForeignData sınıfına bir ImageData özelliği ekler**
Bir bayt dizisi olarak ole nesnesinin görüntüsünü temsil eder. Bunun yanı sıra, OLE nesnelerinin işlenmesini de geliştirdik. Geliştiriciler artık Visio diagram'deki bir OLE nesnesini de değiştirebilir. Lütfen şu kod örneğini kontrol edin:

**C#**

{{< highlight "csharp" >}}

 // load a Visio diagram

Diagram diagram = new Diagram(DirPath + "Drawing1.vsdx");

// get page of the Visio diagram by name

Aspose.Diagram.Page page = diagram.Pages.GetPage("Page-1");

// get shape of the Visio diagram by ID

Aspose.Diagram.Shape OLE_Shape = page.Shapes.GetShape(2);

// filter shapes by type Foreign

if (OLE_Shape.Type == Aspose.Diagram.TypeValue.Foreign)

{

    if (OLE_Shape.ForeignData.ForeignType == ForeignType.Object)

    {

        Stream Ole_stream = new MemoryStream(OLE_Shape.ForeignData.ObjectData);

        // get format of the OLE file object

        Aspose.Words.FileFormatInfo info = Aspose.Words.FileFormatUtil.DetectFileFormat(Ole_stream);

        if (info.LoadFormat == Aspose.Words.LoadFormat.Doc || info.LoadFormat == Aspose.Words.LoadFormat.Docx)

        {

            // modify an OLE object

            var doc = new Aspose.Words.Document(new MemoryStream(OLE_Shape.ForeignData.ObjectData));

            doc.Range.Replace("testing", "Aspose", false, true);

            MemoryStream outStream = new MemoryStream();

            doc.Save(outStream, Aspose.Words.SaveFormat.Docx);

            // save back an OLE object

            OLE_Shape.ForeignData.ObjectData = outStream.ToArray();

        }

    }

}

// save Visio diagram

diagram.Save(DirPath + "modified.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

Makro 'kodu' oluşturulurken hata oluştu: Parametre dili için geçersiz değer belirtildi
