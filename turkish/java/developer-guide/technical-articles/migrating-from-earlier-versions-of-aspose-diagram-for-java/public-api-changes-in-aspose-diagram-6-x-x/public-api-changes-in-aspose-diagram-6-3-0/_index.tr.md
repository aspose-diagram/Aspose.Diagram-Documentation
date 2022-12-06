---
title: Genel API Aspose.Diagram 6.3.0'daki değişiklikler
type: docs
weight: 40
url: /tr/java/public-api-changes-in-aspose-diagram-6-3-0/
---
{{% alert color="primary" %}} 

Bu belge, modül/uygulama geliştiricilerinin ilgisini çekebilecek Aspose.Diagram API sürüm 6.0.0'dan 6.3.0'a yapılan değişiklikleri açıklamaktadır. Yalnızca yeni ve güncellenmiş genel yöntemleri değil, aynı zamanda Aspose.Diagram'deki perde arkasındaki davranışlardaki değişikliklerin açıklamasını da içerir.

{{% /alert %}} 
## **Visio Dosyasının Biçimini Algılama**
### **Biçimi algılamak için çeşitli Sınıflar, Yöntemler ve Özellikler eklenir**
- **FileFormatUtil ve FileFormatInfo Sınıfları Ekleme** 
 - Bu sınıflar, Visio dosya türünü algılamak için programlı erişim sağlar.
- **FileFormatUtil Sınıfında tespitFileFormat Yöntemi ekler** 
 - Bir dosyada saklanan Visio diagram'in formatı hakkındaki bilgileri algılar ve döndürür.
- **FileFormatInfo Sınıfına FileFormatType Özelliği ekler** 
 - Algılanan dosya biçimini alır.
- **FileFormatInfo'ya LoadFormat Özelliği ekler** 
 - Algılanan yük biçimini alır.

 Geliştiriciler, herhangi bir Visio dosyasının biçimini kolayca algılayabilir. Bu yardım konusu, Visio dosya biçiminin (bir dosya yolu veya akış kullanılarak) nasıl algılanacağını ve uzantısının nasıl kontrol edileceğini gösterir:[Visio Dosyasının Formatını Algıla](/diagram/tr/java/introduction/#Introduction-DetecttheFormatofVisioFile)
## **Kaydederken Gizli Visio Sayfalarının Dışa Aktarılmasını Kontrol Edin**
### **SVGSaveOptions, XPSSaveOptions, ImageSaveOptions, HTMLSaveOptions ve PdfSaveOptions Sınıflarına setExportHiddenPage ekler**
- Gizli Visio sayfalarının dışa aktarılması gerekip gerekmediğini tanımlar.

 Geliştiriciler, Visio diagram'i PDF, HTML, Resim (PNG, JPEG, GIF), SVG ve XPS dosyalarına kaydederken gizli Visio sayfalarını dahil edebilir veya hariç tutabilir. Bu yardım konusu, bunun nasıl yapılacağını gösterir:[Kaydederken Gizli Visio Sayfalarının Dışa Aktarılmasını Kontrol Edin](/diagram/tr/java/set-orientation-and-control-the-export-of-hidden-visio-pages-on-saving/#control-the-export-of-hidden-visio-pages-on-saving)
