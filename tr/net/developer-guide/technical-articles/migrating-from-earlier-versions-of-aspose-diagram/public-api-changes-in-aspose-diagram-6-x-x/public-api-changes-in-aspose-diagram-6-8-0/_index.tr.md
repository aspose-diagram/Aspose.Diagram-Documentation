---
title: Genel API Aspose.Diagram 6.8.0'daki değişiklikler
type: docs
weight: 10
url: /tr/net/public-api-changes-in-aspose-diagram-6-8-0/
---
{{% alert color="primary" %}} 

Bu belge, Aspose.Diagram API sürümünde 6.6.0'dan 6.8.0'a modül/uygulama geliştiricilerin ilgisini çekebilecek değişiklikleri açıklamaktadır. Yalnızca yeni ve güncellenmiş genel yöntemleri değil, aynı zamanda Aspose.Diagram'deki perde arkasındaki davranışlardaki değişikliklerin açıklamasını da içerir.

{{% /alert %}} 
## **Bir ActiveX Denetimi Ekleme**
Geliştiriciler, Visio diagram'de bir ActiveX denetimi ekleyebilir. AddActiveXControl yöntemini ekledik.[Sayfa](http://www.aspose.com/api/net/diagram/aspose.diagram/page) sınıf. Lütfen bu kod örneğini kontrol edin:

**C#**

{{< highlight "csharp" >}}

 // load an existing Visio diagram

Diagram diagram = new Diagram();

// insert an ActiveX control

diagram.Pages[0].AddActiveXControl(ControlType.Image, 1, 1, 1, 1);

// save diagram

diagram.Save(@"C:\temp\MyOutput.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

Makro 'kodu' oluşturulurken hata oluştu: Parametre dili için geçersiz değer belirtildi
## **Katmanın Renk Onay Kutusunu Ayarlayın**
Geliştiriciler, Aspose.Diagram API'i kullanarak Katmanın Renk Onay Kutusunu ayarlayabilir veya alabilir. Lütfen bu kod örneğini kontrol edin:

**C#**

{{< highlight "csharp" >}}

 // Load source Visio diagram

Diagram diagram = new Diagram(@"c:\temp\Drawing1.vsdx");

// Get Visio page

Aspose.Diagram.Page page = diagram.Pages.GetPage("Page-1");

// Initialize a new Layer class object

Layer layer = new Layer();

// Set Layer name

layer.Name.Value = "Layer1";

// Set Layer Visibility

layer.Visible.Value = BOOL.True;

// set the color checkbox of Layer

layer.IsColorChecked = BOOL.True;

// Add Layer to the particular page sheet

page.PageSheet.Layers.Add(layer);

// Get shape by ID

Shape shape = page.Shapes.GetShape(3);

// Assign shape to this new Layer

shape.LayerMem.LayerMember.Value = layer.IX.ToString();

// Save diagram

diagram.Save(@"c:\temp\AddLayer_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

Makro 'kodu' oluşturulurken hata oluştu: Parametre dili için geçersiz değer belirtildi
## **Shape Sınıfına InheritFill Özelliği ekler**
Geliştiriciler, fill özelliğini devralabilir veya ayarlayabilir. Shape sınıfına InheritFill özelliğini ekledik. Lütfen bu kod örneğini kontrol edin:

**C#**

{{< highlight "csharp" >}}

 // call the diagram constructor to load a VSDX diagram

Diagram diagram = new Diagram(@"c:\temp\Drawing1.vsdx");

// get page by ID

Page page = diagram.Pages.GetPage("Page-1");

// get shape by ID

Shape shape = page.Shapes.GetShape(1);

// get the fill formatting values

Console.WriteLine(shape.InheritFill.FillBkgnd.Value);

Console.WriteLine(shape.InheritFill.FillForegnd.Value);

Console.WriteLine(shape.InheritFill.FillPattern.Value);

{{< /highlight >}}

Makro 'kodu' oluşturulurken hata oluştu: Parametre dili için geçersiz değer belirtildi
