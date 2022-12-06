---
title: İlk Başvurunuz Aspose.Diagram - Hello World
type: docs
weight: 30
url: /tr/java/your-first-aspose-diagram-application-hello-world/
description: Bu sayfada Aspose.Diagram kitaplığı ile ilk uygulamanın nasıl oluşturulacağı açıklanmaktadır.
---
{{% alert color="primary" %}}

Bu öğretici, Aspose.Diagram' basit API'i kullanarak ilk uygulamanın (Hello World) nasıl oluşturulacağını gösterir. Bu basit uygulama, belirli bir Sayfada 'Hello World' metniyle bir Microsoft Visio dosyası oluşturur.

{{% /alert %}}

## **Hello World Uygulamasını Oluşturma**

Aşağıdaki adımlar, Aspose.Diagram API'i kullanarak Hello World uygulamasını oluşturur:

1.  örneğini oluşturun[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) sınıf.
1.  Ehliyetin varsa o zaman[uygula](https://reference.aspose.com/diagram/java/com.aspose.diagram/License).
 Değerlendirme sürümünü kullanıyorsanız, lisansla ilgili kod satırlarını atlayın.
1. Yeni bir Visio dosyası oluşturun veya mevcut bir Visio dosyasını açın.
1. Yeni bir metin kutusu oluşturun.
1.  kelimeleri ekle**Hello World!** bir metin kutusuna.
1. Değiştirilen Microsoft Visio dosyasını oluşturun.

Yukarıdaki adımların uygulanması aşağıdaki örneklerde gösterilmektedir.

### **Kod Örneği: Yeni Bir Diagram Oluşturma**

Aşağıdaki örnek sıfırdan yeni bir diagram oluşturur, Hello World yazar! ilk sayfada ve Visio dosyasını kaydeder.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-CreateNewVisio-CreateNewVisio.java" >}}

### **Kod Örneği: Mevcut Bir Dosyayı Açma**

Aşağıdaki örnek, "Sample.vsdx" adlı mevcut bir Microsoft Visio şablon dosyasını açar, "Hello World!" girer. metni ilk sayfaya kaydeder ve diagram'i kaydeder.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-ReadVisioDiagram-ReadVisioDiagram.java" >}}
