---
title: Metin Kutularıyla Çalışmak
type: docs
weight: 200
url: /tr/java/working-with-text-boxes/
---
## **Visio Şeklin Metin Bloğu Bölümünde Metni Biçimlendir**
 Aspose.Diagram API, geliştiricilerin bir şeklin metin bloğundaki metnin metin yönünü, hizalamayı, kenar boşluklarını, arka plan rengini, arka plan rengi şeffaflığını ve varsayılan sekme durma konumunu kontrol etmesine olanak tanır. kullanarak programlı olarak bu özelliklerle etkileşime girebilirler.[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/).
### **Şeklin Metin Bloğundaki metnin yönünü, hizalamasını, kenar boşluklarını, arka plan rengini, şeffaflığı ve varsayılan sekme durma konumunu ayarlayın**
 Visio şekil sayfasının metin bloğu formatı bölümü, formatlama bilgilerini içerir. bu[Şekil](https://reference.aspose.com/diagram/java/com.aspose.diagram/Shape) sınıf teklifleri[Metin bloğu](https://reference.aspose.com/diagram/java/com.aspose.diagram/TextBlock) şeklin metninin görsel görünümünü almak veya ayarlamak için özellik.
### **Metin Programlama Örneği Biçimlendir**
Aşağıdaki kod parçası yönü, hizalamayı, kenar boşluklarını, arka plan rengini, arka plan rengi şeffaflığını ve yönlendirme açısının varsayılan sekme durma konumunu ve şeklin metninin üstteki konumunu ayarlar.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(FormatShapeTextBlockSection.class); 
// load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// get the page by its name
Page page1 = diagram.getPages().getPage("Page-1");
// get shape by its ID
Shape shape = page1.getShapes().getShape(1);
// set orientation angle
DoubleValue margin = new DoubleValue(4, MeasureConst.PT);

// set left, right, top and bottom margins of the shape's text block
shape.getTextBlock().setLeftMargin(margin);
shape.getTextBlock().setRightMargin(margin);
shape.getTextBlock().setTopMargin(margin);
shape.getTextBlock().setBottomMargin(margin);

// set the text direction
shape.getTextBlock().getTextDirection().setValue(TextDirectionValue.VERTICAL);
// set the text alignment
shape.getTextBlock().getVerticalAlign().setValue(VerticalAlignValue.MIDDLE);
// set the text block background color
shape.getTextBlock().getTextBkgnd().getUfe().setF("RGB(95,108,53)");
// set the background color transparency in percent
shape.getTextBlock().getTextBkgndTrans().setValue(50);
// set the distance between default tab stops for the selected shape.
shape.getTextBlock().getDefaultTabStop().setValue(2);

// save Visio
diagram.save(dataDir + "FormatShapeTextBlockSection_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Şekil Metninin Konumunu Döndürün ve Ayarlayın**
Aspose.Diagram API, geliştiricilerin metin konumunu ayarlamasına ve ayrıca Visio Şeklinde metni döndürmesine olanak tanır. Bu görevi gerçekleştirmek için, şekil sayfasındaki metin dönüşümleri bölümü TxtPin, TxtLocPin, TxtWidth ve TxtHeight özelliklerini sağlar. Geliştiriciler, Aspose.Diagram API'i kullanarak programlı olarak bu özelliklerle etkileşim kurabilir.

Metin dönüştürme bölümü, bir şeklin metin bloğu hakkındaki konumsal bilgileri içerir. Bu örnekler, şekil metni konumlarının ve yönlendirme açısının nasıl ayarlanacağını gösterir:

- [Şeklin metin konumunu üstte ayarla](/diagram/tr/java/working-with-text-boxes/).
- [Altta şeklin metin konumunu ayarla](/diagram/tr/java/working-with-text-boxes/).
- [Şeklin metin konumunu solda ayarla](/diagram/tr/java/working-with-text-boxes/).
- [Şeklin metin konumunu sağda ayarla](/diagram/tr/java/working-with-text-boxes/).
### **Şeklin metin konumunu üstte ayarla**
Aşağıdaki kod parçası, yönlendirme açısını ve şeklin metninin üstteki konumunu ayarlar.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(SetShapeTextPositionAtTop.class);   
// load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get shape
long shapeid = 1;
Shape shape = diagram.getPages().getPage("Page-1").getShapes().getShape(shapeid);

	    // set text position at the top,
	    // TxtLocPinY = "TxtHeight*0" and TxtPinY = "Height*1"
	    shape.getTextXForm().getTxtLocPinY().setValue(0);
	    shape.getTextXForm().getTxtPinY().setValue(shape.getXForm().getHeight().getValue());
	
	    // set orientation angle
	    double angleDeg = 0;
	    double angleRad = (Math.PI / 180) * angleDeg;
	    shape.getTextXForm().getTxtAngle().setValue(angleRad);

// save Visio diagram in the local storage
diagram.save(dataDir + "SetShapeTextPositionAtTop_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

### **Altta şeklin metin konumunu ayarla**
Aşağıdaki kod parçası, alt kısımdaki şeklin metninin oryantasyon açısını ve konumunu ayarlar.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(SetShapeTextPositionAtBottom.class);  
// load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get shape
long shapeid = 1;
Shape shape = diagram.getPages().getPage("Page-1").getShapes().getShape(shapeid);

	     // set text position at the bottom,
	     // TxtLocPinY = "TxtHeight*1" and TxtPinY = "Height*0"
	     shape.getTextXForm().getTxtLocPinY().setValue(shape.getTextXForm().getTxtHeight().getValue());
	     shape.getTextXForm().getTxtPinY().setValue(0);
	
	     // set orientation angle
	     double angleDeg = 0;
	     double angleRad = (Math.PI / 180) * angleDeg;
	     shape.getTextXForm().getTxtAngle().setValue(angleRad);     

// save Visio diagram in the local storage
diagram.save(dataDir + "SetShapeTextPositionAtBottom_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

### **Şeklin metin konumunu solda ayarla**
Aşağıdaki kod parçası, yönlendirme açısını ve şeklin metninin soldaki konumunu ayarlar.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(SetShapeTextPositionAtLeft.class);  
// load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get shape
long shapeid = 1;
Shape shape = diagram.getPages().getPage("Page-1").getShapes().getShape(shapeid);

// set text position at the left,
// TxtLocPinX = "TxtWidth*1" and TxtPinX = "Width*0"
shape.getTextXForm().getTxtLocPinX().setValue(shape.getTextXForm().getTxtWidth().getValue());
shape.getTextXForm().getTxtPinX().setValue(0);
// set orientation angle
double angleDeg = 0;
double angleRad = (Math.PI / 180) * angleDeg;
shape.getTextXForm().getTxtAngle().setValue(angleRad);
        
// save Visio diagram in the local storage
diagram.save(dataDir + "SetShapeTextPositionAtLeft_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

### **Şeklin metin konumunu sağda ayarla**
Aşağıdaki kod parçası, sağdaki şeklin metninin oryantasyon açısını ve konumunu ayarlar.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(SetShapeTextPositionAtRight.class);  
// load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// get shape
long shapeid = 1;
Shape shape = diagram.getPages().getPage("Page-1").getShapes().getShape(shapeid);

// set text position at the right,
// TxtLocPinX = "TxtWidth*0" and TxtPinX = "Width*1"
shape.getTextXForm().getTxtLocPinX().setValue(0);
shape.getTextXForm().getTxtPinX().setValue(shape.getXForm().getWidth().getValue());
// set orientation angle
double angleDeg = 0;
double angleRad = (Math.PI / 180) * angleDeg;
shape.getTextXForm().getTxtAngle().setValue(angleRad);
        
// save Visio diagram in the local storage
diagram.save(dataDir + "SetShapeTextPositionAtRight_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

