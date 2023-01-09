---
title: Genel API Aspose.Diagram 5.8.0'daki değişiklikler
type: docs
weight: 20
url: /tr/net/public-api-changes-in-aspose-diagram-5-8-0/
---
{{% alert color="primary" %}} 

Bu belge, Aspose.Diagram API sürümünde 5.7.0'dan 5.8.0'a modül/uygulama geliştiricilerin ilgisini çekebilecek değişiklikleri açıklamaktadır. Yalnızca yeni ve güncellenmiş genel yöntemleri değil, aynı zamanda Aspose.Diagram'deki perde arkasındaki davranışlardaki değişikliklerin açıklamasını da içerir.

{{% /alert %}} 
## **HTMLSaveOptions'a SaveToolBar Seçeneği eklendi**
HTMLSaveOptions sınıfına yeni SaveToolBar seçeneği eklendi. Araç çubuğunun kaydedilip kaydedilmeyeceğini belirtir. Varsayılan değer doğrudur. Örnek kodlar:

**C#**

{{< highlight "java" >}}

 // initialize HTMLSaveOptions class object

HTMLSaveOptions opts = new HTMLSaveOptions();

// set save toolbar option

opts.SaveToolBar = false;

{{< /highlight >}}

**VB**

{{< highlight "java" >}}

 ' initialize HTMLSaveOptions class object

Dim opts As New HTMLSaveOptions()

' set save toolbar option

opts.SaveToolBar = False

{{< /highlight >}}
## **VSDX SaveFileFormat'a Kaydetme Seçeneği eklendi**
Daha önce Aspose.Diagram API, VSDX formatını okumayı desteklerken, şimdi VSDX formatında diyagram yazma desteği ekledik. Örnek kodlar:

**C#**

{{< highlight "java" >}}

 // save diagram in the VSDX format

diagram.Save("C:\\temp\\Output.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

**VB**

{{< highlight "java" >}}

 ' save diagram in the VSDX format

diagram.Save("C:\temp\Output.vsdx", SaveFileFormat.VSDX)

{{< /highlight >}}
## **ShapeCollection Sınıfına Grup Yöntemi eklendi**
Geliştiriciler artık Visio diagram'de Aspose.Diagram API'i kullanarak birden fazla şekli gruplayabilir. Örnek kodlar:

**C#**

{{< highlight "java" >}}

 // load a Visio diagram

Diagram diagram = new Diagram(@"c:\temp\test.vdx");

// Initialize an array of shapes

Aspose.Diagram.Shape[]ss = new Aspose.Diagram.Shape[2];

// extract and assign shapes to the array

ss[0]= diagram.Pages[0].Shapes.GetShape(1);

ss[1]= diagram.Pages[0].Shapes.GetShape(2);

// mark array shapes as group

diagram.Pages[0].Shapes.Group(ss);

// save visio diagram

diagram.Save(@"c:\temp\out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

**VB**

{{< highlight "java" >}}

 ' load a Visio diagram

Dim diagram As New Diagram("c:\temp\test.vdx")

' Initialize an array of shapes

Dim ss As Aspose.Diagram.Shape() = New Aspose.Diagram.Shape(1) {}

' extract and assign shapes to the array

ss(0) = diagram.Pages(0).Shapes.GetShape(1)

ss(1) = diagram.Pages(0).Shapes.GetShape(2)

' mark array shapes as group

diagram.Pages(0).Shapes.Group(ss)

' save visio diagram

diagram.Save("c:\temp\out.vsdx", SaveFileFormat.VSDX)

{{< /highlight >}}
