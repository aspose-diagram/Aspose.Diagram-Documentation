---
title: Genel API Aspose.Diagram 16.11.0'daki değişiklikler
type: docs
weight: 20
url: /tr/net/public-api-changes-in-aspose-diagram-16-11-0/
---
{{% alert color="primary" %}} 

Bu belge, modül/uygulama geliştiricilerinin ilgisini çekebilecek 6.8.0 sürümünden 16.11.0 sürümüne Aspose.Diagram API değişikliklerini açıklamaktadır. Yalnızca yeni ve güncellenmiş genel yöntemleri değil, aynı zamanda Aspose.Diagram'deki perde arkasındaki davranışlardaki değişikliklerin açıklamasını da içerir.

{{% /alert %}} 
## **Bir ActiveX Denetiminin Özelliklerini Değiştirme**
 Geliştiriciler bir ActiveX denetimi alabilir ve ardından özelliklerini değiştirebilir. ActiveXControl özelliğini ekledik.[Şekil](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) sınıf. Lütfen bu kod örneğini kontrol edin:

**C#**

{{< highlight "csharp" >}}

 // load a Visio diagram

Diagram diagram = new Diagram(@"C:\temp\Drawing1.vsd");

// get a Visio page by name

Page page = diagram.Pages.GetPage("Page-1");

// get a shape by ID

Shape shape = page.Shapes.GetShape(1);

// get an ActiveX control

CommandButtonActiveXControl cbac = (CommandButtonActiveXControl)shape.ActiveXControl;

// set width of the command button control

cbac.Width = 4;

// set height of the command button control

cbac.Height = 4;

// set caption of the command button control

cbac.Caption = "Test Button";

// save diagram

diagram.Save(@"C:\temp\Output.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

Makro 'kodu' oluşturulurken hata oluştu: Parametre dili için geçersiz değer belirtildi
## **Visio Diagram'e bir Metin Şekli ekleyin**
Geliştiriciler, Aspose.Diagram API'i kullanarak Visio diagram'e bir metin şekli ekleyebilir. Lütfen bu kod örneğini kontrol edin:

**C#**

{{< highlight "csharp" >}}

 // create a new diagram

Diagram diagram = new Diagram();

// set parameters

double PinX = 1, PinY = 1, Width = 1, Height = 1;

string text = "Test text";

// add text to a Visio page

diagram.Pages[0].AddText(PinX, PinY, Width, Height, text);

// save diagram 

diagram.Save(@"C:\temp\Output.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

Makro 'kodu' oluşturulurken hata oluştu: Parametre dili için geçersiz değer belirtildi
