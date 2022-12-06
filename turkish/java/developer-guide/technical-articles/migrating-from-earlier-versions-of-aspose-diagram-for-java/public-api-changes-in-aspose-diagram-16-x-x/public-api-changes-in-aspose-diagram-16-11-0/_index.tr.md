---
title: Genel API Aspose.Diagram 16.11.0'daki değişiklikler
type: docs
weight: 20
url: /tr/java/public-api-changes-in-aspose-diagram-16-11-0/
---
{{% alert color="primary" %}} 

Bu belge, modül/uygulama geliştiricilerinin ilgisini çekebilecek 6.8.0 sürümünden 16.11.0 sürümüne Aspose.Diagram API değişikliklerini açıklamaktadır. Yalnızca yeni ve güncellenmiş genel yöntemleri değil, aynı zamanda Aspose.Diagram'deki perde arkasındaki davranışlardaki değişikliklerin açıklamasını da içerir.

{{% /alert %}} 
### **Bir ActiveX Denetiminin Özelliklerini Değiştirme**
 Geliştiriciler bir ActiveX denetimi alabilir ve ardından özelliklerini değiştirebilir. ActiveXControl özelliğini ekledik.[Şekil](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) sınıf. Lütfen bu kod örneğini kontrol edin:

**Java**

{{< highlight "csharp" >}}

 // load a Visio diagram

Diagram diagram = new Diagram("C:\\temp\\Drawing1.vsd");

// get a Visio page by name

Page page = diagram.getPages().getPage("Page-1");

// get a shape by ID

Shape shape = page.getShapes().getShape(1);

// get an ActiveX control

CommandButtonActiveXControl cbac = (CommandButtonActiveXControl)shape.getActiveXControl();

// set width of the command button control

cbac.setWidth(4);

// set height of the command button control

cbac.setHeight(4);

// set caption of the command button control

cbac.setCaption("Test Button");

// save diagram

diagram.save("C:\\temp\\Output.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
### **Visio Diagram'e bir Metin Şekli ekleyin**
Geliştiriciler, Aspose.Diagram API'i kullanarak Visio diagram'e bir metin şekli ekleyebilir. Lütfen bu kod örneğini kontrol edin:

**Java**

{{< highlight "java" >}}

 // create a new diagram

Diagram diagram = new Diagram();

// set parameters

double PinX = 1, PinY = 1, Width = 1, Height = 1;

String text = "Test text";

// add text to a Visio page

diagram.getPages().get(0).addText(PinX, PinY, Width, Height, text);

// save diagram 

diagram.save("C:\\temp\\Output.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
