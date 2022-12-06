---
title: Shapes Gluing ile Çalışmak
type: docs
weight: 10
url: /tr/java/working-with-shapes-gluing/
---
## **Bağlayıcıları Belirli Bir Şekilde Yapıştırın**
[Ekle ve Bağla Visio Şekiller](/diagram/tr/java/add-and-connect-visio-shapes/) Microsoft Visio Aspose.Diagram for Java numaralı diyagramlarda bir şeklin nasıl eklenip diğer şekillere bağlanacağı anlatılmaktadır. Bu şekle yapıştırılmış konektörler de bulmak mümkündür.
### **Yapıştırılmış Şekiller Alma**
 Tarafından sunulan GluedShapes yöntemi[Şekil](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape)sınıf, bir şekle yapıştırılmış tüm bağlayıcıların kimliklerinin bir listesini veya söz konusu şekil bir bağlayıcı ise, bağlı olduğu şekillerin kimliklerini almak için kullanılabilir.[Şekil Koleksiyonu](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/shapecollection) class, kimliğine göre bir şekil bulmak için kullanılabilir.

Aşağıdaki kod nasıl yapılacağını gösterir:

1. Bir örnek dosya yükleyin.
1. Belirli bir şekle erişin.
1. Bu şekle yapıştırılmış tüm bağlayıcıların kimliklerinin bir listesini alın.
#### **Bağlayıcıları Yapıştırılmış Programlama Örneği Alın**
Aspose.Diagram for Java kullanarak bir şekle yapıştırılmış tüm konektörleri bulmak için Java uygulamanızda aşağıdaki kodu kullanın.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-Glue-GetGluedConnectors-GetGluedConnectors.java" >}}
## **Yapıştırıcı Visio Şekilleri Bağlantı Noktasıyla Birlikte**
Aspose.Diagram for Java, geliştiricilerin bağlantı noktalarından şekilleri birbirine yapıştırmasına olanak tanır.
### **Tutkal Şekilleri**
 Tarafından sunulan GlueShapes yöntemi[Sayfa](https://reference.aspose.com/diagram/java/com.aspose.diagram/page) sınıf kullanılabilir.

|<p>**Giriş diagram** </p><p>![yapılacaklar:resim_alternatif_Metin](http://i.imgur.com/Z69f4hg.png)</p>|<p>**Şekilleri yapıştırdıktan sonra diagram** </p><p>![yapılacaklar:resim_alternatif_Metin](http://i.imgur.com/5TJpDwc.png)</p>|
|:- |:- |
Aşağıdaki kod nasıl yapılacağını gösterir:

1. Bir örnek dosya yükleyin.
1. Şekilleri yapıştırın.
1. diagram'i kaydedin.
#### **Tutkal Visio Şekil Programlama Örneği**
Bağlantı noktalarından şekilleri yapıştırmak için Java uygulamanızda aşağıdaki kodu kullanın:

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-Glue-GlueVisioShapes-GlueVisioShapes.java" >}}
## **Kabın İçindeki Tutkal Şekilleri**
Aspose.Diagram for Java, geliştiricilerin grup şekillerini bir kapsayıcı içine yapıştırmalarına olanak tanır.
### **Tutkal Grubu Şekli**
Page sınıfı tarafından sunulan GlueShapesInContainer yöntemi kullanılabilir.

|<p>**Giriş diagram** </p><p>![yapılacaklar:resim_alternatif_Metin](http://i.imgur.com/HRRzIEh.png)</p>|<p>**Grup şekillerini yapıştırdıktan sonra diagram** </p><p>![yapılacaklar:resim_alternatif_Metin](http://i.imgur.com/YxCiOgU.png)</p>|
|:- |:- |
Aşağıdaki kod nasıl yapılacağını gösterir:

1. Bir örnek dosya yükleyin.
1. Grup şekillerini yapıştırın.
1. diagram'i kaydedin.
#### **Şekilleri Programlama Örneği İçinde Tutkalla**
Grup şeklini bir kabın içine yapıştırmak için Java uygulamanızda aşağıdaki kodu kullanın:

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-Glue-GlueContainerShape-GlueContainerShape.java" >}}
