---
title: Bir Şeklin Pin Değerlerini ve Ayar Boyutunu Hesaplayın
type: docs
weight: 60
url: /tr/net/calculate-pin-values-and-setting-size-of-a-shape/
description: Bu bölümde Aspose.Diagram ile Alt Şeklin PinX ve PinY Değerlerinin nasıl hesaplanacağı açıklanmaktadır.
---
## **Alt Şeklin PinX ve PinY Değerlerini Hesaplayın**
 Şekil, grup şeklinin bir alt düğümüyse, xformu, ana şeklinin göreli bir koordinatıdır, ancak mutlak koordinat değildir.[Sayfa](http://www.aspose.com/api/net/diagram/aspose.diagram/page). Kullanıcının mutlak koordinatı alması gerekiyorsa, bu örnek kod yardımcı olur.

Yerel koordinatlarda belirtilen bir nokta, aşağıdaki dönüşümler aşağıdaki sırayla uygulanarak ana koordinatlara dönüştürülebilir:

1. Cell_Type öğesinin LocPinX özelliğinin değerini x koordinatından çıkarın.
1. Cell_Type'ın LocPinY özelliğinin değerini y koordinatından çıkarın.
1. Cell_Type öğesinin FlipX özelliğinin değeri bire eşitse, noktayı y ekseni etrafında aynalayın.
1. Cell_Type öğesinin FlipY özelliğinin değeri bire eşitse, noktayı x ekseni etrafında aynalayın.
1. Noktayı, Cell_Type öğesinin Angle özelliğinin değerine göre orijin etrafında saat yönünün tersine döndürün.
1. PinX Cell_Type değerini x koordinatına ekleyin.
1. PinY Cell_Type değerini y koordinatına ekleyin.
### **PinX ve PinY Programlama Örneğinin Hesaplanması**
Aspose.Diagram for .NET API kullanarak bir alt şeklin PinX ve PinY değerlerini hesaplamak için .NET uygulamanızda aşağıdaki kodu kullanın.








{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get a group shape by ID and page index is 0
Shape shape = diagram.Pages[0].Shapes.GetShape(795);
// Get a sub-shape of the group shape by id
Shape subShape = shape.Shapes.GetShape(794);

Matrix m = new Matrix();
// Apply the translation vector
m.Translate(-(float)subShape.XForm.LocPinX.Value, -(float)subShape.XForm.LocPinY.Value);
// Set the elements of that matrix to a rotation
m.Rotate((float)subShape.XForm.Angle.Value);
// Apply the translation vector
m.Translate((float)subShape.XForm.PinX.Value, (float)subShape.XForm.PinY.Value);

// Get pinx and piny
double pinx = m.OffsetX;
double piny = m.OffsetY;
// Calculate the sub-shape pinx and piny
double resultx = shape.XForm.PinX.Value - shape.XForm.LocPinX.Value - pinx;
double resulty = shape.XForm.PinY.Value - shape.XForm.LocPinY.Value - piny;

{{< /highlight >}}

## **Bir Şeklin Yüksekliğini ve Genişliğini Ayarlama**
 bu[Şekil](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) Class, SetHeight ve SetWidth yöntemlerini kullanarak şeklin yüksekliğini ve genişliğini belirleyerek şeklin boyutunu kontrol etmenizi sağlar.

 Tarafından sunulan SetHeight ve SetWidth yöntemleri[Şekil](http://www.aspose.com/api/net/diagram/aspose.diagram/shape)sınıf, bir şekli kalıpla, kalıp olmadan veya bir grup şekli biçiminde yeniden boyutlandırmayı destekler. Bu makaledeki kod örnekleri, sayfadaki şekli yeniden boyutlandırmak için Yükseklik ve Genişliği ayarlar.

Yükseklik ve Genişliği ayarlama işlemi şu şekildedir:

1. diagram yükleyin.
1. Belirli bir şekil bulun.
1. Bir şeklin yüksekliğini ayarlayın.
1. Bir şeklin Genişliğini ayarlayın.
1. diagram'i kaydedin.
### **Ayar Yükseklik ve Genişlik Programlama Örneği**
Aşağıdaki kod parçacığı, şeklin yüksekliğini ve genişliğini nasıl ayarlayacağınızı gösterir. Kod, şekil kimliği 1 olan bir şekil adı dikdörtgeni arar ve Yükseklik ve Genişliğini çift olarak ayarlar.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-1");
// Get shape by id
Shape shape = page.Shapes.GetShape(796);
// Alter the size of Shape
shape.SetWidth(2 * shape.XForm.Width.Value);
shape.SetHeight(2 * shape.XForm.Height.Value);
// Save diagram
diagram.Save(dataDir + "ChangeShapeSize_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

