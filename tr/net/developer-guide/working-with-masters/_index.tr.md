---
title: Ustalarla Çalışmak
type: docs
weight: 70
url: /tr/net/working-with-masters/
description: Bu bölümde Aspose.Diagram ile master ekleme veya master bilgilerinin nasıl alınacağı açıklanmaktadır.
---
## **Ana Bilgileri Alma**
Bir şekil ustası, Visio şablonunun başka bir adıdır. Aspose.Diagram ile sayfalar, konektörler ve ayrıca master'lar hakkında bilgi almak mümkündür. Bu makalede, bir diagram numaralı telefondan kimliğin ve adın nasıl alınacağı açıklanmaktadır.

 bu[Usta](http://www.aspose.com/api/net/diagram/aspose.diagram/master) nesne temsil eder[Şekil](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) diagram'de nesnenin yöneticisi. Diagram sınıfı tarafından sunulan Masters özelliği, Aspose.Diagram.Master nesnelerinin bir koleksiyonunu destekler. Bu özellik, ana kimliği ve adı olan ana bilgileri almak için kullanılabilir. Ana şekil tarafından hangi şeklin devralındığını belirlemek için Page.Shapes özelliğini kullanın.
### **Ana Bilgi Programlama Örneğinin Alınması**
Aşağıdaki kod parçası, bir diagram'den ana bilgileri alır.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Masters-RetrieveMasterInfo-RetrieveMasterInfo.cs" >}}
## **Şekiller Şablonundan Master Ekleme**
Şablon, belirli bir Microsoft Office Visio şablonuyla ilişkili bir şekil koleksiyonudur. Aspose.Diagram ile bir şablondan bir çizime herhangi bir ana şekil eklemek mümkündür.
### **Usta Ekle**
 bu[Usta](http://www.aspose.com/api/net/diagram/aspose.diagram/master) nesne temsil eder[Şekil](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) diagram'de nesnenin yöneticisi. Diagram sınıfı tarafından sunulan AddMaster yöntemi, bir şablondan bir ana öğe eklenmesine izin verir. Aşağıdaki dört yolu sunar:

- Şablon dosyası yolu ve ana kimlik.
- Şablon dosyası yolu ve ana adı.
- Şablon dosyası akışı ve ana kimlik.
- Şablon dosyası akışı ve ana ad.
- diagram kaynağından diagram'e master ekleyin
#### **Ana Programlama Örneği Ekle**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Masters-AddMasterFromStencil-AddMasterFromStencil.cs" >}}
## **Sıfırdan Usta Oluştur**
 Aspose.Diagram API oluşturmaya izin verir[Usta](http://www.aspose.com/api/net/diagram/aspose.diagram/master) herhangi bir şablon, çizim veya şablon olmadan sıfırdan. Geliştiriciler, Master'ın oluşturulmasını özelleştirebilir. Diagram sınıfı tarafından sunulan AddMaster yöntemi, bir ana öğe eklenmesine izin verir.
### **Ana Programlama Örneği Oluşturma**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Load-Save-Convert-CreateMasterFromScratch-CreateMasterFromScratch.cs" >}}
## **Visio Dosyasından Master Alın**
Bazen, geliştiricilerin bir Visio çizim ustasının ayrıntılarını alması gerekir. Aspose.Diagram API bu özelliği destekler.

 Aspose.Diagram for .NET sunuyor[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram)Visio çizimini temsil eden sınıf. Diagram sınıfı tarafından sunulan Masters özelliği, Aspose.Diagram.Master nesne koleksiyonunu destekler. Bu özellik, belirli bir master'ın ayrıntılarını almak için kullanılabilir. MasterCollection sınıfı, bir Master nesnesi almak için çağrılabilen GetMasterByName ve GetMaster yöntemlerini kullanıma sunar.
### **Kimliğe göre Ana Nesne Alma**
Bu örnek şu şekilde çalışır:

1. Diagram sınıfından bir nesne oluşturun.
1. Diagram.Masters sınıfının GetMaster yöntemini çağırın.
#### **Kimliğe Göre Ana Nesne Programlama Örneği**
Aşağıdaki örnek, bir Visio çiziminden kimliğe göre nasıl master alınacağını gösterir.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Masters-GetMasterbyID-GetMasterbyID.cs" >}}
### **Ada Göre Ana Nesne Alma**
Bu örnek şu şekilde çalışır:

1. Diagram sınıfından bir nesne oluşturun.
1. Diagram.Masters sınıfının GetMasterByName yöntemini çağırın.
#### **İsme Göre Ana Nesne Programlama Örneği**
Aşağıdaki örnek, bir Visio çiziminden ada göre bir ana nesnenin nasıl alınacağını gösterir.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Masters-GetMasterbyName-GetMasterbyName.cs" >}}
## **Visio Çiziminde Master Varlığını Kontrol Edin**
Aspose.Diagram API, Visio çiziminde bir master olup olmadığını kontrol etmeyi destekler. MasterCollection özelliği ile geliştiriciler, adına veya kimliğine göre bir master olup olmadığını kontrol edebilir.

 Aspose.Diagram for .NET sunuyor[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) Visio çizimini temsil eden sınıf. Diagram sınıfı tarafından sunulan Masters özelliği, Aspose.Diagram.Master nesne koleksiyonunu destekler. Bu özellik, belirli bir ana öğenin varlığını kontrol etmek için kullanılabilir. MasterCollection sınıfı, master adı veya ID parametresi ile çağrılabilen IsExist yöntemini gösterir.
### **Kimliğe göre Ana Varlığı kontrol etme**
Bu örnek şu şekilde çalışır:

1. Diagram sınıfından bir nesne oluşturun.
1. Diagram.Masters sınıfının IsExist yöntemini çağırın.
#### **ID Programlama Örneği ile Master Presence**
Aşağıdaki örnek, bir Visio çiziminde kimliğe göre bir master varlığının nasıl kontrol edileceğini gösterir.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Masters-CheckMasterPresencebyID-CheckMasterPresencebyID.cs" >}}
### **Ada Göre Ana Varlığı Kontrol Etme**
Bu örnek şu şekilde çalışır:

1. Diagram sınıfından bir nesne oluşturun.
1. Diagram.Masters sınıfının IsExist yöntemini çağırın.
#### **Ada Göre Master Presence Programlama Örneği**
Aşağıdaki örnek, Visio çiziminden ada göre bir master varlığının nasıl kontrol edileceğini gösterir.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Masters-CheckMasterPresencebyName-CheckMasterPresencebyName.cs" >}}
