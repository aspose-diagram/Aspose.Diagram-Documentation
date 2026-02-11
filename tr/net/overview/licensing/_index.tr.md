---
title: lisanslama
type: docs
weight: 50
url: /tr/net/licensing/
description: Aspose. Diagram for .NET müşterilerini Klasik lisans ve Sayaçlı Lisans almaya davet ediyor. Ürünü daha iyi keşfetmek için sınırlı bir lisans kullanmanın yanı sıra.
---
## **Değerlendir Aspose.Diagram**
Aspose.Diagram for .NET ürününü değerlendirme amaçlı kolayca indirebilirsiniz. Lütfen şuraya bakın:[Aspose.Diagram for .NET indirme sayfası](https://www.nuget.org/packages/Aspose.Diagram/)en son sürümü öğrenmek için. Değerlendirme indirmesi, satın alınan indirme ile aynıdır. Değerlendirme sürümü, lisansı uygulamak için birkaç satır kod eklediğinizde kolayca lisanslanır.

Aspose.Diagram değerlendirme sürümü (belirtilen bir lisans olmadan) tam ürün işlevselliği sağlar, ancak belgenin ortasına aç ve kaydet üzerine bir değerlendirme filigranı ekler ve Visio diagram dosyanızın ilk sayfasının yalnızca ilk on şeklini okumayı sınırlar. .

![yapılacaklar:resim_alternatif_Metin](licensing_1.png)
### **Değerlendirme Sürümü Sınırlamaları**
Değerlendirme sürümü, aşağıdakiler dışında tüm özellikleri sağlar:

- Visio diagram ilk sayfasının sadece ilk on şeklini okuyabilirsiniz.
- Dışa aktarılan resimlerde ve PDF dosyalarında da değerlendirme filigranı göreceksiniz.

{{% alert color="primary" %}} 

 Aspose.Diagram'i değerlendirme kısıtlamaları olmadan denemek istiyorsanız, 30 günlük geçici bir lisans talep edin. Bakınız[Geçici Lisans nasıl alınır?](https://purchase.aspose.com/temporary-license) daha fazla bilgi için.

{{% /alert %}} 
## **Bir Lisansın Uygulanması**
kendinle mutlu olduktan sonra[değerlendirme](https://downloads.aspose.com/diagram/net) Aspose.Diagram for .NET, Aspose web sitesinden bir lisans satın alın:[Satın Alma Portalı](https://purchase.aspose.com/buy) . Mevcut farklı lisans türlerini öğrenin. Eğer sorunuz varsa,[Aspose satış ekibiyle iletişime geçin](https://about.aspose.com/contact) ve size yardımcı olmaktan mutluluk duyacaklardır.

Her Aspose lisansı, bu süre içinde çıkan tüm yeni sürümlere veya düzeltmelere ücretsiz yükseltmeler için bir yıllık abonelik içerir. Hem lisanslı hem de değerlendirme kullanıcılarına ücretsiz ve sınırsız teknik destek sağlıyoruz.

Lisans, ürün adı, lisanslı geliştirici sayısı, abonelik bitiş tarihi vb. gibi ayrıntıları içeren düz metin bir XML dosyasıdır. Dosya dijital olarak imzalanmıştır, bu nedenle dosyayı değiştirmeyin: dosyaya fazladan bir satır sonu eklemek bile dosyayı geçersiz kılar.
### **Lisans Ne Zaman Uygulanmalı?**
Bu basit kuralları takip edin:

- Lisansın uygulama etki alanı başına yalnızca bir kez ayarlanması gerekir.
- Diğer Aspose.Diagram sınıflarını kullanmadan önce lisansı ayarlamanız gerekir.
- SetLicense'i birden çok kez aramak zararlı değildir, ancak işlemci zamanını boşa harcar.
- Bir Windows Forms veya konsol uygulaması geliştiriyorsanız, Aspose.Diagram sınıflarını kullanmadan önce başlangıç kodunda SetLicense'i arayın.
- Bir ASP.NET uygulaması geliştirirken, Aplication_Start korumalı yönteminde Global.asax.cs dosyasından SetLicense'i çağırın. Uygulama başladığında bir kez çağrılır.
- SetLicense'i Page_Load metodları içerisinden çağırmayınız çünkü bu, bir web sayfası her yüklendiğinde lisansın da yükleneceği anlamına gelmektedir.
- Bir sınıf kitaplığı geliştiriyorsanız, Aspose.Diagram kullanan sınıfın statik oluşturucusundan SetLicense'i çağırırsınız. Statik oluşturucu, Aspose.Diagram lisansının doğru şekilde ayarlandığından emin olarak sınıfınızın bir örneği oluşturulmadan önce yürütülür.
### **Dosya veya Akış Nesnesi Kullanarak Lisansı Uygulayın**
 Kullan[Lisans.SetLicense](https://reference.aspose.com/diagram/net/aspose.diagram/license)bileşeni lisanslama yöntemi. Bir lisans ayarlamanın en kolay yolu, lisans dosyasını Aspose.Diagram.dll ile aynı klasöre koymak ve aşağıda gösterildiği gibi dosya adını yolsuz olarak belirtmektir.
#### **Dosyadan Lisans Yükleme**
Bu kod parçacığı, bir dosyada veya katıştırılmış bir kaynakta depolanan bir lisansı başlatır.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// Set path of the license file, i.e. c:\temp\
string dataDir = @"c:\temp\";

License license = new License();
license.SetLicense(dataDir + "Aspose.Diagram.lic");

{{< /highlight >}}
```
#### **Akış Nesnesinden Lisans Yükleme**
Bu kod parçacıkları, lisansı akıştan başlatır.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// Set path of the license file, i.e. c:\temp\
string dataDir = @"c:\temp\";
// Load an existing Visio file in the stream
FileStream LicStream = new FileStream(dataDir + "Aspose.Diagram.lic", FileMode.Open);

License license = new License();
license.SetLicense(LicStream);

{{< /highlight >}}
```
## **Tarifeli Lisansı Uygula**
Aspose.Diagram for .NET API, geliştiricilerin ölçülü lisans uygulamasına olanak tanır. Yeni bir lisanslama mekanizmasıdır. Yeni lisanslama mekanizması, mevcut lisanslama yöntemiyle birlikte kullanılacaktır. API özelliğinin kullanımına göre faturalandırılmak isteyen müşterilerimiz tarifeli lisanslamayı kullanabilirler. Daha fazla ayrıntı için lütfen bkz.[Ölçülü Lisanslama SSS](https://purchase.aspose.com/faqs/licensing/metered)bölüm.

yeni bir sınıf[ölçülü](https://reference.aspose.com/diagram/net/aspose.diagram/metered)ölçülü anahtarı uygulamak için eklendi. Bu kod örneği, ölçülü genel ve özel anahtarların nasıl ayarlanacağını gösterir:

```
{{< highlight "csharp" >}}
// Initialize a Metered license class object
Aspose.Diagram.Metered metered = new Aspose.Diagram.Metered();
// apply public and private keys
metered.SetMeteredKey("your-public-key", "your-private-key");
{{< /highlight >}}
```
