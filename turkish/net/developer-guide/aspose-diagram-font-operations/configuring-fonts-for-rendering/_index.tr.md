---
title: İşleme için Yazı Tiplerini Yapılandırma
type: docs
weight: 10
url: /tr/net/configuring-fonts-for-rendering/
---
## **Olası Kullanım Senaryoları**

Aspose.Diagram API'ler, sayfaları görüntü formatlarında oluşturmanın yanı sıra PDF ve XPS formatlarına dönüştürme olanağı sağlar. Dönüştürme doğruluğunu en üst düzeye çıkarmak için elektronik tabloda kullanılan yazı tiplerinin işletim sisteminin varsayılan yazı tipi dizininde bulunması gerekir. Gerekli yazı tiplerinin mevcut olmaması durumunda, Aspose.Diagram API'leri gerekli yazı tiplerini mevcut olanlarla değiştirmeye çalışacaktır.

## **Yazı Tiplerinin Seçimi**

Aspose.Diagram API'lerinin perde arkasında takip ettiği süreç aşağıdadır.

1. API, elektronik tabloda kullanılan yazı tipi adıyla tam olarak eşleşen dosya sistemindeki yazı tiplerini bulmaya çalışır.
1.  API altında tanımlanan yazı tipini bulamazsa**[SaveOptions.DefaultFont](https://reference.aspose.com/diagram/net/aspose.diagram.saving/saveoptions/defaultfont/)** özelliği altında belirtilen yazı tipini kullanmaya çalışır.**[FontConfigs.DefaultFontName](https://reference.aspose.com/diagram/net/aspose.diagram/fontconfigs/defaultfontname/)**Emlak.
1.  API altında tanımlanan yazı tipini bulamazsa**[FontConfigs.DefaultFontName](https://reference.aspose.com/diagram/net/aspose.diagram/fontconfigs/defaultfontname/)** özelliği, mevcut tüm yazı tiplerinden en uygun yazı tiplerini seçmeye çalışır.
1. Son olarak, API, dosya sisteminde herhangi bir yazı tipi bulamazsa, sayfayı Times New Roman kullanarak işler.

## **Özel Yazı Klasörlerini Ayarla**

 Aspose.Diagram API'ler, gerekli yazı tipleri için işletim sisteminin varsayılan yazı tipi dizinini arar. Gerekli yazı tiplerinin sistemin yazı tipi dizininde bulunmaması durumunda, API'ler özel (kullanıcı tanımlı) dizinlerde arama yapar. bu**[Yazı Tipi Yapılandırmaları](https://reference.aspose.com/diagram/net/aspose.diagram/fontconfigs/)** class, aşağıda ayrıntılı olarak açıklandığı gibi, özel yazı tipi dizinlerini ayarlamanın çeşitli yollarını ortaya çıkardı.

1. **[FontConfigs.SetFontFolder](https://reference.aspose.com/diagram/net/aspose.diagram/fontconfigs/setfontfolder/)**: Ayarlanacak yalnızca bir klasör varsa bu yöntem kullanışlıdır.

1. **[FontConfigs.SetFontFolders](https://reference.aspose.com/diagram/net/aspose.diagram/fontconfigs/setfontfolders/)**Bu yöntem, yazı tipleri birden çok klasörde bulunduğunda ve kullanıcı tüm yazı tiplerini tek bir klasörde birleştirmek yerine tüm klasörleri ayrı ayrı ayarlamak istediğinde kullanışlıdır.
1. **[FontConfigs.SetFontSources](https://reference.aspose.com/diagram/net/aspose.diagram/fontconfigs/setfontsources/)**: Bu mekanizma, kullanıcı birden çok klasörden yazı tiplerini veya tek bir yazı tipi dosyasını veya bir bayt dizisinden yazı tipi verilerini yüklemek istediğinde kullanışlıdır.

{{% alert color="primary" %}}

 İkisi birden**[FontConfigs.SetFontFolder](https://reference.aspose.com/diagram/net/aspose.diagram/fontconfigs/setfontfolder/)** & **[FontConfigs.SetFontFolders](https://reference.aspose.com/diagram/net/aspose.diagram/fontconfigs/setfontfolders/)** yöntemler bir Boole tipi ikinci parametreyi kabul eder. Geçen**doğru** çünkü ikinci parametre Aspose.Diagram API'lerini yazı tipi dosyaları için alt klasörleri aramaya yönlendirecektir.

{{% /alert %}}

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-OS-Fonts-Location-SetCustomFontFolders-SetCustomFontFolders.cs" >}}

{{% alert color="primary" %}}

Lütfen başvuru başlangıcında yukarıda belirtilen yöntemlerden herhangi birini kullanınız, yani; Aspose.Diagram API'lerinin diğer nesnelerini çağırmadan önce.

{{% /alert %}} {{% alert color="primary" %}}

Yazı tipi kaynaklarını ayarlamak için yukarıda belirtilen yöntemlerin tümü kullanılırsa, yalnızca son ayarlar geçerli olacaktır.

{{% /alert %}}

