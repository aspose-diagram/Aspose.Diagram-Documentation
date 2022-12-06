---
title: Genel API Aspose.Diagram 5.8.0'daki değişiklikler
type: docs
weight: 20
url: /tr/java/public-api-changes-in-aspose-diagram-5-8-0/
---
{{% alert color="primary" %}} 

Bu belge, Aspose.Diagram API sürümünde 5.7.0'dan 5.8.0'a modül/uygulama geliştiricilerin ilgisini çekebilecek değişiklikleri açıklamaktadır. Yalnızca yeni ve güncellenmiş genel yöntemleri değil, aynı zamanda Aspose.Diagram'deki perde arkasındaki davranışlardaki değişikliklerin açıklamasını da içerir.

{{% /alert %}} 
### **HTMLSaveOptions'a SaveToolBar Seçeneği eklendi**
HTMLSaveOptions sınıfına yeni SaveToolBar seçeneği eklendi. Araç çubuğunun kaydedilip kaydedilmeyeceğini belirtir. Varsayılan değer doğrudur. Örnek kodlar:

**Java**

{{< highlight "java" >}}

 // initialize HTMLSaveOptions class object

HTMLSaveOptions opts = new HTMLSaveOptions();

// set save toolbar option

opts.setSaveToolBar(false);

{{< /highlight >}}
### **VSDX SaveFileFormat'a Kaydetme Seçeneği eklendi**
Daha önce Aspose.Diagram API, VSDX formatını okumayı desteklerken, şimdi VSDX formatında diyagram yazma desteği ekledik. Örnek kodlar:

**Java**

{{< highlight "java" >}}

 // save diagram in the VSDX format

diagram.save("C:\\temp\\Output.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
### **ShapeCollection Sınıfına Grup Yöntemi eklendi**
Geliştiriciler artık Visio diagram'de Aspose.Diagram API'i kullanarak birden fazla şekli gruplayabilir. Örnek kodlar:

**Java**

{{< highlight "java" >}}

 // load a Visio diagram

Diagram diagram = new Diagram("c:\\temp\\test.vsd");

// Initialize an array of shapes

Shape[]shapes = new Shape[2];

// extract and assign shapes to the array

shapes[0]= diagram.getPages().get(0).getShapes().getShape(1);

shapes[1]= diagram.getPages().get(0).getShapes().getShape(2);

// mark array shapes as group

diagram.getPages().get(0).getShapes().group(shapes);

// save visio diagram

diagram.save("c:\\temp\\out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
