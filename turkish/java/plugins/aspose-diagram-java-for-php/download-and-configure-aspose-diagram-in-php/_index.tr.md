---
title: PHP'de Aspose.Diagram'i İndirin ve Yapılandırın
type: docs
weight: 10
url: /tr/java/download-and-configure-aspose-diagram-in-php/
---
## **Gerekli Kitaplıkları İndirin**
Aşağıda belirtilen gerekli kütüphaneleri indirin. Bunlar, Ruby örnekleri için Aspose.Diagram Java'i çalıştırmak için gereklidir.

- [Aspose.Diagram for Java Bileşen](https://repository.aspose.com/webapp/#/artifacts/browse/tree/General/repo/com/aspose/aspose-diagram)
## **Sosyal Kodlama Sitelerinden Örnekler İndirin**
Çalışan örneklerin aşağıdaki yayınları, aşağıda belirtilen sosyal kodlama sitelerinden indirilebilir:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/tree/master/Plugins/Aspose_Diagram_Java_for_PHP)
## **yükleme**
PHP için Aspose.Diagram Java kurulumu çok basit ve kolaydır, lütfen talimatları izleyin:

Aşağıdaki komutu çalıştırın.

{{< highlight "java" >}}

 $ gem install asposediagramjava

{{< /highlight >}}
## **kullanma**
visio çizimini Pdf belgesine aktarmak için gerekli dosyaları ekleyin.

{{< highlight "java" >}}

 require File.dirname(File.dirname(File.dirname(__FILE__))) + '/lib/asposediagramjava'

include Asposediagramjava

include Asposediagramjava::ExportToPdf

initialize_aspose_Diagram

{{< /highlight >}}

Yukarıdaki kodu anlayalım.

1. İlk satır, Aspose.Diagram'in yüklendiğinden ve kullanılabilir olduğundan emin olur.
1. Aspose.Diagram'e erişmek için gereken dosyaları ekleyin
1. Kitaplıkları başlat. aspose Java sınıfları, aspose.yml dosyasında sağlanan yoldan yüklenir
