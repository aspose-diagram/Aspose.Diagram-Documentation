---
title: Metin Kutularıyla Çalışmak
type: docs
weight: 210
url: /tr/net/working-with-text-boxes/
description: Bu bölümde bir metin şeklinin Aspose.Diagram ile nasıl biçimlendirileceği açıklanmaktadır.
---
## **Visio Şeklin Metin Bloğu Bölümünde Metni Biçimlendir**
 Aspose.Diagram API, geliştiricilerin bir şeklin metin bloğundaki metnin metin yönünü, hizalamayı, kenar boşluklarını, arka plan rengini, arka plan rengi şeffaflığını ve varsayılan sekme durma konumunu kontrol etmesine olanak tanır. kullanarak programlı olarak bu özelliklerle etkileşime girebilirler.[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/).
### **Şeklin Metin Bloğundaki metnin yönünü, hizalamasını, kenar boşluklarını, arka plan rengini, şeffaflığı ve varsayılan sekme durma konumunu ayarlayın**
 Visio şekil sayfasının metin bloğu formatı bölümü, biçimlendirme bilgilerini içerir. bu[Şekil](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) sınıf teklifleri[Metin bloğu](http://www.aspose.com/api/net/diagram/aspose.diagram/textblock) şeklin metninin görsel görünümünü almak veya ayarlamak için özellik.
### **Metin Programlama Örneği Biçimlendir**
Aşağıdaki kod parçası yönü, hizalamayı, kenar boşluklarını, arka plan rengini, arka plan rengi şeffaflığını ve yönlendirme açısının varsayılan sekme durma konumunu ve şeklin metninin üstteki konumunu ayarlar.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_ShapeTextBoxData();
            
// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get the page by its name
Aspose.Diagram.Page page1 = diagram.Pages.GetPage("Page-1");
// Get shape by its ID
Aspose.Diagram.Shape shape = page1.Shapes.GetShape(1);
// Set orientation angle
DoubleValue margin = new DoubleValue(4, MeasureConst.PT);

// Set left, right, top and bottom margins of the shape's text block
shape.TextBlock.LeftMargin = margin;
shape.TextBlock.RightMargin = margin;
shape.TextBlock.TopMargin = margin;
shape.TextBlock.BottomMargin = margin;
// Set the text direction
shape.TextBlock.TextDirection.Value = TextDirectionValue.Vertical;
// Set the text alignment
shape.TextBlock.VerticalAlign.Value = VerticalAlignValue.Middle;
// Set the text block background color
shape.TextBlock.TextBkgnd.Ufe.F = "RGB(95,108,53)";
// Set the background color transparency in percent
shape.TextBlock.TextBkgndTrans.Value = 50;
// Set the distance between default tab stops for the selected shape.
shape.TextBlock.DefaultTabStop.Value = 2;

// Save Visio
diagram.Save(dataDir + "FormatShapeTextBlockSection_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Visio Şekil Metninin Konumunu Döndürün ve Ayarlayın**
 Aspose.Diagram API, geliştiricilerin metin konumunu ayarlamasına ve ayrıca Visio Şeklinde metni döndürmesine olanak tanır. Bu görevi gerçekleştirmek için, şekil sayfasındaki metin dönüşümleri bölümü TxtPin, TxtLocPin, TxtWidth ve TxtHeight özelliklerini sağlar. Geliştiriciler, kullanarak bu özelliklerle programlı olarak etkileşim kurabilir.[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/).
### **Şekil Metninin Konumunu Döndürün ve Ayarlayın**
Metin dönüştürme bölümü, bir şeklin metin bloğu hakkındaki konumsal bilgileri içerir. Aşağıdaki örnekler, şekil metni konumlarının ve yönlendirme açısının nasıl ayarlanacağını gösterir.
#### **Şeklin metin konumunu üstte ayarla**
Aşağıdaki kod parçası, yönlendirme açısını ve şeklin metninin üstteki konumunu ayarlar.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_ShapeTextBoxData();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get shape
long shapeid = 1;
Shape shape = diagram.Pages.GetPage("Page-1").Shapes.GetShape(shapeid);

// Set text position at the top,
// TxtLocPinY = "TxtHeight*0" and TxtPinY = "Height*1"
shape.TextXForm.TxtLocPinY.Value = 0;
shape.TextXForm.TxtPinY.Value = shape.XForm.Height.Value;

// Set orientation angle
double angleDeg = 0;
double angleRad = (Math.PI / 180) * angleDeg;
shape.TextXForm.TxtAngle.Value = angleRad;

// Save Visio diagram in the local storage
diagram.Save(dataDir + "SetShapeTextPositionAtTop_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
#### **Altta şeklin metin konumunu ayarla**
Aşağıdaki kod parçası, alt kısımdaki şeklin metninin oryantasyon açısını ve konumunu ayarlar.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_ShapeTextBoxData();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get shape
long shapeid = 1;
Shape shape = diagram.Pages.GetPage("Page-1").Shapes.GetShape(shapeid);

// Set text position at the bottom,
// TxtLocPinY = "TxtHeight*1" and TxtPinY = "Height*0"
shape.TextXForm.TxtLocPinY.Value = shape.TextXForm.TxtHeight.Value;
shape.TextXForm.TxtPinY.Value = 0;

// Set orientation angle
double angleDeg = 0;
double angleRad = (Math.PI / 180) * angleDeg;
shape.TextXForm.TxtAngle.Value = angleRad;

// Save Visio diagram in the local storage
diagram.Save(dataDir + "SetShapeTextPositionAtBottom_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
#### **Şeklin metin konumunu solda ayarla**
Aşağıdaki kod parçası, yönlendirme açısını ve şeklin metninin soldaki konumunu ayarlar.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_ShapeTextBoxData();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get shape
long shapeid = 1;
Shape shape = diagram.Pages.GetPage("Page-1").Shapes.GetShape(shapeid);

// Set text position at the left,
// TxtLocPinX = "TxtWidth*1" and TxtPinX = "Width*0"
shape.TextXForm.TxtLocPinX.Value = shape.TextXForm.TxtWidth.Value;
shape.TextXForm.TxtPinX.Value = 0;
// Set orientation angle
double angleDeg = 0;
double angleRad = (Math.PI / 180) * angleDeg;
shape.TextXForm.TxtAngle.Value = angleRad;

// Save Visio diagram in the local storage
diagram.Save(dataDir + "SetShapeTextPositionAtLeft_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
#### **Şeklin metin konumunu sağda ayarla**
Aşağıdaki kod parçası, sağdaki şeklin metninin oryantasyon açısını ve konumunu ayarlar.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_ShapeTextBoxData();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get shape
long shapeid = 1;
Shape shape = diagram.Pages.GetPage("Page-1").Shapes.GetShape(shapeid);

// Set text position at the right,
// TxtLocPinX = "TxtWidth*0" and TxtPinX = "Width*1"
shape.TextXForm.TxtLocPinX.Value = 0;
shape.TextXForm.TxtPinX.Value = shape.XForm.Width.Value;
// Set orientation angle
double angleDeg = 0;
double angleRad = (Math.PI / 180) * angleDeg;
shape.TextXForm.TxtAngle.Value = angleRad;

// Save Visio diagram in the local storage
diagram.Save(dataDir + "SetShapeTextPositionAtRight_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
