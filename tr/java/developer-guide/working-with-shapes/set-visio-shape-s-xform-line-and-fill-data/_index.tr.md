---
title: Visio Shape'in XForm, Çizgi ve Dolgu Verilerini Ayarla
type: docs
weight: 70
url: /tr/java/set-visio-shape-s-xform-line-and-fill-data/
---
## **XForm Verilerini Ayarlama**
 XForm öğesi, Microsoft Visio XML şemasının bir parçasıdır. XForm, örneğin genişlik, yükseklik, dönüş ve şeklin döndürülüp çevrilmediği gibi bir şekil konumu belirtir. bu[XForm](https://reference.aspose.com/diagram/java/com.aspose.diagram/xform) tarafından açığa çıkarılan mülk,[Şekil](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) sınıfı, Aspose.Diagram.XForm nesnesini destekler. XForm özelliği, bir şeklin XForm verilerini almak veya güncellemek için kullanılabilir. Bu makaledeki kod örnekleri, sayfadaki şekilleri taşımak için PinX (X-koordinatı) ve PinY (Y-koordinatı) XForm değerlerini değiştirir.

**Giriş diagram** 

![yapılacaklar:resim_alternatif_Metin](set-visio-shape-s-xform-line-and-fill-data_1.png)

**diagram sonra** **PinX** **ve** **PinY** **değerler değiştirildi** 

![yapılacaklar:resim_alternatif_Metin](set-visio-shape-s-xform-line-and-fill-data_2.png)

XForm verilerini güncelleme işlemi şu şekildedir:

1. Bir diagram yükleyin.# Belirli bir şekil bulun.# Şeklin XForm verilerini güncelleyin.
1. diagram'i kaydedin.
### **Programlama Örneği**
Aşağıdaki kod parçacığı, bir şeklin XForm verilerinin nasıl güncelleneceğini gösterir. Kod, şekil kimliği 1 olan bir şekil adları sürecini arar ve X ve Y koordinatlarını 5 olarak ayarlar.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(SetXFormdata.class); 
// call a Diagram class constructor to load the VSD diagram
Diagram diagram = new Diagram(dataDir + "SetXFormdata.vsd");

//Find a particular shape and update its XForm
for(Shape shape :(Iterable<Shape>) diagram.getPages().get(0).getShapes())
{
    if (shape.getNameU().toLowerCase() == "process" && shape.getID() == 1)
    {
        shape.getXForm().getPinX().setValue(5);
        shape.getXForm().getPinY().setValue(5);
    }
}
// save diagram
diagram.save(dataDir + "SetXFormdata_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Visio Şeklin Çizgi Verisini Ayarla**
Şekiller çeşitli şekillerde biçimlendirilebilir. Bu makale, bir satırın özniteliklerinin nasıl belirtileceğini gösterir.

Microsoft Visio, kullanıcıların satırları çeşitli şekillerde biçimlendirmesine olanak tanır. Aspose.Diagram for Java şunları destekler:

- Ağırlık: bir çizginin kalınlığı.
- Renk: şeklin çizgi rengini ayarlar.
- Çizgi Rengi Şeffaflığı: şeklin çizgi rengi şeffaflığını yüzde olarak ayarlayın.
- Desen: çizginin düz, kesikli veya başka bir desene sahip olup olmadığını tanımlar.
- Yuvarlama: köşelerin yarıçapı.
- Başlangıç ve bitiş okları: Satırda ok olup olmadığı belirtilir.
- Başlangıç ve bitiş ok boyutları: ok boyutlarını ayarlayın.
- Cap: Çizginin yuvarlanması biter.
### **Bir şeklin kenarlığının çizgi rengini, kalınlığını, tire tipini, saydamlığını, yuvarlamasını, ok tipini ve ok boyutunu değiştirin**
 bu[Astar](https://reference.aspose.com/diagram/java/com.aspose.diagram/line) tarafından açığa çıkarılan mülk,[Şekil](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape)sınıfı, Aspose.Diagram.Line nesnesini destekler. Bu özellik, bir şeklin çizgi verilerini almak veya güncellemek için kullanılabilir.
#### **Hat Veri Programlama Örneği**
Aşağıdaki kod parçası, şeklin satır verilerini günceller.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(SetLineData.class);

// load a Visio diagram
Diagram diagram = new Diagram(dataDir + "SetLineData.vsd");
// get the page by its name
Page page1 = diagram.getPages().getPage("Page-1");
// get shape by its ID
Shape shape = page1.getShapes().getShape(1);
// set line dash type by index
shape.getLine().getLinePattern().setValue(4);
// set line weight, defualt in PT
shape.getLine().getLineWeight().setValue(2);
// set color of the shape's line
shape.getLine().getLineColor().getUfe().setF("RGB(95,108,53)");
// set line rounding, default in inch
shape.getLine().getRounding().setValue(0.3125);
// set line caps
shape.getLine().getLineCap().setValue(BOOL.TRUE);
// set line color transparency in percent
shape.getLine().getLineColorTrans().setValue(50);

/* add arrows to the connector or curve shapes */
// select arrow type by index
shape.getLine().getBeginArrow().setValue(4);
shape.getLine().getEndArrow().setValue(4);
// set arrow size 
shape.getLine().getBeginArrowSize().setValue(ArrowSizeValue.LARGE);
shape.getLine().getBeginArrowSize().setValue(ArrowSizeValue.LARGE);

// save the Visio
diagram.save(dataDir + "SetLineData_Out.vsdx", SaveFileFormat.VSDX);
// save diagram
diagram.save(dataDir+ "output.vdx", SaveFileFormat.VDX);

{{< /highlight >}}
```
## **Visio Şeklin Dolgu Verisini Ayarla**
Şekiller çeşitli şekillerde biçimlendirilebilir. Bu konu, bir şeklin dolgusunun nasıl belirtileceğini açıklar.

 Microsoft Office Visio, kullanıcıların dolguları çeşitli şekillerde biçimlendirmesine olanak tanır. bu[Doldurmak](https://reference.aspose.com/diagram/java/com.aspose.diagram/fill) Aspose.Diagram for Java API sınıfı ayarı destekler:

- Arka plan ve ön plan renkleri.
- şeffaflık
- Kalıpları doldurun.
- gölgeler
### **Dolgu Değerlerini Ayarlama**
Shape sınıfı tarafından sunulan Fill özelliği, Aspose.Diagram.Fill nesnesini destekler. Fill özelliği, bir şeklin dolgu verilerini almak veya güncellemek için kullanılabilir.

|<p>**diagram girişi** </p><p>![yapılacaklar:resim_alternatif_Metin](http://i.imgur.com/OrhEecb.png)</p>|<p>**Dolgu rengini değiştirdikten sonra diagram** </p><p>![yapılacaklar:resim_alternatif_Metin](http://i.imgur.com/HO0wmZ8.png)</p>|
|:- |:- |
#### **Veri Programlama Örneği Doldur**
Aşağıdaki kod parçacığı, bir şeklin dolgu verilerini günceller. Kod, şekil kimliği 1 olan dikdörtgen adlı bir şekli arar ve dolgu arka planını ve ön plan renklerini ayarlar.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(SetFillData.class);


//Call the diagram constructor to load diagram from a VDX file
Diagram diagram = new Diagram(dataDir+ "Drawing1.vsd");

//Find a particular shape and update its XForm
for (com.aspose.diagram.Shape shape : (Iterable<Shape>) diagram.getPages().get(0).getShapes())
{
    if (shape.getNameU().toLowerCase() == "rectangle" && shape.getID() == 1)
    {
        shape.getFill().getFillBkgnd().setValue(diagram.getPages().getPage(0).getShapes().getShape(0).getFill().getFillBkgnd().getValue());
        shape.getFill().getFillForegnd().setValue("#ebf8df");
    }
}
// save diagram
diagram.save(dataDir+ "SetFillData_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
### **Visio Şeklinin Miras Alınan Dolgu Verilerini Alma**
Visio şekilleri, ana stili ve ana şekli devralabilir. Geliştiriciler, bir Visio şeklinin devralma dolgu verilerini alabilir veya ayarlayabilir. Shape sınıfı tarafından sunulan InheritFill özelliği, üst stil ve ana şekil tarafından devralınan şekle ilişkin dolgu biçimlendirme değerlerini içerir.
#### **Devralınan Doldurma Verilerini Al Programlama Örneği**
Aşağıdaki kod parçacığı, şeklin devralınan dolgu verilerini alır. Lütfen bu örnek kodu kontrol edin:

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getSharedDataDir(RetrieveInheritedFillData.class) + "Shapes/";

// Call the diagram constructor to load a VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get page by ID
Page page = diagram.getPages().getPage("Page-1");
// Get shape by ID
Shape shape = page.getShapes().getShape(1);
// Get the fill formatting values
System.out.println(shape.getInheritFill().getFillBkgnd().getValue());
System.out.println(shape.getInheritFill().getFillForegnd().getValue());
System.out.println(shape.getInheritFill().getFillPattern().getValue());
System.out.println(shape.getInheritFill().getShapeShdwObliqueAngle().getValue());
System.out.println(shape.getInheritFill().getShapeShdwOffsetX().getValue());
System.out.println(shape.getInheritFill().getShapeShdwOffsetY().getValue());
System.out.println(shape.getInheritFill().getShapeShdwScaleFactor().getValue());
System.out.println(shape.getInheritFill().getShapeShdwType().getValue());
System.out.println(shape.getInheritFill().getShdwBkgnd().getValue());
System.out.println(shape.getInheritFill().getShdwBkgndTrans().getValue());
System.out.println(shape.getInheritFill().getShdwForegnd().getValue());
System.out.println(shape.getInheritFill().getShdwForegndTrans().getValue());
System.out.println(shape.getInheritFill().getShdwPattern().getValue());

{{< /highlight >}}
```
