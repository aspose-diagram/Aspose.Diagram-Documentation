---
title: Konnektör Tipi Şekil ile Çalışma
type: docs
weight: 80
url: /tr/java/working-with-connector-type-shape/
---
## **Visio'de Konektör Türü Şeklinin Görünümünü Ayarlayın**
Bu konuda, geliştiricilerin Aspose.Diagram for Java'i kullanarak dinamik bağlayıcı türü şeklinin görünümünü nasıl değiştirebilecekleri açıklanmaktadır.
### **Bağlayıcı Görünümünü Ayarla**
 Tarafından sunulan SetConnectorsType yöntemi[Şekil](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) class, bağlayıcı türü şeklinin görünümünü ayarlamak için kullanılabilir.

Aşağıdaki kod nasıl yapılacağını gösterir:

1. Bir numune yükleyin diagram.
1. belirli bir sayfa alın.
1. belirli bir konektör şekli elde edin.
1. şeklin görünümünü ayarlayın.
1. kaydet diagram
#### **Bağlayıcı Görünümü Programlama Örneği Ayarla**
Aspose.Diagram for Java kullanarak konektör tipi şeklinin görünümünü ayarlamak için Java uygulamanızda aşağıdaki kodu kullanın.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(SetConnectorAppearance.class);  
// call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

//get a particular page
Page page = diagram.getPages().getPage("Page-3");
//get a dynamic connector type shape by id
Shape shape = page.getShapes().getShape(18);
// set dynamic connector appearance
shape.setConnectorsType(ConnectorsTypeValue.STRAIGHT_LINES);

//saving Visio diagram
diagram.save(dataDir + "SetConnectorAppearance_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Bağlayıcı Şeklinin Yeniden Yönlendirme Seçeneğini Belirleyin**
 Tarafından sunulan ConFixedCode özelliği[Düzen](https://reference.aspose.com/diagram/java/com.aspose.diagram/layout) sınıf, yeniden yönlendirme seçeneğini seçmek için kullanılabilir. tarafından sunulan Layout özelliği[Şekil](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/shape) sınıf kullanılacaktır.

|<p>**Yeniden Yönlendirme Seçenekleri Nasıl Seçilir?** </p><p>![yapılacaklar:resim_alternatif_Metin](http://i.imgur.com/1O70sSA.png)</p>|
|:- |
Aşağıdaki kod nasıl yapılacağını gösterir:

1. Bir örnek dosya yükleyin.
1. belirli bir sayfa alın.
1. belirli bir konektör şekli elde edin.
1. yeniden yönlendirme seçeneklerini ayarlayın.
1. diagram'i kaydedin.
### **Yeniden Yönlendirme Seçeneği Programlama Örneği Seçin**
Aspose.Diagram for Java kullanarak bağlayıcı şeklinin yeniden yönlendirme seçeneğini belirlemek için Java uygulamanızda aşağıdaki kodu kullanın.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(RerouteConnectors.class);   
// call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get page by name
Page page = diagram.getPages().getPage("Page-3");

// get a particular connector shape
Shape shape = page.getShapes().getShape(18);
// set reroute option
shape.getLayout().getConFixedCode().setValue(ConFixedCodeValue.NEVER_REROUTE);

// save Visio diagram
diagram.save(dataDir + "RerouteConnectors_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
