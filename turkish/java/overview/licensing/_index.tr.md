---
title: lisanslama
type: docs
weight: 60
url: /tr/java/licensing/
---
## **Değerlendirme Sürümü Sınırlamaları**
 Aspose.Diagram for Java'in ücretsiz değerlendirme sürümü şu adresten indirilebilir:[Aspose Depo](https://repository.aspose.com/webapp/#/artifacts/browse/tree/General/repo/com/aspose/aspose-diagram).
### **sınırlama**
Değerlendirme sürümü, aşağıdakiler dışında tüm özellikleri sağlar:

- VSD dosyanızın sadece ilk sayfasının ilk on şeklini okuyabilirsiniz.
- Dışa aktarılan görüntülerde ve PDF dosyalarında da değerlendirme filigranı göreceksiniz.

 Aspose.Diagram'i değerlendirme kısıtlamaları olmadan denemek istiyorsanız, 30 günlük geçici bir lisans talep edin. Bakınız[Geçici Lisans nasıl alınır?](https://purchase.aspose.com/temporary-license) daha fazla bilgi için.
## **Bir Lisansın Uygulanması**
 değerlendirme sürümünü indirebilirsiniz.**Aspose.Diagram** for Java gelen[Aspose Depo](https://repository.aspose.com/webapp/#/artifacts/browse/tree/General/repo/com/aspose/aspose-diagram). Değerlendirme sürümü, ürünün lisanslı sürümüyle kesinlikle aynı yetenekleri sağlar. Ayrıca, bir lisans satın aldığınızda ve lisansı uygulamak için birkaç satır kod eklediğinizde, değerlendirme sürümü kolayca lisanslanır.

 Değerlendirmenizden memnun olduğunuzda**Aspose.Diagram** , yapabilirsiniz[lisans satın al](https://purchase.aspose.com/buy) Aspose web sitesinde. Sunulan farklı abonelik türleri hakkında bilgi sahibi olun. Herhangi bir sorunuz varsa, Aspose satış ekibiyle iletişime geçmekten çekinmeyin.

Her Aspose lisansı, bu süre içinde çıkan tüm yeni sürümlere veya düzeltmelere ücretsiz yükseltmeler için bir yıllık abonelik içerir. Teknik destek ücretsiz ve sınırsızdır ve hem lisanslı hem de değerlendirme kullanıcılarına sağlanır.

{{% alert color="primary" %}} 

 test etmek istersen**Aspose.Diagram** değerlendirme sürümü sınırlamaları olmadan, 30 günlük bir geçici lisans talep edin. Bakınız[Geçici Lisans nasıl alınır?](https://purchase.aspose.com/temporary-license) daha fazla bilgi için.

{{% /alert %}} 
### **Lisans Ayarlama**
Lisans, ürün adı, lisanslandığı geliştirici sayısı, abonelik bitiş tarihi gibi ayrıntıları içeren bir düz metin XML dosyasıdır. Dosya dijital olarak imzalanmıştır, bu nedenle dosyayı değiştirmeyin; dosyaya yanlışlıkla fazladan bir satır sonu eklenmesi bile dosyayı geçersiz kılacaktır.

Belgelerle herhangi bir işlem yapmadan önce bir lisans başvurusunda bulunmanız gerekir. Bir Diagram nesnesi oluşturmadan önce bunu yaptığınızdan emin olun. Uygulama veya işlem başına yalnızca bir kez lisans ayarlamanız gerekir.

Lisans, aşağıdaki konumlardaki bir akıştan veya dosyadan yüklenebilir:

1. Açık yol.
1. Aspose.Diagram.jar dosyasını içeren klasör.

 Kullan[Lisans.setLicense()](https://reference.aspose.com/diagram/java/com.aspose.diagram/License) bileşeni lisanslama yöntemi. Genellikle bir lisans ayarlamanın en kolay yolu, lisans dosyasını Aspose.Diagram.jar ile aynı klasöre koymak ve aşağıdaki örnekte gösterildiği gibi yolsuz sadece dosya adını belirtmektir:
#### **örnek 1**
 Bu örnekte**Aspose.Diagram** uygulamanızın JAR'larını içeren klasörde lisans dosyasını bulmaya çalışacaktır.

**Java**

{{< highlight "csharp" >}}

 com.aspose.diagram.License license = new com.aspose.diagram.License();

license.setLicense("Aspose.Diagram.Java.lic");

{{< /highlight >}}
#### **Örnek 2**
Akıştan bir lisans başlatır.

**Java**

{{< highlight "csharp" >}}

 com.aspose.diagram.License license = new com.aspose.diagram.License();

license.setLicense(new java.io.FileInputStream("Aspose.Diagram.Java.lic"));

{{< /highlight >}}
### **Lisansı Doğrula**
 Lisansın uygun şekilde ayarlanıp ayarlanmadığını doğrulamak mümkündür. bu[Lisans](https://reference.aspose.com/diagram/java/com.aspose.diagram/License)class, lisans uygun şekilde ayarlanmışsa true değerini döndürecek olan isLicensed alanına sahiptir.

**Java**

{{< highlight "csharp" >}}

 License license = new License();

license.setLicense("Aspose.Diagram.Java.lic");

if (License.isLicensed()) {

    System.out.println("License is Set!");

}

{{< /highlight >}}
## **Tarifeli Lisansı Uygula**
Aspose.Diagram for Java API, geliştiricilerin ölçülü lisans uygulamasına olanak tanır. Yeni bir lisanslama mekanizmasıdır. Yeni lisanslama mekanizması, mevcut lisanslama yöntemiyle birlikte kullanılacaktır. API özelliğinin kullanımına göre faturalandırılmak isteyen müşterilerimiz tarifeli lisanslamayı kullanabilirler. Daha fazla ayrıntı için lütfen bkz.[Ölçülü Lisanslama SSS](https://purchase.aspose.com/faqs/licensing/metered)bölüm.

yeni bir sınıf[ölçülü](https://reference.aspose.com/diagram/java/com.aspose.diagram/Metered) ölçülü anahtarı uygulamak için eklendi. Bu kod örneği, ölçülü genel ve özel anahtarların nasıl ayarlanacağını gösterir:

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-License-PublicAndPrivateKeys-PublicAndPrivateKeys.java" >}}
