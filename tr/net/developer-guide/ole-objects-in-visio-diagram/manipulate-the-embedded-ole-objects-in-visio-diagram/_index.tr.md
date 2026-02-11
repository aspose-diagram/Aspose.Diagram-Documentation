---
title: Visio Diagram'de Katıştırılmış OLE Nesnelerini Yönetin
type: docs
weight: 10
url: /tr/net/manipulate-the-embedded-ole-objects-in-visio-diagram/
description: Bu sayfa, ole nesnesinin Aspose.Diagram kitaplığıyla nasıl değiştirileceğini açıklar.
---
{{% alert color="primary" %}}

Microsoft Office Visio, Visio diagram içindeki OLE nesnelerinin değiştirilmesini destekler. Bir visio dosyası Visio çiziminin dışında bulunuyorsa ve geliştiricilerin bu dosyaları çizimin içine otomatik olarak eklemek için .NET uygulamalarına bir özellik eklemeleri gerekiyorsa, bunu kullanarak başarabilirler.[Aspose.Diagram for .NET API](https://products.aspose.com/diagram/net/).

{{% /alert %}}
## **Gömülü OLE Nesneleri Programlama Örneğinin İşlenmesi**
[Nesne Verileri](http://www.aspose.com/api/net/diagram/aspose.diagram/foreigndata/properties/objectdata) mülkiyeti[Yabancı Veri](http://www.aspose.com/api/net/diagram/aspose.diagram/foreigndata)sınıfı, geliştiricilerin Visio diagram'deki mevcut OLE nesnelerini işlemesine olanak tanır. Bu yardım konusu, geliştiricilerin Word belgesinin bir OLE nesnesini nasıl alıp düzenleyebileceklerini gösterir.[Aspose.Words for .NET API](https://products.aspose.com/words/net)ve ardından Visio diagram'de bir OLE nesnesi olarak geri kaydedin.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_OLEObjects();

// Load a Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page of the Visio diagram by name
Aspose.Diagram.Page page = diagram.Pages.GetPage("Page-1");
// Get shape of the Visio diagram by ID
Aspose.Diagram.Shape OLE_Shape = page.Shapes.GetShape(2);

// Filter shapes by type Foreign
if (OLE_Shape.Type == Aspose.Diagram.TypeValue.Foreign)
{
    if (OLE_Shape.ForeignData.ForeignType == ForeignType.Object)
    {
        Stream Ole_stream = new MemoryStream(OLE_Shape.ForeignData.ObjectData);
        // Get format of the OLE file object
        Aspose.Words.FileFormatInfo info = Aspose.Words.FileFormatUtil.DetectFileFormat(Ole_stream);
        if (info.LoadFormat == Aspose.Words.LoadFormat.Doc || info.LoadFormat == Aspose.Words.LoadFormat.Docx)
        {
            // Modify an OLE object
            var doc = new Aspose.Words.Document(new MemoryStream(OLE_Shape.ForeignData.ObjectData));
            doc.Range.Replace("testing", "Aspose", false, true);
            MemoryStream outStream = new MemoryStream();
            doc.Save(outStream, Aspose.Words.SaveFormat.Docx);
            // Save back an OLE object
            OLE_Shape.ForeignData.ObjectData = outStream.ToArray();
        }
    }
}
// Save Visio diagram
diagram.Save(dataDir + "ManipulateObjects_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
