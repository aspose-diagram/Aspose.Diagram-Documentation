---
title: Katmanlarla Çalışmak
type: docs
weight: 160
url: /tr/python-java/working-with-layers/
---
### **Şekil Nesnelerini Katmanlarla Yapılandırma**
Python için Java üzerinden Aspose.Diagram, şekil nesnelerini Microsoft Office Visio diagram'deki katmanlarla yapılandırmaya izin verir. Her şekil birden fazla katmana ait olabilir, böylece geliştiriciler son kullanıcı ihtiyaçlarına uygun şekilleri yönetebilir.

 bu[Şekil](https://reference.aspose.com/diagram/java/com.aspose.diagram/Shape) class nesnesi, Visio çiziminde katmanlara / katmanlardan şekil nesneleri eklemeye / kaldırmaya izin veren LayerMember özelliğini sunar. Kullanıcılar bu özellikleri programlı olarak Aspose.Diagram API kullanarak aşağıdaki gibi yönetebilir:

**diagram'in katmanlarına / katmanlarından şekil nesneleri ekleyin, kaldırın ve taşıyın.** 

Aşağıdaki kod parçası, şekil nesneleri özelliklerini eklemeye, kaldırmaya ve taşımaya yardımcı olur.
#### **Programlama Örnekleri**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Layers-ConfigureShapeLayers.py" >}}
### **Visio Sayfa Sayfasına Katman Ekleme**
Python üzerinden Java için Aspose.Diagram, geliştiricilerin özel şekil kategorilerini düzenlemek için yeni katmanlar eklemesine ve ardından bu katmanlara programlı olarak şekiller atamasına olanak tanır.

 bu[Katman Koleksiyonu](https://reference.aspose.com/diagram/java/com.aspose.diagram/LayerCollection) class, yeni bir tane eklemeye izin veren add yöntemini sunar.[Katman](https://reference.aspose.com/diagram/java/com.aspose.diagram/layer) sınıf nesnesi[Visio çizimi](DrawingFlowChart.vsdx). Geliştiriciler, sınıf nesnesini başlatarak Katman özelliklerini ayarlayabilir.

Aşağıdaki kod parçası, Katman nesneleri eklemeye yardımcı olur.
#### **Programlama Örnekleri**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Layers-AddLayer.py" >}}

{{% alert color="primary" %}} 

Java aracılığıyla Python için Aspose.Diagram, geliştiricilerin mevcut Visio diagram katmanlarına erişmesini sağlar.

{{% /alert %}} 
### **Mevcut Tüm Katmanları Alın**
 bu[Sayfa Sayfası](https://reference.aspose.com/diagram/java/com.aspose.diagram/PageSheet) mülkiyeti[Sayfa](https://reference.aspose.com/diagram/java/com.aspose.diagram/Page) class, kullanılabilir katmanların listesinin alınmasına izin verir.[Visio çizimi](DrawingFlowChart.vsdx) kullanarak[Katman Koleksiyonu](https://reference.aspose.com/diagram/java/com.aspose.diagram/layercollection) sınıf.

Aşağıdaki kod parçası, Katmanların listesini almanıza yardımcı olur.
#### **Programlama Örnekleri**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Layers-RetrieveAllLayers.py" >}}
