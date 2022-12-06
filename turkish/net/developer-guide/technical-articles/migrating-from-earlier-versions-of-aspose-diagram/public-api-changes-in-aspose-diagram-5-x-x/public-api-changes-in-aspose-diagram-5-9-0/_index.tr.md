---
title: Genel API Aspose.Diagram 5.9.0'daki değişiklikler
type: docs
weight: 10
url: /tr/net/public-api-changes-in-aspose-diagram-5-9-0/
---
{{% alert color="primary" %}} 

Bu belge, modül/uygulama geliştiricilerinin ilgisini çekebilecek 5.8.0 sürümünden 5.9.0 sürümüne Aspose.Diagram API değişikliklerini açıklamaktadır. Yalnızca yeni ve güncellenmiş genel yöntemleri değil, aynı zamanda Aspose.Diagram'deki perde arkasındaki davranışlardaki değişikliklerin açıklamasını da içerir.

{{% /alert %}} 
## **Sonuç HTML'sini Akışa Kaydet**
Diagram sınıfına yeni Save yöntemi eklendi. Akış nesnesi ve dosya kaydetme biçimi olmak üzere iki parametre alır.
Örnek kod:

**C#**

{{< highlight "java" >}}

 // load an existing visio diagram

Diagram diagram = new Diagram("Basic Flowchart.vsd");

// save resultant HTML directly to a stream

MemoryStream stream = new MemoryStream();

diagram.Save(stream, SaveFileFormat.HTML);

{{< /highlight >}}

**VB**

{{< highlight "java" >}}

 ' load an existing visio diagram

Dim diagram As Diagram = New Diagram("Basic Flowchart.vsd")

' save resultant HTML directly to a stream

MemoryStream stream = new MemoryStream()

diagram.Save(stream, SaveFileFormat.HTML)

{{< /highlight >}}
## **Başka Bir Visio'den Temaları ve Sayfa Sayfasını Kopyala**
Diagram sınıfı, CopyTheme yöntemini sunar ve PageSheet sınıfı, bir şekli kopyalama hedefini ve diğer işleme görevlerini gerçekleştirmek için Copy yöntemini sunar.
 Örnek kodlar:[Mevcut Bir Visio'den Şekilleri Kopyala](/diagram/tr/net/add-retrieve-copy-and-read-visio-shape-data/)
## **VSTX ve VSSX SaveFileFormat'a Kaydetme Seçenekleri eklendi**
Daha önce Aspose.Diagram API, VSDX formatını okuma ve yazmayı desteklerken, şimdi VSTX ve VSSX formatlarında diyagram yazma desteği ekledik. Örnek kodlar:

**C#**

{{< highlight "java" >}}

 // save diagram in the VSTX format

diagram.Save("C:\\temp\\Output.vstx", SaveFileFormat.VSTX);

// save diagram in the VSSX format

diagram.Save("C:\\temp\\Output.vssx", SaveFileFormat.VSSX);

{{< /highlight >}}

**VB**

{{< highlight "java" >}}

 ' save diagram in the VSTX format

diagram.Save("C:\\temp\\Output.vstx", SaveFileFormat.VSTX)

' save diagram in the VSSX format

diagram.Save("C:\\temp\\Output.vssx", SaveFileFormat.VSSX)

{{< /highlight >}}
## **VSSX LoadFileFormat'a Okuma Seçeneği eklendi**
Daha önce Aspose.Diagram API, VSDX formatını okuma ve yazmayı desteklerken, şimdi VSSX şablon formatını okuma desteğini de ekledik. Örnek kodlar:

**C#**

{{< highlight "java" >}}

 // read VSSX stencil

Diagram diagram = new Diagram(@"C:\temp\Stencil.vssx", LoadFileFormat.VSSX);

{{< /highlight >}}

**VB**

{{< highlight "java" >}}

 ' read VSSX stencil

Diagram diagram = new Diagram(@"C:\temp\Stencil.vssx", LoadFileFormat.VSSX)

{{< /highlight >}}
