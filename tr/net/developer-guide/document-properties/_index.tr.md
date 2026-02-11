---
title: Belge Özelliklerini Yönet
linktitle: Döküman özellikleri
type: docs
weight: 80
url: /tr/net/document-properties/
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

Aspose.Diagram for .NET, API ve Sürüm Numarası ile ilgili bilgileri doğrudan çıktı belgelerine yazar.

Lütfen Aspose.Diagram for .NET'e bu bilgileri çıktı Belgelerinden değiştirme veya kaldırma talimatı veremeyeceğinizi unutmayın.

{{% /alert %}}

### **Belge Özelliklerine Erişme**

 Aspose.Diagram API'ler, yerleşik ve özel olmak üzere her iki belge özelliği türünü de destekler. Aspose.Diagram'[**Diagram**](https://reference.aspose.com/diagram/net/aspose.diagram/Diagram) class bir Visio dosyasını temsil eder ve bir visio dosyası gibi[**Diagram**](https://reference.aspose.com/diagram/net/aspose.diagram/Diagram) sınıf, her biri tarafından temsil edilen birden çok sayfa içerebilir.[**Sayfa**](https://reference.aspose.com/diagram/net/aspose.diagram/page) sınıf oysa sayfaların koleksiyonu şu şekilde temsil edilir:[**Sayfa Koleksiyonu**](https://reference.aspose.com/diagram/net/aspose.diagram/pagecollection)sınıf.

 Kullan[**Diagram**](https://reference.aspose.com/diagram/net/aspose.diagram/Diagram)Dosyanın belge özelliklerine aşağıda açıklandığı gibi erişmek için.

- Yerleşik belge özelliklerine erişmek için şunu kullanın:[**diagram.DocumentProps**](https://reference.aspose.com/diagram/net/aspose.diagram/documentproperties).
-  Özel belge özelliklerine erişmek için şunu kullanın:[**diagram.DocumentProps.CustomProps**](https://reference.aspose.com/diagram/net/aspose.diagram/documentproperties/properties/customprops).


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load a Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

//// Display Visio version and document modification time at different stages 
Console.WriteLine("Visio Instance Version : " + diagram.Version);
Console.WriteLine("Full Build Number Created : " + diagram.DocumentProps.BuildNumberCreated);
Console.WriteLine("Full Build Number Edited : " + diagram.DocumentProps.BuildNumberEdited);
Console.WriteLine("Date Created : " + diagram.DocumentProps.TimeCreated);
Console.WriteLine("Date Last Edited : " + diagram.DocumentProps.TimeEdited);
Console.WriteLine("Date Last Printed : " + diagram.DocumentProps.TimePrinted);
Console.WriteLine("Date Last Saved : " + diagram.DocumentProps.TimeSaved);
Console.WriteLine("CustomProps Length " + diagram.DocumentProps.CustomProps.Count);

{{< /highlight >}}


### **Özel Belge Özellikleri Ekleme veya Kaldırma**

Bu konunun başında daha önce açıkladığımız gibi, geliştiriciler yerleşik özellikler ekleyemez veya kaldıramaz çünkü bu özellikler sistem tanımlıdır, ancak kullanıcı tanımlı oldukları için özel özellikler eklemek veya kaldırmak mümkündür.

### **Özel Özellikler Ekleme**

 Aspose.Diagram API'ler şu bilgileri açığa çıkardı:[**Ekle**](https://reference.aspose.com/diagram/net/aspose.diagram/custompropcollection/methods/add) için yöntem[**Özel Prop Koleksiyonu**](https://reference.aspose.com/diagram/net/aspose.diagram/custompropcollection)koleksiyona özel özellikler eklemek için sınıf.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load a Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

//// Get CustomProperties of diagram
Aspose.Diagram.CustomPropCollection customProperties = diagram.DocumentProps.CustomProps;
//Set property of CustomProp
Aspose.Diagram.CustomProp customProp = new Aspose.Diagram.CustomProp();
customProp.PropType = Aspose.Diagram.PropType.String;
customProp.CustomValue.ValueString = "Test";
//Add CustomProp to Collection
customProperties.Add(customProp);

{{< /highlight >}}


### **Özel Özellikleri Kaldırma**

 Aspose.Diagram'i kullanarak özel özellikleri kaldırmak için[**CustomPropCollection.Kaldır**](https://reference.aspose.com/diagram/net/aspose.diagram/custompropcollection/methods/remove)yöntemini seçin ve kaldırılacak belge özelliğinin adını iletin.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Diagrams-RemovingCustomProperties.cs" >}}
