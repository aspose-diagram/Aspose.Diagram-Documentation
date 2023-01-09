---
title: Katmanlarla Çalışmak
type: docs
weight: 160
url: /tr/java/working-with-layers/
---
### **Şekil Nesnelerini Katmanlarla Yapılandırma**
Aspose.Diagram for Java, şekil nesnelerini Microsoft Office Visio diagram'de katmanlarla yapılandırmaya izin verir. Her şekil birden fazla katmana ait olabilir, böylece geliştiriciler son kullanıcı ihtiyaçlarına uygun şekilleri yönetebilir.

 bu[Şekil](https://reference.aspose.com/diagram/java/com.aspose.diagram/Shape) class nesnesi, Visio çiziminde katmanlara / katmanlardan şekil nesneleri eklemeye / kaldırmaya izin veren LayerMember özelliğini sunar. Kullanıcılar bu özellikleri programlı olarak Aspose.Diagram API kullanarak aşağıdaki gibi yönetebilir:

**diagram'in katmanlarına / katmanlarından şekil nesneleri ekleyin, kaldırın ve taşıyın.** 

![yapılacaklar:resim_alternatif_Metin](working-with-layers_1.png)

Aşağıdaki kod parçası, şekil nesneleri özelliklerini eklemeye, kaldırmaya ve taşımaya yardımcı olur.
#### **Programlama Örnekleri**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Layers-ConfigureShapeLayers-ConfigureShapeLayers.java" >}}
### **Visio Sayfa Sayfasına Katman Ekleme**
Aspose.Diagram for Java, geliştiricilerin özel şekil kategorilerini düzenlemek için yeni katmanlar eklemesine ve ardından bu katmanlara programlı olarak şekiller atamasına olanak tanır.

 bu[Katman Koleksiyonu](https://reference.aspose.com/diagram/java/com.aspose.diagram/LayerCollection) class, yeni bir tane eklemeye izin veren add yöntemini sunar.[Katman](https://reference.aspose.com/diagram/java/com.aspose.diagram/layer)Visio çizimindeki sınıf nesnesi. Geliştiriciler, sınıf nesnesini başlatarak Katman özelliklerini ayarlayabilir.

Aşağıdaki kod parçası, Katman nesneleri eklemeye yardımcı olur.
#### **Programlama Örnekleri**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Layers-AddLayer-AddLayer.java" >}}

{{% alert color="primary" %}} 

Aspose.Diagram for Java, geliştiricilere mevcut Visio diagram katmanlarına erişim sağlar.

{{% /alert %}} 
### **Mevcut Tüm Katmanları Alın**
 bu[Sayfa Sayfası](https://reference.aspose.com/diagram/java/com.aspose.diagram/PageSheet) mülkiyeti[Sayfa](https://reference.aspose.com/diagram/java/com.aspose.diagram/Page) class, kullanarak Visio diagram'den kullanılabilir katmanların listesini almaya izin verir.[Katman Koleksiyonu](https://reference.aspose.com/diagram/java/com.aspose.diagram/layercollection) sınıf.

Aşağıdaki kod parçası, Katmanların listesini almanıza yardımcı olur.
#### **Programlama Örnekleri**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Layers-RetrieveAllLayers-RetrieveAllLayers.java" >}}
