---
title: Visio Shape'in XForm, Çizgi ve Dolgu Verilerini Ayarla
type: docs
weight: 20
url: /tr/net/set-visio-shape-s-xform-line-and-fill-data/
description: Bu bölümde, çizgi verileri dahil şeklin stilinin nasıl ayarlanacağı ve Aspose.Diagram ile verilerin nasıl doldurulacağı açıklanmaktadır.
---
## **XForm Verilerini Ayarlama**
 XForm öğesi, Microsoft Visio XML şemasının bir parçasıdır. XForm, örneğin genişlik, yükseklik, dönüş ve şeklin döndürülüp çevrilmediği gibi bir şekil konumu belirtir. bu[XForm](http://www.aspose.com/api/net/diagram/aspose.diagram/xform) tarafından açığa çıkarılan mülk,[Şekil](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) sınıfı, Aspose.Diagram.XForm nesnesini destekler. XForm özelliği, bir şeklin XForm verilerini almak veya güncellemek için kullanılabilir. Bu makaledeki kod örnekleri, sayfadaki şekilleri taşımak için PinX (X-koordinatı) ve PinY (Y-koordinatı) XForm değerlerini değiştirir.

XForm verilerini güncelleme işlemi şu şekildedir:

1. Bir diagram yükleyin.# Belirli bir şekil bulun.# Şeklin XForm verilerini güncelleyin.
1. diagram'i kaydedin.
### **Programlama Örneği**
Aşağıdaki kod parçacığı, bir şeklin XForm verilerinin nasıl güncelleneceğini gösterir. Kod, şekil kimliği 1 olan bir şekil adları sürecini arar ve X ve Y koordinatlarını 5 olarak ayarlar.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSD diagram
Diagram diagram = new Diagram(dataDir + "SetXFormdata.vsd");

// Find a particular shape and update its XForm
foreach (Aspose.Diagram.Shape shape in diagram.Pages[0].Shapes)
{
    if (shape.NameU.ToLower() == "process" && shape.ID == 1)
    {
        shape.XForm.PinX.Value = 5;
        shape.XForm.PinY.Value = 5;
    }
}
// Save diagram
diagram.Save(dataDir + "SetXFormdata_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Visio Şeklin Çizgi Verisini Ayarla**
Şekiller çeşitli şekillerde biçimlendirilebilir. Bu makale, bir satırın özniteliklerinin nasıl belirtileceğini gösterir.

Microsoft Visio, kullanıcıların satırları çeşitli şekillerde biçimlendirmesine olanak tanır. Aspose.Diagram for .NET şunları destekler:

- Ağırlık: bir çizginin kalınlığı.
- Renk: şeklin çizgi rengini ayarlar.
- Çizgi Rengi Şeffaflığı: şeklin çizgi rengi şeffaflığını yüzde olarak ayarlayın.
- Desen: çizginin düz, kesikli veya başka bir desene sahip olup olmadığını tanımlar.
- Yuvarlama: köşelerin yarıçapı.
- Başlangıç ve bitiş okları: Satırda ok olup olmadığı belirtilir.
- Başlangıç ve bitiş ok boyutları: ok boyutlarını ayarlayın.
- Cap: Çizginin yuvarlanması biter.
### **Bir şeklin kenarlığının çizgi rengini, kalınlığını, tire tipini, saydamlığını, yuvarlamasını, ok tipini ve ok boyutunu değiştirin**
 bu[Astar](http://www.aspose.com/api/net/diagram/aspose.diagram/line) tarafından açığa çıkarılan mülk,[Şekil](http://www.aspose.com/api/net/diagram/aspose.diagram/shape)sınıfı, Aspose.Diagram.Line nesnesini destekler. Bu özellik, bir şeklin çizgi verilerini almak veya güncellemek için kullanılabilir.
#### **Hat Veri Programlama Örneği**
Aşağıdaki kod parçası, şeklin satır verilerini günceller.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load a Visio diagram
Diagram diagram = new Diagram(dataDir + "SetLineData.vsd");
// Get the page by its name
Aspose.Diagram.Page page1 = diagram.Pages.GetPage("Page-1");
// Get shape by its ID
Aspose.Diagram.Shape shape = page1.Shapes.GetShape(1);
// Set line dash type by index
shape.Line.LinePattern.Value = 4;
// Set line weight, defualt in inch
shape.Line.LineWeight.Value = 2;
// Set color of the shape's line
shape.Line.LineColor.Ufe.F = "RGB(95,108,53)";
// Set line rounding, default in inch
shape.Line.Rounding.Value = 0.3125;
// Set line caps
shape.Line.LineCap.Value = BOOL.True;
// Set line color transparency in percent
shape.Line.LineColorTrans.Value = 50;

/* add arrows to the connector or curve shapes */
// Select arrow type by index
shape.Line.BeginArrow.Value = 4;
shape.Line.EndArrow.Value = 4;
// Set arrow size 
shape.Line.BeginArrowSize.Value = ArrowSizeValue.Large;
shape.Line.EndArrowSize.Value = ArrowSizeValue.Large;

// Save the Visio
diagram.Save(dataDir + "SetLineData_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Visio Şeklin Dolgu Verisini Ayarla**
 Şekiller çeşitli şekillerde biçimlendirilebilir. Bu konu, bir şeklin dolgusunun nasıl belirtileceğini açıklar. Microsoft Office Visio, kullanıcıların dolguları çeşitli şekillerde biçimlendirmesine olanak tanır. bu[Doldurmak](http://www.aspose.com/api/net/diagram/aspose.diagram/fill) Aspose.Diagram for .NET API sınıfı ayarı destekler:

- Arka plan ve ön plan renkleri.
- şeffaflık
- Kalıpları doldurun.
- gölgeler
### **Dolgu Değerlerini Ayarlama**
 Tarafından sunulan Fill özelliği[Şekil](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) sınıf, destekler[Aspose.Diagram.Fill](http://www.aspose.com/api/net/diagram/aspose.diagram/fill) nesne. Fill özelliği, bir şeklin dolgu verilerini almak veya güncellemek için kullanılabilir.
#### **Veri Programlama Örneği Doldur**
Aşağıdaki kod parçacığı, bir şeklin dolgu verilerini günceller. Kod, şekil kimliği 1 olan dikdörtgen adlı bir şekli arar ve dolgu arka planını ve ön plan renklerini ayarlar.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSD diagram
Diagram diagram = new Diagram(dataDir + "SetFillData.vsd");

// Find a particular shape and update its XForm
foreach (Aspose.Diagram.Shape shape in diagram.Pages[0].Shapes)
{
    if (shape.NameU.ToLower() == "rectangle" && shape.ID == 1)
    {
        shape.Fill.FillBkgnd.Value = diagram.Pages[1].Shapes[0].Fill.FillBkgnd.Value;
        shape.Fill.FillForegnd.Value = "#ebf8df";
    }
}
// Save diagram
diagram.Save(dataDir + "SetFillData_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
### **Visio Şeklinin Miras Alınan Dolgu Verilerini Alma**
 Visio şekilleri, ana stili ve ana şekli devralabilir. Geliştiriciler, bir Visio şeklinin devralma dolgu verilerini alabilir veya ayarlayabilir. Tarafından sunulan InheritFill özelliği[Şekil](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class, ana stil ve ana şekil tarafından devralınan şeklin dolgu biçimlendirme değerlerini içerir.
#### **Devralınan Doldurma Verilerini Al Programlama Örneği**
Aşağıdaki kod parçacığı, şeklin devralınan dolgu verilerini alır. Lütfen bu örnek kodu kontrol edin:

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Diagrams();

// Call the diagram constructor to load a VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get page by ID
Page page = diagram.Pages.GetPage("Page-1");
// Get shape by ID
Shape shape = page.Shapes.GetShape(1);
// Get the fill formatting values
Console.WriteLine(shape.InheritFill.FillBkgnd.Value);
Console.WriteLine(shape.InheritFill.FillForegnd.Value);
Console.WriteLine(shape.InheritFill.FillPattern.Value);
Console.WriteLine(shape.InheritFill.ShapeShdwObliqueAngle.Value);
Console.WriteLine(shape.InheritFill.ShapeShdwOffsetX.Value);
Console.WriteLine(shape.InheritFill.ShapeShdwOffsetY.Value);
Console.WriteLine(shape.InheritFill.ShapeShdwScaleFactor.Value);
Console.WriteLine(shape.InheritFill.ShapeShdwType.Value);
Console.WriteLine(shape.InheritFill.ShdwBkgnd.Value);
Console.WriteLine(shape.InheritFill.ShdwBkgndTrans.Value);
Console.WriteLine(shape.InheritFill.ShdwForegnd.Value);
Console.WriteLine(shape.InheritFill.ShdwForegndTrans.Value);
Console.WriteLine(shape.InheritFill.ShdwPattern.Value);

{{< /highlight >}}
```
