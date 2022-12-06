---
title: giriiş
type: docs
weight: 10
url: /tr/java/introduction/
---
{{% alert color="primary" %}} 

Microsoft Visio, diagram üzerinde yapılan işlemlerle ilgili bilgileri dosya içerisinde saklar. Örneğin, belgenin oluşturulduğu saat ve tarih, en son ne zaman düzenlendiği, yazdırıldığı veya kaydedildiği dosyayla birlikte kaydedilir. Microsoft Visio'in hangi sürümünün oluşturulduğu ve dosyanın en son düzenlendiği bilgisi de kaydedilir.

Bu makalede, bu bilgilerin nasıl alınacağı açıklanmaktadır.

{{% /alert %}} 
## **Aspose.Diagram for Java Kitaplığının Versiyonunu Alın**
 tarafından sunulan getVersion() yöntemi[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/Diagram) sınıfı ve tarafından sunulan getBuildNumberCreated() yöntemi[Döküman özellikleri](https://reference.aspose.com/diagram/java/com.aspose.diagram/DocumentProperties) sınıfı, belgeyi oluşturmak için kullanılan Microsoft Visio örneğinin sürümünü ve tam yapı numarasını belirlemek için kullanılır.
### **Bir Belgenin Oluşturulduğu, Düzenlendiği ve Kaydedildiği Microsoft Visio Sürümünün Belirlenmesi**
 tarafından sunulan getBuildNumberEdited() yöntemi[Döküman özellikleri](https://reference.aspose.com/diagram/java/com.aspose.diagram/DocumentProperties) class, belgeyi düzenlemek için kullanılan Microsoft Visio örneğinin tam yapı numarasını belirlemek için kullanılır.

tarafından sunulan getTimeCreated(), getTimeEdited(), getTimePrinted() ve getTimeSaved() yöntemleri[Döküman özellikleri](https://reference.aspose.com/diagram/java/com.aspose.diagram/DocumentProperties) sınıfı, Microsoft Visio belgesinin oluşturulduğu, en son düzenlendiği, en son yazdırıldığı ve en son kaydedildiği zamanı belirlemek için kullanılır.

Dosyadaki bilgileri değiştirmek için bu özellikleri de ayarlayabilirsiniz.

Aşağıdaki kod örnekleri, dosyanın ne tarafından oluşturulduğu, ne zaman oluşturulduğu, düzenlendiği, yazdırıldığı ve kaydedildiği hakkında bilgilerin nasıl alınacağını gösterir.

**Bir konsol penceresindeki kod çıktısı** 

![yapılacaklar:resim_alternatif_Metin](introduction_1.png)
#### **Programlama Örneği**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Introduction-GetLibraryVersion-GetLibraryVersion.java" >}}
## **Yazma Microsoft Visio Doküman Özet Bilgi**
Microsoft Visio, sizin ve iş arkadaşlarınızın bir diagram'i tanımlamasına yardımcı olacak bir dizi belge özeti bilgisi özelliği tanımlamanıza olanak tanır. Başlık, konu, yazar ve açıklama gibi özet özellikler, arama yaparken dosyayı bulmayı ve göz atarken tanımayı kolaylaştırır Dosyalar.

 bu[Döküman özellikleri](https://reference.aspose.com/diagram/java/com.aspose.diagram/DocumentProperties)class, bir Microsoft Visio diagram'in özet bilgilerini ayarlamak veya almak için bir dizi özellik sunar. Aspose.Diagram for Java çizim özet bilgilerini güncelleyebilir ve ardından çizim dosyasını VDX'e geri yazabilir.

{{% alert color="primary" %}} 

karşı değerler ayarlayamayacağınızı lütfen unutmayın.**Başvuru**ve**Üretici**çünkü bu alanların karşısında Aspose Ltd. ve Aspose.Diagram for Java xxx görüntülenecektir.

{{% /alert %}} 
### **Yazma Microsoft Visio Doküman Özet Bilgi**
Mevcut bir VDX veya VSD dosyasının çizim özeti bilgilerini güncellemek için:

1.  örneğini oluşturun[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/Diagram) sınıf.
1. Diagram çizim dosyası için özet bilgileri tanımlamak üzere Diagram.getDocumentProps() yöntemi tarafından sunulan özellikleri ayarlayın.
1. Visio çizim dosyasını VDX'e yazmak için Diagram sınıfının save() yöntemini çağırın.

Özet bilgileri kontrol edin:

1. VDX çıkış dosyasını Microsoft Visio'de açın.
1.  seçme**Bilgi** dan**Dosya** Menü.

**Güncellenmiş özet bilgileri gösteren Bilgi iletişim kutusu** 

![yapılacaklar:resim_alternatif_Metin](introduction_2.png)
#### **Programlama Örneği**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Introduction-SetVisioProperties-SetVisioProperties.java" >}}
## **Visio Dosyasının Biçimini Algılama**
 kullanma[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/)API, geliştiriciler Visio dosyasının biçimini dosyayı açmadan önce algılayabilir çünkü dosya uzantısı dosya içeriğinin uygun olduğunu garanti etmez.
### **Biçim Programlama Örneği Algıla**
Aşağıdaki örnek kod, bir dosya biçiminin (dosya yolu veya akışı kullanılarak) nasıl algılanacağını ve uzantısının nasıl kontrol edileceğini gösterir.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Introduction-DetectVisioFileFormat-DetectVisioFileFormat.java" >}}
## **Visio Dosyasının Biçimini Bir InputStream'den Algılama**
Aspose.Diagram for Java API'i kullanan geliştiriciler, bir giriş akışı geçirerek Visio dosyasının biçimini algılayabilir. Bunu başarmak için FileFormatUtil sınıfının DetectFileFormat yöntemi kullanılabilir.
### **Bir InputStream Programlama Örneğinden Format Algılama**
Aşağıdaki örnek kod, bir giriş akışı kullanılarak bir dosya biçiminin nasıl algılanacağını gösterir.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Introduction-DetectFormatfromInputStream-DetectFormatfromInputStream.java" >}}
