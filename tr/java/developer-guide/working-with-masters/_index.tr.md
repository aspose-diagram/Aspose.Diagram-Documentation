---
title: Ustalarla Çalışmak
type: docs
weight: 30
url: /tr/java/working-with-masters/
---
## **Ana Bilgileri Alma**
Bir şekil ustası, Visio şablonunun başka bir adıdır. Aspose.Diagram ile sayfalar, bağlayıcılar ve ayrıca kalıplar hakkında bilgi almak mümkündür. Bu makalede, bir diagram numaralı telefondan kimliğin ve adın nasıl alınacağı açıklanmaktadır.

 bu[Usta](https://reference.aspose.com/diagram/java/com.aspose.diagram/master) nesne temsil eder[Şekil](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape)diagram'de nesnenin yöneticisi. Diagram sınıfı tarafından sunulan Masters özelliği, Aspose.Diagram.Master nesnelerinin bir koleksiyonunu destekler. Bu özellik, ana kimliği ve adı olan ana bilgileri almak için kullanılabilir.

Ana şekil tarafından hangi şeklin devralındığını belirlemek için Page.Shapes özelliğini kullanın.

**Kodun çıktısını gösteren bir konsol penceresi.** 

![yapılacaklar:resim_alternatif_Metin](http://i.imgur.com/DPn5sP9.png)
### **Ana Bilgi Programlama Örneğinin Alınması**
Aşağıdaki kod parçası, bir diagram'den ana bilgileri alır.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Masters-RetrieveMasterInfo-RetrieveMasterInfo.java" >}}
## **Şekiller Şablonundan Master Ekleme**
Şablon, belirli bir Microsoft Office Visio şablonuyla ilişkili bir şekil koleksiyonudur. Aspose.Diagram ile bir şablondan bir çizime herhangi bir ana şekil eklemek mümkündür.
### **Usta Ekle**
Master nesnesi, diagram'de bir Shape nesnesinin master'ını temsil eder. Diagram sınıfı tarafından sunulan AddMaster yöntemi, bir şablondan master eklenmesine izin verir. Aşağıdaki dört yolu sunar:

- Şablon dosyası yolu ve ana kimlik.
- Şablon dosyası yolu ve ana adı.
- Şablon dosyası akışı ve ana kimlik.
- Şablon dosyası akışı ve ana ad.
- diagram kaynağından diagram'e master ekleyin
#### **Ana Programlama Örneği Ekle**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Masters-AddMasterFromStencil-AddMasterFromStencil.java" >}}
## **Sıfırdan Usta Oluştur**
Aspose.Diagram API, herhangi bir şablon, çizim veya şablon olmadan sıfırdan bir Master oluşturmanıza olanak tanır. Geliştiriciler, Master'ın oluşturulmasını özelleştirebilir. Diagram sınıfı tarafından sunulan addMaster yöntemi, bir ana öğe eklenmesine izin verir.
#### **Ana Programlama Örneği Oluşturma**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Masters-CreateMasterfromScratch-CreateMasterfromScratch.java" >}}

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Masters-BASE64Encoder-BASE64Encoder.java" >}}
## **Visio Dosyasından Master Alın**
Bazen, geliştiricilerin bir Visio çizim ustasının ayrıntılarını alması gerekir. Aspose.Diagram API bu özelliği destekler.

 Aspose.Diagram for Java sunuyor[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram)Visio çizimini temsil eden sınıf. Diagram sınıfı tarafından sunulan Masters özelliği, Aspose.Diagram.Master nesne koleksiyonunu destekler. Bu özellik, belirli bir master'ın ayrıntılarını almak için kullanılabilir. MasterCollection sınıfı, bir Master nesnesi almak için çağrılabilen GetMasterByName ve GetMaster yöntemlerini kullanıma sunar.
### **Kimliğe göre Ana Nesne Alma**
Bu örnek şu şekilde çalışır:

1. Diagram sınıfından bir nesne oluşturun.
1. Diagram.Masters sınıfının GetMaster yöntemini çağırın.
#### **Kimliğe Göre Ana Nesne Programlama Örneği**
Aşağıdaki örnek, bir Visio çiziminden kimliğe göre nasıl master alınacağını gösterir.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Masters-GetMasterbyID-GetMasterbyID.java" >}}
### **Ada Göre Ana Nesne Alma**
Bu örnek şu şekilde çalışır:

1. Diagram sınıfından bir nesne oluşturun.
1. Diagram.Masters sınıfının GetMasterByName yöntemini çağırın.
#### **İsme Göre Ana Nesne Programlama Örneği**
Aşağıdaki örnek, bir Visio çiziminden ada göre bir ana nesnenin nasıl alınacağını gösterir.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Masters-GetMasterbyName-GetMasterbyName.java" >}}
## **Visio Çiziminde Master Varlığını Kontrol Edin**
Aspose.Diagram API, Visio çiziminde bir master olup olmadığını kontrol etmeyi destekler. MasterCollection özelliği ile geliştiriciler, adına veya kimliğine göre bir master olup olmadığını kontrol edebilir.

 Aspose.Diagram for Java sunuyor[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) Visio çizimini temsil eden sınıf. Diagram sınıfı tarafından sunulan Masters özelliği, Aspose.Diagram.Master nesne koleksiyonunu destekler. Bu özellik, belirli bir ana öğenin varlığını kontrol etmek için kullanılabilir. MasterCollection sınıfı, master adı veya ID parametresi ile çağrılabilen IsExist yöntemini gösterir.
### **Kimliğe göre Ana Varlığı kontrol etme**
Bu örnek şu şekilde çalışır:

1. Diagram sınıfından bir nesne oluşturun.
1. Diagram.Masters sınıfının IsExist yöntemini çağırın.
#### **ID Programlama Örneği ile Master Presence**
Aşağıdaki örnek, bir Visio çiziminde kimliğe göre bir master varlığının nasıl kontrol edileceğini gösterir.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Masters-CheckMasterPresencebyID-CheckMasterPresencebyID.java" >}}
### **Ada Göre Ana Varlığı Kontrol Etme**
Bu örnek şu şekilde çalışır:

1. Diagram sınıfından bir nesne oluşturun.
1. Diagram.Masters sınıfının IsExist yöntemini çağırın.
#### **Ada Göre Master Presence Programlama Örneği**
Aşağıdaki örnek, Visio çiziminden ada göre bir master varlığının nasıl kontrol edileceğini gösterir.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Masters-CheckMasterPresencebyName-CheckMasterPresencebyName.java" >}}
