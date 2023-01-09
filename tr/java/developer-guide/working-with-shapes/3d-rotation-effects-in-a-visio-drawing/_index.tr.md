---
title: Visio Çiziminde 3B Döndürme Efektleri
type: docs
weight: 90
url: /tr/java/3d-rotation-effects-in-a-visio-drawing/
---
## **Şekil Sayfasında 3B Döndürme Özelliklerini Ayarlama**
Aspose.Diagram for Java API, geliştiricilerin şekil sayfasındaki 3B döndürme değerlerini değiştirmesine olanak tanır. RotationXAngle, RotationYANgle ve RotationZAngle hücre değerleri, ilgili eksenlerin her birinde dönüş derecesini kontrol eder. RotationType'ın enum değeri, döndürme türünü kontrol eder:

1. Şeklin doğrusal perspektif dikkate alınmadan döndürüldüğü paralel döndürme.
1. Şeklin doğrusal perspektifle döndürüldüğü perspektif döndürme.
1. Şeklin eğik projeksiyonla döndürüldüğü eğik döndürme ön ayarları (sol alt, sağ alt, sol üst ve sağ üst).

bu**Metni Düz Tut**hücre değeri, bir şeklin metninin, şeklin 3 boyutlu dönüşünü göz ardı edip etmeyeceğini gösterir. 2 boyutlu döndürme için geçerli değildir. bu**Yerden Mesafe**hücre değeri, 3 boyutlu döndürüldüğünde noktalarda nesnenin yerden kaldırıldığı mesafeyi belirler. bu**Perspektif**hücre değeri, perspektif döndürme için perspektif açısını derece cinsinden (0 ila 359,9) belirler.
### **3B Döndürme Özelliklerini Ayarlama**
Tarafından sunulan ThreeDFormat üyesi[Şekil](https://reference.aspose.com/diagram/java/com.aspose.diagram/Shape)class, 3B döndürme özelliklerini ayarlamak için kullanılabilir.

Aşağıdaki kod nasıl yapılacağını gösterir:

1. Bir kaynak çizimi yükleyin.
1. Sayfa adı ve kimlik parametrelerine göre bir şekil alın.
1. 3B döndürme özelliklerini ayarlayın.
1. Çizimi kaydet
#### **3B Döndürme Programlama Örneği**
Aspose.Diagram for Java API'i kullanarak 3B döndürme özelliklerini ayarlamak için Java uygulamanızda aşağıdaki kodu kullanın.

**Java**

{{< highlight "java" >}}

 // load diagram

Diagram diagram = new Diagram("c:\\temp\\TestTemplate.vsdx");

// get shape by ID and page name

Shape shape = diagram.getPages().getPage("Page-1").getShapes().getShape(0);



// set 3D rotation properties

shape.getThreeDFormat().getRotationXAngle().setValue(2.61);

shape.getThreeDFormat().getRotationYAngle().setValue(2.61);

shape.getThreeDFormat().getRotationZAngle().setValue(3);

shape.getThreeDFormat().getRotationType().setValue(RotationTypeValue.PARALLEL);

shape.getThreeDFormat().getPerspective().setValue(0);

shape.getThreeDFormat().getDistanceFromGround().setValue(0);

shape.getThreeDFormat().getKeepTextFlat().setValue(BOOL.TRUE);

// save drawing

diagram.save("c:\\temp\\TestTemplate.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
