---
title: Bir Şeklin Pin Değerlerini ve Ayar Boyutunu Hesaplayın
type: docs
weight: 40
url: /tr/java/calculate-pin-values-and-setting-size-of-a-shape/
---
## **Alt Şeklin PinX ve PinY Değerlerini Hesaplayın**
 Şekil, grup şeklinin alt öğesiyse, xform'u ana şeklinin göreli koordinatıdır, ancak mutlak koordinat değildir.[Sayfa](https://reference.aspose.com/diagram/java/com.aspose.diagram/page). Kullanıcının mutlak koordinatı alması gerekiyorsa, bu örnek kod yardımcı olur.

Yerel koordinatlarda belirtilen bir nokta, aşağıdaki dönüşümler aşağıdaki sırayla uygulanarak ana koordinatlara dönüştürülebilir:

1. Cell_Type öğesinin LocPinX özelliğinin değerini x koordinatından çıkarın.
1. Cell_Type'ın LocPinY özelliğinin değerini y koordinatından çıkarın.
1. Cell_Type öğesinin FlipX özelliğinin değeri bire eşitse, noktayı y ekseni etrafında aynalayın.
1. Cell_Type öğesinin FlipY özelliğinin değeri bire eşitse, noktayı x ekseni etrafında aynalayın.
1. Noktayı, Cell_Type öğesinin Angle özelliğinin değerine göre orijin etrafında saat yönünün tersine döndürün.
1. PinX Cell_Type değerini x koordinatına ekleyin.
1. PinY Cell_Type değerini y koordinatına ekleyin.
### **PinX ve PinY Programlama Örneğinin Hesaplanması**
Aspose.Diagram for Java API kullanarak bir alt şeklin PinX ve PinY değerlerini hesaplamak için Java uygulamanızda aşağıdaki kodu kullanın.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(CalculateCenterOfSubShapes.class);
        
// load Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get group shape
Shape shape = diagram.getPages().get(0).getShapes().getShape(138);
// get sub-shape of the group shape
Shape subShape = shape.getShapes().getShape(140);


AffineTransform m = new AffineTransform();
// apply the translation vector
m.translate(-(float)subShape.getXForm().getLocPinX().getValue(), -(float)subShape.getXForm().getLocPinY().getValue());		
// set the elements of that matrix to a rotation
m.rotate((float)subShape.getXForm().getAngle().getValue());
// apply the translation vector
m.translate((float)subShape.getXForm().getPinX().getValue(), (float)subShape.getXForm().getPinY().getValue());

// get pinx and piny		
double pinx = m.getTranslateX();
double piny = m.getTranslateY();
		
// calculate the sub-shape pinx and piny
double resultx = shape.getXForm().getPinX().getValue() - shape.getXForm().getLocPinX().getValue() - pinx;
double resulty = shape.getXForm().getPinY().getValue() - shape.getXForm().getLocPinY().getValue() - piny;

{{< /highlight >}}

## **Bir Şeklin Yüksekliğini ve Genişliğini Ayarlama**
 bu[Şekil](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) Class, SetHeight ve SetWidth yöntemlerini kullanarak şeklin yüksekliğini ve genişliğini belirleyerek şeklin boyutunu kontrol etmenizi sağlar.

 Tarafından sunulan SetHeight ve SetWidth yöntemleri[Şekil](https://reference.aspose.com/diagram/java/com.aspose.diagram/Shape)sınıf, bir şekli kalıpla, kalıp olmadan veya bir grup şekli biçiminde yeniden boyutlandırmayı destekler.

Bu makaledeki kod örnekleri, sayfadaki şekli yeniden boyutlandırmak için Yükseklik ve Genişliği ayarlar.

**Giriş diagram** 

![yapılacaklar:resim_alternatif_Metin](http://i.imgur.com/cTiNWa7.png)

**Yükseklik ve Genişlik değiştirildikten sonra diagram**

![yapılacaklar:resim_alternatif_Metin](calculate-pin-values-and-setting-size-of-a-shape_1.png)

Yükseklik ve Genişliği ayarlama işlemi şu şekildedir:

1. diagram yükleyin.
1. Belirli bir şekil bulun.
1. Bir şeklin yüksekliğini ayarlayın.
1. Bir şeklin Genişliğini ayarlayın.
1. diagram'i kaydedin.
### **Ayar Yükseklik ve Genişlik Programlama Örneği**
Aşağıdaki kod parçacığı, şeklin yüksekliğini ve genişliğini nasıl ayarlayacağınızı gösterir. Kod, şekil kimliği 1 olan bir şekil adı dikdörtgeni arar ve Yükseklik ve Genişliğini çift olarak ayarlar.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ChangeShapeSize.class);
        
// call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get page by name
Page page = diagram.getPages().getPage("Page-1");
// get shape by id
Shape shape = page.getShapes().getShape(796);
// alter the size of Shape
shape.setWidth(2 * shape.getXForm().getWidth().getValue());
shape.setHeight(2 * shape.getXForm().getHeight().getValue());
// save diagram
diagram.save(dataDir + "ChangeShapeSize_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

