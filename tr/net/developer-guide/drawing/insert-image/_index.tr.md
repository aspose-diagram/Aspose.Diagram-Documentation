---
title: Resim ekle
type: docs
weight: 70
url: /tr/net/drawing/insert-image
description: Bu bölüm, visio numaralı sayfaya Aspose.Diagram ile nasıl resim ekleneceğini açıklar. Resim eklemek ve pdf, svg, html, resim, xps ve diğer formatlarda kaydetmek için C#'i kullanarak destekleyin.
---
 bu[Sayfa](http://www.aspose.com/api/net/diagram/aspose.diagram/page)nesne, ön plan sayfasının veya arka plan sayfasının çizim alanını temsil eder. Tarafından sunulan Pages özelliği[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) class, Aspose.Diagram.Page nesnelerinin koleksiyonunu destekler.

## **Visio'e Resim Ekle**
Aspose.Diagram for .NET API, geliştiricilerin bir sayfaya resim şekli eklemesine olanak tanır. Aşağıdaki kod örneği, bir Visio çizimine nasıl resim ekleneceğini gösterir.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
Page page = diagram.Pages[0];       
double pinX = 3, pinY = 3, width = 4, hieght = 4;
using (FileStream fs = new FileStream("image.png", FileMode.Open))
{
    page.AddShape(pinX, pinY, width, hieght, fs);
}
// Save diagram
diagram.Save(dataDir + "AddImageToPage_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}


## **SVG'e Resim Ekle**
Aspose.Diagram for .NET API, geliştiricilerin bir sayfaya resim şekli eklemesine olanak tanır. Aşağıdaki kod örneği, bir Visio çizimine nasıl resim ekleneceğini ve SVG formatında nasıl kaydedileceğini gösterir.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
Page page = diagram.Pages[0];       
double pinX = 3, pinY = 3, width = 4, hieght = 4;
using (FileStream fs = new FileStream("image.png", FileMode.Open))
{
    page.AddShape(pinX, pinY, width, hieght, fs);
}
// Save diagram
diagram.Save(dataDir + "AddImageToPage_out.svg", SaveFileFormat.SVG);

{{< /highlight >}}


## **PNG'e Resim Ekle**
Aspose.Diagram for .NET API, geliştiricilerin bir sayfaya resim şekli eklemesine olanak tanır. Aşağıdaki kod örneği, bir Visio çizimine nasıl resim ekleneceğini ve PNG formatında nasıl kaydedileceğini gösterir.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
Page page = diagram.Pages[0];       
double pinX = 3, pinY = 3, width = 4, hieght = 4;
using (FileStream fs = new FileStream("image.png", FileMode.Open))
{
    page.AddShape(pinX, pinY, width, hieght, fs);
}
// Save diagram
diagram.Save(dataDir + "AddImageToPage_out.png", SaveFileFormat.PNG);

{{< /highlight >}}


## **PDF'e Resim Ekle**
Aspose.Diagram for .NET API, geliştiricilerin bir sayfaya resim şekli eklemesine olanak tanır. Aşağıdaki kod örneği, bir Visio çizimine nasıl resim ekleneceğini ve PDF formatında nasıl kaydedileceğini gösterir.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
Page page = diagram.Pages[0];       
double pinX = 3, pinY = 3, width = 4, hieght = 4;
using (FileStream fs = new FileStream("image.png", FileMode.Open))
{
    page.AddShape(pinX, pinY, width, hieght, fs);
}
// Save diagram
diagram.Save(dataDir + "AddImageToPage_out.pdf", SaveFileFormat.PDF);

{{< /highlight >}}


## **HTML'e Resim Ekle**
Aspose.Diagram for .NET API, geliştiricilerin bir sayfaya resim şekli eklemesine olanak tanır. Aşağıdaki kod örneği, bir Visio çizimine nasıl resim ekleneceğini ve HTML formatında nasıl kaydedileceğini gösterir.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
Page page = diagram.Pages[0];       
double pinX = 3, pinY = 3, width = 4, hieght = 4;
using (FileStream fs = new FileStream("image.png", FileMode.Open))
{
    page.AddShape(pinX, pinY, width, hieght, fs);
}
// Save diagram
diagram.Save(dataDir + "AddImageToPage_out.html", new HTMLSaveOptions());

{{< /highlight >}}

