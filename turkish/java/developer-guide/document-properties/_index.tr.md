---
title: Belge Özelliklerini Yönet
linktitle: Döküman özellikleri
type: docs
weight: 80
url: /tr/java/document-properties/
aliases: [/java/document-properties/]
description: visio dosyalarının belge özelliklerini yönetin.
---
## **giriiş**

Microsoft Visio, visio dosyalarına özellik ekleme olanağı sağlar. Bu belge özellikleri yararlı bilgiler sağlar ve aşağıda ayrıntıları verildiği gibi 2 kategoriye ayrılır.

- Sistem tanımlı (yerleşik) özellikler: Yerleşik özellikler, belge başlığı, yazar adı, belge istatistikleri vb. gibi belge hakkında genel bilgiler içerir.
- Kullanıcı tanımlı (özel) özellikler: Son kullanıcı tarafından ad-değer çifti şeklinde tanımlanan özel özellikler.

{{% alert color="primary" %}}

Yerleşik ve özel özellikler hakkında bilinmesi gereken en önemli nokta, yerleşik özelliklere erişilip değiştirilebileceği, ancak oluşturulamayacağı veya kaldırılamayacağıdır. Ancak, özel özellikler oluşturulabilir ve yönetilebilir.

{{% /alert %}}

## **Microsoft Visio'i Kullanarak Belge Özelliklerini Yönetme**

 Microsoft Visio, Visio dosyalarının belge özelliklerini WYSIWYG tarzında yönetmenizi sağlar. açmak için lütfen aşağıdaki adımları izleyin.**Özellikleri** Visio 2016'daki iletişim kutusu.

1.  itibaren**Dosya** menü, seç**Bilgi**.

|**Bilgi Menüsünün Seçilmesi**|
|:- |
|![yapılacaklar:resim_alternatif_Metin](managing-document-properties_1.png)|
1.  Tıklamak**Özellikleri** başlığını açın ve "Gelişmiş Özellikler"i seçin.

|**Gelişmiş Özellikler Seçimine Tıklama**|
|:- |
|![yapılacaklar:resim_alternatif_Metin](managing-document-properties_2.png)|
1. Dosyanın belge özelliklerini yönetin.

|**Özellikler İletişim Kutusu**|
|:- |
|![yapılacaklar:resim_alternatif_Metin](managing-document-properties_3.png)|
Özellikler iletişim kutusunda Genel, Özet, İstatistikler, İçerik ve Gümrük gibi farklı sekmeler bulunur. Her sekme, dosyayla ilgili farklı türden bilgilerin yapılandırılmasına yardımcı olur. Özel sekmesi, özel özellikleri yönetmek için kullanılır.

## **Aspose.Diagram Kullanarak Belge Özellikleriyle Çalışma**

Geliştiriciler, Aspose.Diagram API'lerini kullanarak belge özelliklerini dinamik olarak yönetebilir. Bu özellik geliştiricilerin, dosyanın ne zaman alındığı, işlendiği, zaman damgası eklendiği vb. yararlı bilgileri dosyayla birlikte depolamasına yardımcı olur.

{{% alert color="primary" %}}

Aspose.Diagram for Java, API ve Sürüm Numarası ile ilgili bilgileri doğrudan çıktı belgelerine yazar.

Lütfen Aspose.Diagram for Java'e bu bilgileri çıktı Belgelerinden değiştirme veya kaldırma talimatı veremeyeceğinizi unutmayın.

{{% /alert %}}

### **Belge Özelliklerine Erişme**

 Aspose.Diagram API'ler, yerleşik ve özel olmak üzere her iki belge özelliği türünü de destekler. Aspose.Diagram'[**Diagram**](https://reference.aspose.com/diagram/java/com.aspose.diagram/Diagram) class bir Visio dosyasını temsil eder ve bir visio dosyası gibi[**Diagram**](https://reference.aspose.com/diagram/java/com.aspose.diagram/Diagram) sınıf, her biri tarafından temsil edilen birden çok sayfa içerebilir.[**Sayfa**](https://reference.aspose.com/diagram/java/com.aspose.diagram/page) sınıf oysa sayfaların koleksiyonu şu şekilde temsil edilir:[**Sayfa Koleksiyonu**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pagecollection)sınıf.

 Kullan[**Diagram**](https://reference.aspose.com/diagram/java/com.aspose.diagram/Diagram)Dosyanın belge özelliklerine aşağıda açıklandığı gibi erişmek için.

- Yerleşik belge özelliklerine erişmek için şunu kullanın:[**diagram.DocumentProps**](https://reference.aspose.com/diagram/java/com.aspose.diagram/documentproperties).
-  Özel belge özelliklerine erişmek için şunu kullanın:[**diagram.DocumentProps.CustomProps**](https://reference.aspose.com/diagram/java/com.aspose.diagram/CustomPropCollection).

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Introduction-DetectFormatfromInputStream-DetectFormatfromInputStream.java" >}}

### **Özel Belge Özellikleri Ekleme veya Kaldırma**

Bu konunun başında daha önce açıkladığımız gibi, geliştiriciler yerleşik özellikler ekleyemez veya kaldıramaz çünkü bu özellikler sistem tanımlıdır, ancak kullanıcı tanımlı oldukları için özel özellikler eklemek veya kaldırmak mümkündür.

### **Özel Özellikler Ekleme**

 Aspose.Diagram API'ler şu bilgileri açığa çıkardı:[**Ekle**](https://reference.aspose.com/diagram/java/com.aspose.diagram/custompropcollection#add(com.aspose.diagram.CustomProp) ) yöntemi[**Özel Prop Koleksiyonu**](https://reference.aspose.com/diagram/java/com.aspose.diagram/custompropcollection)koleksiyona özel özellikler eklemek için sınıf.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Introduction-DetectFormatfromInputStream-DetectFormatfromInputStream.java" >}}

### **Özel Özellikleri Kaldırma**

 Aspose.Diagram'i kullanarak özel özellikleri kaldırmak için[**CustomPropCollection.Kaldır**](https://reference.aspose.com/diagram/java/com.aspose.diagram/custompropcollection#remove(com.aspose.diagram.CustomProp)) yöntemi ve kaldırılacak belge özelliğinin adını iletin.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Introduction-DetectFormatfromInputStream-DetectFormatfromInputStream.java" >}}
