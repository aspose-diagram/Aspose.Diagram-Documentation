---
title: Aspose.Diagram'in Diğer Programlama Dillerinde Kullanılması
type: docs
weight: 120
url: /tr/net/utilizing-aspose-diagram-in-other-programming-languages/
description: Bu sayfada Aspose.Diagram'in Diğer Programlama Dillerinde nasıl kullanılacağı açıklanmaktadır.
---
## **Aspose.Diagram for .NET via COM Interop'u kullanın**
 Bu konudaki bilgiler, geliştiricilerin kullanması gereken senaryolar için geçerlidir.[Aspose.Diagram for .NET](/diagram/tr/net/home/) via COM Desteklenen herhangi bir dilde birlikte çalışma.
### **COM Interop ile Çalışma**
Aspose.Diagram for .NET, .NET Framework'in kontrolünde çalışır ve buna yönetilen kod denir. .NET Framework dışında çalışan dillerin tamamında yazılan koda unmanaged code denir. Yönetilmeyen kod ile Aspose.Diagram arasındaki etkileşim, via'de COM Interop adlı .NET tesisinde gerçekleşir.

 Aspose.Diagram nesneleri, .NET nesneleridir, ancak via COM Interop kullanıldığında, programlama dilinizde COM nesneleri olarak görünürler. Bu nedenle, kullanmaya başlamadan önce programlama dilinizde COM nesnelerini nasıl oluşturacağınızı ve kullanacağınızı bildiğinizden emin olmanız en iyisidir.[Aspose.Diagram for .NET](/diagram/tr/net/home/).

- COM dünyasında, COM sunucusunu ve COM istemcisini ayırıyoruz. COM sunucusu COM sınıflarını saklarken, COM istemcisi COM sunucusundan sınıf örnekleri, yani COM nesneleri ister.
-  COM istemcisi veya yalnızca istemci uygulaması, COM sınıfı içerikleri hakkında bir şeyler bilebilir veya yöntemleri ve özellikleri hakkında tamamen bilgisiz olabilir. Bu nedenle istemci uygulaması, COM sınıf yapısını derleme/inşa etme sırasında veya yalnızca yürütme sırasında keşfedebilir. "Keşif" süreci bağlayıcı olarak bilinir ve bu nedenle**erken bağlama** ve**geç bağlama**.
- kısaca COM sınıfı kara kutu gibidir ve onunla çalışmak için tür kitaplığı gereklidir, bu ikili dosya COM sınıfı yöntemlerinin, özelliklerinin ve COM nesneleriyle çalışmayı destekleyen herhangi bir yüksek seviyeli dilin açıklamasına sahiptir ve genellikle tür kitaplığı eklemek için sözdizimi ifadesine sahiptir. mesela bu[**#içe aktarmak**](http://msdn.microsoft.com/en-us/library/8etzzkb6.aspx) C++'de.
- tür kitaplığı erken bağlama için kullanılır.
-  bir COM nesnesi, yöntemlerini ve özelliklerini iki şekilde ortaya çıkarabilir:**sevk arayüzü** (dispinterface) ve içinde**vtable** (sanal işlev tablosu).
-  içinde**dispinterface** , her yöntem ve özellik benzersiz bir üye tarafından tanımlanır; bu üye, işlevin dağıtım tanıtıcısıdır (veya**DispID**).
- **vtable** yalnızca COM sınıfı arabiriminin desteklediği işlevlere yönelik bir dizi işaretçidir.
-  yöntemlerini her iki arabirim aracılığıyla ortaya çıkaran bir nesne,**çift arayüz**.
- her iki bağlama türünün de avantajları vardır. Erken bağlama, size daha yüksek performans ve derleme zamanı sözdizimi denetimi sağlar. Geç bağlama, olmayı planladığınız müşterileri yazarken en avantajlıdır.***gelecekteki sürümlerle uyumlu*** COM sınıfınızın. Geç bağlama ile, tür kitaplığından gelen bilgiler istemcinize "bağlantılı" olmaz, bu nedenle istemcinizin kod değişikliği olmadan COM sınıfının gelecekteki sürümleriyle çalışabileceğinden daha fazla emin olabilirsiniz.
-  geç bağlama mekanizmasının büyük bir avantajı vardır: COM DLL'nin yaratıcısı, farklı bir işlev arayüzü düzenine sahip yeni bir sürüm yayınlamaya karar verirse, bu yöntemleri çağıran herhangi bir kod, yöntemler artık mevcut olmadığı sürece çökmez; olsa bile**vtable**geç bağlama, yeni DISPID'leri keşfetmeyi ve uygun yöntemleri çağırmayı başarır.

 Sonunda uzmanlaşmanız gereken konular şunlardır:

- Programlama dilinizde COM nesnelerini kullanma. Programlama dili belgelerinize ve bu belgede daha ayrıntılı olarak dile özgü konulara bakın.
-  .NET COM Interop tarafından kullanıma sunulan COM nesneleriyle çalışma. Görmek[Yönetilmeyen Kodla Birlikte Çalışma](https://docs.microsoft.com/en-us/dotnet/framework/interop/) ve[.NET Framework Bileşenlerini COM'a maruz bırakma](https://docs.microsoft.com/en-us/dotnet/framework/interop/exposing-dotnet-components-to-com) MSDN'de.
-  Aspose.Diagram belge nesne modeli. Görmek[Aspose.Diagram Programcı Kılavuzu](https://docs.aspose.com/diagram/net/developer-guide/) ve[API Referans](https://reference.aspose.com/diagram/net).
#### **COM Interop ile Aspose.Diagram for .NET'i kaydedin**
Aspose.Diagram for .NET'i kurmanız ve COM Interop'a kayıtlı olduğundan emin olmanız (yönetilmeyen koddan çağrılabilmesini sağlayarak) gerekir.

Aspose.Diagram for .NET'i COM Interop için manuel olarak kaydetmek için:

1.  itibaren**Başlama** menü, seç**Tüm Programlar** , sonra**Microsoft Visual Studio**, **Visual Studio Araçlar** ve sonunda,**Visual Studio Komut İstemi**. Bazı işletim sistemlerinde şu konumda da bulunur: "C:\Program Files (x86)\Microsoft SDKs\Windows\v7.0A\bin\x64"
1.  Derlemeyi kaydetmek için komutu girin:
   1. .NET Framework 2.0
regasm "C:\Program Files\Aspose\Aspose.Diagram for .NET\bin\net2.0\Aspose.Diagram.dll" /kod tabanı
   1. .NET Framework 3.5
 regasm "C:\Program Files\Aspose\Aspose.Diagram for .NET\bin\net3.5\Aspose.Diagram.dll" /kod tabanı
   1. .NET Framework 4.0
 regasm "C:\Program Files\Aspose\Aspose.Diagram for .NET\bin\net4.0\Aspose.Diagram.dll" /kod tabanı

{{% alert color="primary" %}} 

/codebase'in yalnızca Aspose.Diagram.dll GAC'de yoksa gerekli olduğuna dikkat edin, bu seçeneğin kullanılması kayıt defterinde derleme için regasm yerleştirme yolu yapar.

{{% /alert %}} {{% alert color="primary" %}} 

 regasm.exe, .NET Framework SDK'da bulunan bir araçtır. Tüm .NET Framework SDK araçları,*\Microsoft .NET\Framevork\<FrameworkVersion>* dizin, örneğin*C:\Windows\Microsoft .NET\Framework\v4.0.30319*. Visual Studio .NET'i kullanırsanız:
 itibaren**Başlama** menü, seç**Programlar** , bunu takiben**Microsoft Visual Studio .NET** , sonra**Visual Studio .NET Araçlar** ve sonunda,**Visual Studio .NET 2003 Komut İstemi**.
Gerekli tüm ortam değişkenleri ayarlanmış olarak bir komut istemi çalıştırır.

{{% /alert %}} 
##### **ProgID'ler**
ProgID, "programatik tanımlayıcı" anlamına gelir. Bir nesne oluşturmak için kullanılan bir COM sınıfının adıdır. ProgID'ler, "Aspose.Diagram" kitaplık adından ve sınıf adından oluşur.
##### **Tür Kitaplığı**
Programlama diliniz (örneğin Visual Basic veya Delphi) COM tipi bir kitaplığa başvurmanıza izin veriyorsa, o zaman Aspose.Diagram.tlb'ye bir başvuru ekleyin ve Nesne Tarayıcınızdaki tüm Aspose.Diagram for .NET sınıflarını, yöntemlerini, özelliklerini ve sıralamalarını görün.

Bir TLB dosyası oluşturmak için:

- .NET Framework 2.0
 regasm "C:\Program Files\Aspose\Aspose.Diagram for .NET\bin\net2.0\Aspose.Diagram.dll" /tlb: "C:\Program Files\Aspose\Aspose.Diagram for .NET\bin\net2.0\Aspose.Diagram.tlb" /codebase
- .NET Framework 3.5
 regasm "C:\Program Files\Aspose\Aspose.Diagram for .NET\bin\net3.5\Aspose.Diagram.dll" /tlb: "C:\Program Files\Aspose\Aspose.Diagram for .NET\bin\net3.5\Aspose.Diagram.tlb" /codebase
- .NET Framework 4.0
regasm "C:\Program Files\Aspose\Aspose.Diagram for .NET\bin\net4.0\Aspose.Diagram.dll" /tlb: "C:\Program Files\Aspose\Aspose.Diagram for .NET\bin\net4.0\Aspose.Diagram.tlb" /codebase
#### **COM Nesneleri Oluşturma**
Bir COM nesnesinin oluşturulması, normal bir .NET nesnesinin oluşturulmasına benzer. Oluşturulduktan sonra, sanki bir COM nesnesiymiş gibi nesnenin yöntemlerine ve özelliklerine erişebilirsiniz.

Bazı yöntemlerin aşırı yüklemeleri vardır ve bunlar, değişmeden kalan ilk yöntem dışında, COM Interop tarafından kendilerine eklenen sayısal bir sonekle birlikte gösterilir. Örneğin, Diagram.Save yöntemi aşırı yüklemeleri Diagram.Save, Diagram.Save_2 vb. olur.

{{% alert color="primary" %}} 

 Daha fazla bilgi için bu belgedeki dile özgü makalelere bakın.

{{% /alert %}} 
## **Aspose.Diagram Kaynaklar**
Aşağıda, görevlerinizi gerçekleştirmek için ihtiyaç duyabileceğiniz bazı yararlı kaynakların bağlantıları bulunmaktadır.
- [Aspose.Diagram for Java Çevrimiçi Dokümantasyon](https://docs.aspose.com/diagram/java/)
- [Node.js için Aspose.Diagram via Java Çevrimiçi Belgeler](https://docs.aspose.com/diagram/nodejsjava/)
- [Python için Aspose.Diagram via Java Çevrimiçi Dokümantasyon](https://docs.aspose.com/diagram/pythonjava/)

##### **Sarıcı Montajı Oluşturma**
Aspose.Diagram for .NET sınıflarının, yöntemlerinin ve özelliklerinin birçoğunu kullanmanız gerekiyorsa, bir sarmalayıcı derleme oluşturmayı düşünün (C# veya başka bir .NET programlama dili kullanarak). Sarıcı derlemeler, Aspose.Diagram for .NET'in doğrudan yönetilmeyen koddan kullanılmasını önlemeye yardımcı olur.

İyi bir yaklaşım, Aspose.Diagram for .NET'e başvuran ve tüm işi onunla yapan ve yönetilmeyen koda yalnızca en az sayıda sınıf ve yöntem sunan bir .NET derlemesi geliştirmektir. Uygulamanız daha sonra yalnızca sarıcı kitaplığınızla çalışmalıdır.

 via COM Interop'u çağırmanız gereken sınıf ve yöntemlerin sayısını azaltmak, projeyi basitleştirir. .NET sınıfları via COM Interop'u kullanmak genellikle ileri düzey beceriler gerektirir.
## **COM Interop kullanarak PHP'de Boş Bir Visio Çizimi Oluşturun**
### **Önkoşullar**
 PHP'nizi COM ile çalışacak şekilde yapılandırın. Görmek<http://www.php.net/manual/en/ref.com.php> . Daha fazla bilgi için lütfen adlı makaleyi kontrol edin.[Aspose.Diagram for .NET via COM Interop'u kullanın](/diagram/tr/net/home/).
### **Boş Visio Çizimi Oluşturma**
 Bu, kullanarak boş bir Visio çizimini nasıl oluşturacağınızı gösteren basit bir uygulamadır.[Aspose.Diagram for .NET](/diagram/tr/net/home/) PHP via COM Interop'ta.

**PHP**

{{< highlight "csharp" >}}

 <?php

echo "<h3>Calling Aspose.Diagram for .NET from PHP using COM Interoperatibility</h3>";

//set license

$lic = new COM("Aspose.Diagram.License");

$lic->SetLicense("D:\ASPOSE\Licences\Aspose.Total licenses\Aspose.Total.lic");

// create a new instance of Diagram object using COM interop

$diagram = new COM("Aspose.Diagram.Diagram");

// Save the Visio drawing in the VDX format

$diagram->Save("d:\diagramtest\MyOutput.vdx", 0);

?>



{{< /highlight >}}
