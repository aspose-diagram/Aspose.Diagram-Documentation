---
title: Bir Şeklin Pin Değerlerini ve Ayar Boyutunu Hesaplayın
type: docs
weight: 60
url: /tr/net/calculate-pin-values-and-setting-size-of-a-shape/
description: Bu bölümde Aspose.Diagram ile Alt Şeklin PinX ve PinY Değerlerinin nasıl hesaplanacağı açıklanmaktadır.
---
## **Alt Şeklin PinX ve PinY Değerlerini Hesaplayın**
 Şekil, grup şeklinin bir alt düğümüyse, xformu, ana şeklinin göreli bir koordinatıdır, ancak mutlak koordinat değildir.[Sayfa](http://www.aspose.com/api/net/diagram/aspose.diagram/page). Kullanıcının mutlak koordinatı alması gerekiyorsa, bu örnek kod yardımcı olur.

Yerel koordinatlarda belirtilen bir nokta, aşağıdaki dönüşümler aşağıdaki sırayla uygulanarak ana koordinatlara dönüştürülebilir:

1. Cell_Type öğesinin LocPinX özelliğinin değerini x koordinatından çıkarın.
1. Cell_Type'ın LocPinY özelliğinin değerini y koordinatından çıkarın.
1. Cell_Type öğesinin FlipX özelliğinin değeri bire eşitse, noktayı y ekseni etrafında aynalayın.
1. Cell_Type öğesinin FlipY özelliğinin değeri bire eşitse, noktayı x ekseni etrafında aynalayın.
1. Noktayı, Cell_Type öğesinin Angle özelliğinin değerine göre orijin etrafında saat yönünün tersine döndürün.
1. PinX Cell_Type değerini x koordinatına ekleyin.
1. PinY Cell_Type değerini y koordinatına ekleyin.
### **PinX ve PinY Programlama Örneğinin Hesaplanması**
Aspose.Diagram for .NET API kullanarak bir alt şeklin PinX ve PinY değerlerini hesaplamak için .NET uygulamanızda aşağıdaki kodu kullanın.







{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-CalculateCenterOfSubShapes-CalculateCenterOfSubShapes.cs" >}}
## **Bir Şeklin Yüksekliğini ve Genişliğini Ayarlama**
 bu[Şekil](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) Class, SetHeight ve SetWidth yöntemlerini kullanarak şeklin yüksekliğini ve genişliğini belirleyerek şeklin boyutunu kontrol etmenizi sağlar.

 Tarafından sunulan SetHeight ve SetWidth yöntemleri[Şekil](http://www.aspose.com/api/net/diagram/aspose.diagram/shape)sınıf, bir şekli kalıpla, kalıp olmadan veya bir grup şekli biçiminde yeniden boyutlandırmayı destekler. Bu makaledeki kod örnekleri, sayfadaki şekli yeniden boyutlandırmak için Yükseklik ve Genişliği ayarlar.

Yükseklik ve Genişliği ayarlama işlemi şu şekildedir:

1. diagram yükleyin.
1. Belirli bir şekil bulun.
1. Bir şeklin yüksekliğini ayarlayın.
1. Bir şeklin Genişliğini ayarlayın.
1. diagram'i kaydedin.
### **Ayar Yükseklik ve Genişlik Programlama Örneği**
Aşağıdaki kod parçacığı, şeklin yüksekliğini ve genişliğini nasıl ayarlayacağınızı gösterir. Kod, şekil kimliği 1 olan bir şekil adı dikdörtgeni arar ve Yükseklik ve Genişliğini çift olarak ayarlar.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-ChangeShapeSize-ChangeShapeSize.cs" >}}
