---
title: Katmanlarla Çalışmak
type: docs
weight: 130
url: /tr/net/working-with-layers/
description: Bu bölümde, Aspose.Diagram ile visio şeklinde katman bilgilerinin nasıl ekleneceği veya alınacağı açıklanmaktadır.
---
## **Visio'de Şekil Nesnelerini Katmanlarla Yapılandırma**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) Microsoft Office Visio diagram'deki katmanlarla şekil nesnelerini yapılandırmaya izin verir. Her şekil birden çok katmana ait olabilir, böylece geliştiriciler son kullanıcı ihtiyaçlarına uygun şekilleri yönetebilir. bu[Şekil](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class nesnesi, Visio çiziminde katmanlara şekil nesneleri eklemeye ve katmanlardan kaldırmaya izin veren LayerMember özelliğini sunar. Kullanıcılar bu özellikleri programlı olarak Aspose.Diagram API kullanarak aşağıdaki gibi yönetebilir:
### **Şekil Nesnelerini Yapılandırma Programlama Örneği**
Aşağıdaki kod parçası, şekil nesnesi özelliklerini eklemeye, kaldırmaya ve taşımaya yardımcı olur.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Layers-ConfigureShapeLayers-ConfigureShapeLayers.cs" >}}
## **Visio Diagram'de yeni bir Katman ekleyin**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) geliştiricilerin özel şekil kategorilerini düzenlemek için yeni katmanlar eklemesine ve ardından bu katmanlara programlı olarak şekiller atamasına olanak tanır. bu[Katman Koleksiyonu](http://www.aspose.com/api/net/diagram/aspose.diagram/layercollection) class, yeni bir tane eklemeye izin veren Add yöntemini sunar.[Katman](http://www.aspose.com/api/net/diagram/aspose.diagram/layer) Visio çiziminde. Geliştiriciler, sınıf nesnesini başlatarak Katman özelliklerini ayarlayabilir.
### **Katman Programlama Örneği Ekle**
Aşağıdaki kod parçası, Katman nesneleri eklemeye yardımcı olur.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Layers-AddLayer-AddLayer.cs" >}}
## **Visio Diagram'den Tüm Katmanları Alın**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) Visio diagram'in mevcut katmanlarını almak için geliştiricilere erişim sağlar.[Sayfa Sayfası](http://www.aspose.com/api/net/diagram/aspose.diagram/pagesheet) mülkiyeti[Sayfa](http://www.aspose.com/api/net/diagram/aspose.diagram/page) class, kullanarak bir Visio diagram'den kullanılabilir katmanların listesini almaya izin verir.[Katman Koleksiyonu](http://www.aspose.com/api/net/diagram/aspose.diagram/layercollection) sınıf.
### **Katman Programlama Örneği Al**
Aşağıdaki kod parçası, Katmanların listesini almanıza yardımcı olur.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Layers-RetrieveAllLayers-RetrieveAllLayers.cs" >}}
