---
title: giriiş
type: docs
weight: 10
url: /tr/net/introduction/
description: Aspose.Diagram kitaplığının tanıtımı.
---
## **Aspose.Diagram for .NET Kütüphanesinin Visio Belge Bilgilerini Alın**
Microsoft Visio, diagram üzerinde yapılan işlemlerle ilgili bilgileri dosya içerisinde saklar. Örneğin, belgenin oluşturulduğu saat ve tarih, en son ne zaman düzenlendiği, yazdırıldığı veya kaydedildiği dosyayla birlikte kaydedilir. Microsoft Visio'in hangi sürümünün oluşturulduğu ve dosyanın en son düzenlendiği bilgisi de kaydedilir.

Bu makalede, bu bilgilerin nasıl alınacağı açıklanmaktadır.
### **Bir Belgenin Oluşturulduğu, Düzenlendiği ve Kaydedildiği Microsoft Visio Sürümünün Belirlenmesi**
 Tarafından sunulan Version özelliği[Diagram](https://reference.aspose.com/diagram/net/aspose.diagram/diagram/)sınıfı ve DocumentProperties sınıfı tarafından sunulan BuildNumberCreated özelliği, belgeyi oluşturmak için kullanılan Microsoft Visio örneğinin sürümünü ve tam yapı numarasını belirlemek için kullanılır.

 Tarafından sunulan BuildNumberEdited özelliği[Döküman özellikleri](https://reference.aspose.com/diagram/net/aspose.diagram/documentproperties) class, belgeyi düzenlemek için kullanılan Microsoft Visio örneğinin tam yapı numarasını belirlemek için kullanılır.

DocumentProperties sınıfı tarafından sunulan TimeCreated, TimeEdited, TimePrinted ve TimeSaved özellikleri, Microsoft Visio belgesinin oluşturulduğu, son düzenlendiği, son yazdırıldığı ve son kaydedildiği zamanı belirlemek için kullanılır.

Dosyadaki bilgileri değiştirmek için bu özellikleri de ayarlayabilirsiniz. Aşağıdaki kod örnekleri, dosyanın ne tarafından oluşturulduğu, ne zaman oluşturulduğu, düzenlendiği, yazdırıldığı ve kaydedildiği hakkında bilgilerin nasıl alınacağını gösterir.
#### **Programlama Örneği**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Introduction-GetLibraryVersion-GetLibraryVersion.cs" >}}
## **Yazma Visio Belge Özet Bilgileri**
Microsoft Visio, sizin ve iş arkadaşlarınızın bir diagram'i tanımlamasına yardımcı olacak bir dizi belge özeti bilgisi özelliği tanımlamanıza olanak tanır. Başlık, konu, yazar ve açıklama gibi özet özellikler, dosyanın aranırken bulunmasını ve arandığında tanınmasını kolaylaştırır. dosya tarama
### **Yazma Microsoft Visio Doküman Özet Bilgi**
DocumentProperties sınıfı, bir Microsoft Visio diagram'in özet bilgilerini ayarlamak veya almak için bir dizi özellik sunar. Aspose.Diagram for .NET çizim özet bilgilerini güncelleyebilir ve ardından çizim dosyasını VDX'e geri yazabilir.

{{% alert color="primary" %}} 

karşı değerler ayarlayamayacağınızı lütfen unutmayın.**Başvuru**ve**Üretici**çünkü bu alanların karşısında Aspose Ltd. ve Aspose.Diagram for .NET xxx görüntülenecektir.

{{% /alert %}} 

Mevcut bir VDX veya VSD dosyasının çizim özeti bilgilerini güncellemek için:

1.  örneğini oluşturun[Diagram](https://reference.aspose.com/diagram/net/aspose.diagram/diagram/) sınıf.
1.  Gösterilen özellikleri ayarla[Diagram.DocumentProps](https://reference.aspose.com/diagram/net/aspose.diagram/diagram/properties/documentprops) Visio çizim dosyası için özet bilgileri tanımlamak için.
1. Visio çizim dosyasını VDX'e yazmak için Diagram sınıfının Save yöntemini çağırın.

Özet bilgileri kontrol edin:

1. VDX çıkış dosyasını Microsoft Visio'de açın.
1. Dosya menüsünden Bilgi seçimi.
#### **Yazma Visio Doküman Özet Bilgi Programlama Örneği**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Introduction-SetVisioProperties-SetVisioProperties.cs" >}}
## **Visio Dosyasının Formatını Algıla**
Geliştiriciler, Aspose.Diagram for .NET API'i kullanarak, dosya uzantısı dosya içeriğinin uygun olduğunu garanti etmediğinden, Visio dosyasının biçimini dosyayı açmadan önce algılayabilir.
### **Biçim Programlama Örneği Algıla**
Aşağıdaki örnek kod, bir dosya biçiminin (dosya yolu veya akışı kullanılarak) nasıl algılanacağını ve uzantısının nasıl kontrol edileceğini gösterir.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Introduction-DetectVisioFileFormat-DetectVisioFileFormat.cs" >}}
