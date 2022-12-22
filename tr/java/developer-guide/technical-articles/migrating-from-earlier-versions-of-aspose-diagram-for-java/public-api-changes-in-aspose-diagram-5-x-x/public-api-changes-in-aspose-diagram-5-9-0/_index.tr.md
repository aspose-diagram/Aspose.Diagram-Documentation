---
title: Genel API Aspose.Diagram 5.9.0'daki değişiklikler
type: docs
weight: 10
url: /tr/java/public-api-changes-in-aspose-diagram-5-9-0/
---
{{% alert color="primary" %}} 

Bu belge, modül/uygulama geliştiricilerinin ilgisini çekebilecek 5.8.0 sürümünden 5.9.0 sürümüne Aspose.Diagram API değişikliklerini açıklamaktadır. Yalnızca yeni ve güncellenmiş genel yöntemleri değil, aynı zamanda Aspose.Diagram'deki perde arkasındaki davranışlardaki değişikliklerin açıklamasını da içerir.

{{% /alert %}} 
### **Sonuç HTML'i Akışa Kaydet**
Diagram sınıfına yeni kaydetme yöntemi eklendi. Akış nesnesi ve dosya kaydetme biçimi olmak üzere iki parametre alır.
Örnek kod:

**Java**

{{< highlight "java" >}}

 // Call the diagram constructor to load diagram from a VSD file

Diagram diagram = new Diagram("Basic Flowchart.vsd");

// save resultant HTML directly to a stream

ByteArrayOutputStream dstStream = new ByteArrayOutputStream();

diagram.save(dstStream, SaveFileFormat.HTML);

// In you want to read the result into a Diagram object again, in Java you need to get the

// data bytes and wrap into an input stream.

ByteArrayInputStream srcStream = new ByteArrayInputStream(dstStream.toByteArray());

{{< /highlight >}}
### **Başka Bir Visio'den Temaları ve Sayfa Sayfasını Kopyala**
Diagram sınıfı, CopyTheme yöntemini sunar ve PageSheet sınıfı, bir şekli kopyalama hedefini ve diğer işleme görevlerini gerçekleştirmek için Copy yöntemini sunar.
 Örnek kodlar:[Mevcut Bir Visio'den Şekilleri Kopyala](/diagram/tr/java/working-with-visio-shape-data/#copy-shapes-from-an-existing-visio)
### **VSTX ve VSSX SaveFileFormat'a Kaydetme Seçenekleri eklendi**
Daha önce Aspose.Diagram API, VSDX formatını okuma ve yazmayı desteklerken, şimdi VSTX ve VSSX formatlarında diyagram yazma desteği ekledik. Örnek kodlar:

**Java**

{{< highlight "java" >}}

 // save diagram in the VSTX format

diagram.save("C:\\temp\\Output.vstx", SaveFileFormat.VSTX);

// save diagram in the VSSX format

diagram.save("C:\\temp\\Output.vssx", SaveFileFormat.VSSX);

{{< /highlight >}}
### **VSSX LoadFileFormat'a Okuma Seçeneği eklendi**
Daha önce Aspose.Diagram API, VSDX formatını okuma ve yazmayı desteklerken, şimdi VSSX şablon formatını okuma desteğini de ekledik. Örnek kodlar:

**Java**

{{< highlight "java" >}}

 // read VSSX stencil

Diagram diagram = new Diagram("C:\\temp\\Stencil.vssx", LoadFileFormat.VSSX);

{{< /highlight >}}
