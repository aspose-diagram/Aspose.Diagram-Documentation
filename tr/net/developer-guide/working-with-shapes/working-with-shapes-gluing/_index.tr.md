---
title: Shapes Gluing ile Çalışmak
type: docs
weight: 40
url: /tr/net/working-with-shapes-gluing/
description: Bu bölümde, Aspose.Diagram ile belirli bir şekle yapıştırılan şekillerin nasıl elde edileceği açıklanmaktadır.
---
## **Bağlayıcıları Belirli Bir Şekilde Yapıştırın**
[Ekle ve Bağla Visio Şekiller](https://docs.aspose.com/diagram/net/add-retrieve-copy-and-read-visio-shape-data/) Microsoft Visio Aspose.Diagram for .NET numaralı diyagramlarda bir şeklin nasıl eklenip diğer şekillere bağlanacağı anlatılmaktadır. Bu şekle yapıştırılmış konektörler de bulmak mümkündür.
### **Yapıştırılmış Şekiller Alma**
 Tarafından sunulan GluedShapes yöntemi[Şekil](http://www.aspose.com/api/net/diagram/aspose.diagram/shape)sınıf, bir şekle yapıştırılmış tüm bağlayıcıların kimliklerinin bir listesini veya söz konusu şekil bir bağlayıcı ise, bağlı olduğu şekillerin kimliklerini almak için kullanılabilir.[Şekil Koleksiyonu](http://www.aspose.com/api/net/diagram/aspose.diagram/shapecollection) class, kimliğine göre bir şekil bulmak için kullanılabilir.

Aşağıdaki kod nasıl yapılacağını gösterir:

1. Bir örnek dosya yükleyin.
1. Belirli bir şekle erişin.
1. Bu şekle yapıştırılmış tüm bağlayıcıların kimliklerinin bir listesini alın.
#### **Bağlayıcıları Yapıştırılmış Programlama Örneği Alın**
Aspose.Diagram for .NET kullanarak bir şekle yapıştırılmış tüm konektörleri bulmak için .NET uygulamanızda aşağıdaki kodu kullanın.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-Working-with-Shapes-Gluing-GetGluedConnectors-GetGluedConnectors.cs" >}}
## **Yapıştırıcı Visio Şekilleri Bağlantı Noktasıyla Birlikte**
Aspose.Diagram for .NET, geliştiricilerin bağlantı noktalarından şekilleri birbirine yapıştırmasına olanak tanır.
### **Tutkal Şekilleri**
 Tarafından sunulan GlueShapes yöntemi[Sayfa](http://www.aspose.com/api/net/diagram/aspose.diagram/page) sınıf kullanılabilir.

|<p>**Giriş diagram** </p><p>![yapılacaklar:resim_alternatif_Metin](working-with-shapes-gluing_1.png)</p>|<p>**Şekilleri yapıştırdıktan sonra diagram** </p><p>![yapılacaklar:resim_alternatif_Metin](working-with-shapes-gluing_2.png)</p>|
|:- |:- |
Aşağıdaki kod nasıl yapılacağını gösterir:

1. Bir örnek dosya yükleyin.
1. Şekilleri yapıştırın.
1. diagram'i kaydedin.
#### **Tutkal Visio Şekil Programlama Örneği**
Bağlantı noktalarından şekilleri yapıştırmak için .NET uygulamanızda aşağıdaki kodu kullanın:

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-Working-with-Shapes-Gluing-GlueVisioShapes-GlueVisioShapes.cs" >}}
## **Kabın İçindeki Tutkal Şekilleri**
Aspose.Diagram for .NET, geliştiricilerin grup şekillerini bir kapsayıcı içine yapıştırmalarına olanak tanır.
### **Tutkal Grubu Şekli**
 Tarafından sunulan GlueShapesInContainer yöntemi[Sayfa](http://www.aspose.com/api/net/diagram/aspose.diagram/page) sınıf kullanılabilir.

|<p>**Giriş diagram** </p><p>![yapılacaklar:resim_alternatif_Metin](working-with-shapes-gluing_3.png)</p>|<p>**Grup şekillerini yapıştırdıktan sonra diagram** </p><p>![yapılacaklar:resim_alternatif_Metin](working-with-shapes-gluing_4.png)</p>|
|:- |:- |
Aşağıdaki kod nasıl yapılacağını gösterir:

1. Bir örnek dosya yükleyin.
1. Grup şekillerini yapıştırın.
1. diagram'i kaydedin.
#### **Şekilleri Programlama Örneği İçinde Tutkalla**
Grup şeklini bir kabın içine yapıştırmak için .NET uygulamanızda aşağıdaki kodu kullanın:

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-Working-with-Shapes-Gluing-GlueContainerShape-GlueContainerShape.cs" >}}
