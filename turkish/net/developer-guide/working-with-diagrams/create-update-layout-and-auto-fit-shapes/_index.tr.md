---
title: Şekilleri Oluşturun, Güncelleyin, Düzenleyin ve Otomatik Sığdırın
type: docs
weight: 10
url: /tr/net/create-update-layout-and-auto-fit-shapes/
description: C# Diagram API'i, uygulamalarınızda C#'i kullanarak Visio dosyalarında şekiller oluşturmak, güncellemek ve otomatik mizanpaj oluşturmak için kullanın. C# kod örnekleriyle eksiksiz kılavuz.
---
## **Diagram oluşturma**
 Aspose.Diagram for .NET, Microsoft Office Otomasyon olmadan kendi uygulamalarınız içinden Microsoft Visio diyagramlarını okumanızı ve oluşturmanızı sağlar. Yeni belgeler oluştururken ilk adım, bir diagram oluşturmaktır. Ardından[şekiller ve bağlayıcılar ekleyin](https://docs.aspose.com/diagram/net/add-retrieve-copy-and-read-visio-shape-data/)diagram'i oluşturmak için.[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) yeni bir diagram oluşturmak için sınıf.
### **Programlama Örneği**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Diagrams-CreateDiagram-CreateDiagram.cs" >}}
## **Akış Şeması Stilinde Yerleşim Şekilleri**
 Akış şemaları ve ağ şemaları gibi belirli bağlantılı çizimlerle,**Düzen Şekilleri** şekilleri otomatik olarak konumlandırma özelliği. Otomatik olarak konumlandırma, her şekli manuel olarak yeni bir konuma sürüklemekten daha hızlıdır.

Örneğin, yeni bir süreci dahil etmek için büyük bir akış şemasını güncelliyorsanız, süreci oluşturan şekilleri ekleyip bağlayabilir ve ardından güncellenen çizimin mizanpajını otomatik olarak düzenlemek için mizanpaj özelliğini kullanabilirsiniz.

 Tarafından sunulan Düzen yöntemi[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) class, diagram'in tüm sayfalarında şekilleri düzenler ve/veya bağlayıcıları yeniden yönlendirir. Bu yöntem bir[Düzen Seçenekleri](https://reference.aspose.com/diagram/net/aspose.diagram.autolayout/layoutoptions)argüman olarak nesne. Şekilleri otomatik olarak düzenlemek için LayoutOptions sınıfı tarafından sunulan farklı özellikleri kullanın.

Aşağıdaki resim, otomatik düzen uygulanmadan önce bu makaledeki kod parçacıkları tarafından yüklenen diagram'i göstermektedir. Kod parçacıkları nasıl uygulanacağını gösterir[akış şeması düzenleri](https://docs.aspose.com/diagram/net/create-update-layout-and-auto-fit-shapes/) ve[kompakt ağaç düzenleri](https://docs.aspose.com/diagram/net/create-update-layout-and-auto-fit-shapes/).

**Kaynak diagram.**

![yapılacaklar:resim_alternatif_Metin](create-update-layout-and-auto-fit-shapes_1.png)

Bu makaledeki kod parçacıkları, diagram kaynağını alır ve her birini ayrı bir dosyaya kaydederek ona birkaç otomatik düzen türü uygular.

|<p>**Düzen aşağıdan yukarıya şekillenir** </p><p>![yapılacaklar:resim_alternatif_Metin](create-update-layout-and-auto-fit-shapes_2.png)</p>|<p>**Yerleşim şekilleri yukarıdan aşağıya** </p><p>![yapılacaklar:resim_alternatif_Metin](create-update-layout-and-auto-fit-shapes_3.png)</p>|
|:- |:- |
|<p>**Düzen şekilleri soldan sağa** </p><p>![yapılacaklar:resim_alternatif_Metin](create-update-layout-and-auto-fit-shapes_4.png)</p>|<p>**Düzen şekilleri sağdan sola** </p><p>![yapılacaklar:resim_alternatif_Metin](create-update-layout-and-auto-fit-shapes_5.png)</p>|
Şekilleri akış şeması stilinde düzenlemek için:

1. Diagram sınıfının bir örneğini oluşturun.
1. LayoutOptions sınıfının bir örneğini oluşturun ve Flowchart stiliyle ilgili özellikleri ayarlayın.
1. LayoutOptions'ı geçirerek Diagram sınıfının Layout yöntemini çağırın.
1. Visio çizimini yazmak için Diagram sınıfının Save yöntemini çağırın.
### **Akış Şeması Stili Programlama Örneği**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Diagrams-LayOutShapesInFlowchartStyle-LayOutShapesInFlowchartStyle.cs" >}}
### **Şekilleri Kompakt Ağaç Stilinde Yerleştirme**
 Kompakt ağaç düzeni stili, bir ağaç yapısı oluşturmaya çalışır. ile aynı girdi dosyasını kullanır.[yukarıdaki örnek](https://docs.aspose.com/diagram/net/create-update-layout-and-auto-fit-shapes/)ve birkaç farklı kompakt ağaç stiline kaydeder.

|<p>**Kompakt ağaç düzeni - aşağı ve sağ** </p><p>![yapılacaklar:resim_alternatif_Metin](create-update-layout-and-auto-fit-shapes_6.png)</p>|
|:- |
|<p>**Kompakt ağaç düzeni - aşağı ve sola** </p><p>![yapılacaklar:resim_alternatif_Metin](create-update-layout-and-auto-fit-shapes_7.png)</p>|


|<p>**Kompakt ağaç düzeni - sağa ve aşağıya** </p><p>![yapılacaklar:resim_alternatif_Metin](create-update-layout-and-auto-fit-shapes_8.png)</p>|<p>**Kompakt ağaç düzeni - sol ve aşağı** </p><p>![yapılacaklar:resim_alternatif_Metin](create-update-layout-and-auto-fit-shapes_9.png)</p>|
|:- |:- |
Şekilleri kompakt ağaç stilinde düzenlemek için:

1.  örneğini oluşturun[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) sınıf.
1. LayoutOptions sınıfının bir örneğini oluşturun ve kompakt ağaç stili özelliklerini ayarlayın.
1. LayoutOptions'ı geçirerek Diagram sınıfının Layout yöntemini çağırın.
1. Visio dosyasını yazmak için Diagram sınıfının Save yöntemini çağırın.
#### **Kompakt Ağaç Stili Programlama Örneği**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Diagrams-LayOutShapesInCompactTreeStyle-LayOutShapesInCompactTreeStyle.cs" >}}
## **Visio Diagram'i otomatik sığdır**
 Aspose.Diagram API, Visio çiziminin otomatik sığdırılmasını destekler. Bu özellik işlemi, dış şekilleri Visio sayfa sınırının içine getirmeye yardımcı olur. Aspose.Diagram for .NET API var[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) Visio çizimini temsil eden sınıf. bu[DiyagramKaydetmeSeçenekleri](https://reference.aspose.com/diagram/net/aspose.diagram.saving/diagramsaveoptions) class, Visio çizimine otomatik sığdırmak için AutoFitPageToDrawingContent özelliğini gösterir.

Bu örnek şu şekilde çalışır:

1. Diagram sınıfından bir nesne oluşturun.
1. DiagramSaveOptions sınıfından bir nesne oluşturun ve ortaya çıkan dosya biçimini iletin.
1. DiagramSaveOptions nesnesinin AutoFitPageToDrawingContent özelliğini ayarlayın.
1. Diagram sınıf nesnesinin Kaydetme yöntemini çağırın ve ayrıca tam dosya yolunu ve DiagramSaveOptions nesnesini iletin.
### **Otomatik Sığdırma Programlama Örneği**
Aşağıdaki örnek kod, Visio diagram'de şekillerin nasıl otomatik sığdırılacağını gösterir.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Diagrams-AutoFitShapesInVisio-AutoFitShapesInVisio.cs" >}}
## **VBA Project ile Çalışmak**
### **Visio Diagram'de VBA Modül Kodunu Değiştirin**
 Bu makale, Aspose.Diagram for .NET kullanılarak bir VBA modül kodunun otomatik olarak nasıl değiştirileceğini gösterir.[Vba Modülü](http://www.aspose.com/api/net/diagram/aspose.diagram.vba/VbaModule), [VbaModül Koleksiyonu](http://www.aspose.com/api/net/diagram/aspose.diagram.vba/VbaModuleCollection), [Vba Projesi](http://www.aspose.com/api/net/diagram/aspose.diagram.vba/VbaProject), [VbaProje Referansı](http://www.aspose.com/api/net/diagram/aspose.diagram.vba/VbaProjectReference) ve[VbaProjectReferenceCollection](http://www.aspose.com/api/net/diagram/aspose.diagram.vba/VbaProjectReferenceCollection) sınıflar. Bu sınıflar, VBA projesi üzerinde kontrol sahibi olmanıza yardımcı olur. Geliştiriciler, VBA modül kodunu çıkarabilir ve değiştirebilir.
### **VBA Modülü Kod Programlama Örneği Değiştirin**
Lütfen bu kod örneğini kontrol edin:

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Diagrams-ModifyVBAModule-ModifyVBAModule.cs" >}}
### **Visio Diagram'den Tüm Makroları Kaldır**
 Aspose.Diagram for .NET, geliştiricilerin Visio diagram'den tüm makroları kaldırmasına olanak tanır.[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) sınıfı, Visio çiziminden tüm makroları kaldırmanıza olanak tanır.
### **Tüm Makroları Kaldır Programlama Örneği**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Diagrams-RemoveMacrosFromVisio-RemoveMacrosFromVisio.cs" >}}
## **VSTO ile Yeni Diagram Oluşturma**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/)geliştiricilerin Microsoft Office Visio diyagramları oluşturup bunlarla çalışmasına ve yazılım uygulamalarına özellikler eklemesine olanak tanır. Visio dosyalarıyla çalışmanın başka yolları da vardır, en yaygını Microsoft Otomasyon'dur. Ne yazık ki, bunun bazı sınırlamaları var. Aspose.Diagram güçlü ve hızlıdır ve Microsoft Office kurulumu olmadan bağımsız çalışır.

 Bu geçiş makalesi, öncelikle nasıl kullanılacağını gösterir[VSTO](https://docs.aspose.com/diagram/net/create-update-layout-and-auto-fit-shapes/) ve daha sonra[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) yeni bir diagram oluşturmak ve ona bazı şekiller eklemek için. Aspose.Diagram kodunun VSTO kodundan daha kısa olduğunu fark edeceksiniz. Kodu kendi gelişiminiz için bir temel olarak kullanmaktan çekinmeyin ve ihtiyaçlarınızı karşılayacak şekilde geliştirin. VSTO, Microsoft Visio dosyalarıyla programlama yapmanızı sağlar. Yeni bir diagram oluşturmak için:

1. Bir Visio uygulama nesnesi oluşturun.
1. Uygulama nesnesini görünmez yapın.
1. Boş bir diagram oluşturun.
1. Visio kalıptan (şablon) şekiller ekleyin.
1. Dosyayı VDX olarak kaydedin.
### **VSTO Programlama Örneği ile Yeni Diagram Oluşturun**
{{% alert color="primary" %}}

Visio = Microsoft.Office.Interop.Visio kullanarak;
İthalatlar Visio = Microsoft.Office.Interop.Visio

{{% /alert %}}


**Örnek:**

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Knowledge-Base-CreatingDiagramWithVSTO-CreatingDiagramWithVSTO.cs" >}}
## **Aspose.Diagram for .NET ile Yeni Diagram Oluşturma**
Aspose.Diagram API kullanarak geliştiriciler makinede Microsoft Office Visio kurulumuna ihtiyaç duymazlar ve Microsoft Office Otomasyondan bağımsız çalışabilirler.

Yeni bir diagram oluşturmak için:

1. Boş bir diagram oluşturun.
1. Visio kalıptan (şablon) şekiller ekleyin.
1. Dosyayı VDX olarak kaydedin.
### **Yeni Diagram ile Aspose.Diagram for .NET Programlama Örneği**
{{% alert color="primary" %}}

Aspose.Diagram kullanarak;
İthal Aspose.Diagram

{{% /alert %}}

Örnek:

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Knowledge-Base-CreatingDiagramWithAspose-CreatingDiagramWithAspose.cs" >}}
## **Şekil Özelliklerini Güncelle**
 Microsoft Visio diyagramlarıyla çalışırken, kullanıcılar metin, stil, konum, yükseklik ve genişlik gibi şekil özelliklerini güncelleyebilir. Visio dosyalarıyla çalışan bir yazılım geliştiricisi olarak, bunu programlı olarak yapmanız istenecektir. İyi haber şu ki, Microsoft'in sağladığı Visio dosyalarıyla programlama mekanizmaları, VSTO kullanılarak veya[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/).

 Aşağıdaki konu nasıl kullanılacağını gösterir[VSTO](https://products.aspose.com/diagram/net/) ve[Aspose.Diagram](https://products.aspose.com/diagram/net/) şekil özelliklerini güncellemek için. Aşağıdaki kod parçacıkları, VSTO ve Aspose.Diagram for .NET için şekil özelliklerinin nasıl güncelleneceğini gösterir. Kodu kullanmaktan ve kendi özel durumunuza uygulamaktan çekinmeyin.
### **Şekil Özelliklerini VSTO ile Güncelleme**
VSTO, Microsoft Visio dosyalarıyla programlama yapmanızı sağlar. Şekil özelliklerini güncellemek için:

1. Bir Visio uygulama nesnesi oluşturun.
1. Uygulama nesnesini görünmez yapın.
1. Mevcut bir Visio VSD dosyasını açın.
1. Gerekli şekli bulun.
1. Şekil özelliklerini (metin, metin stili, konum ve boyut) güncelleyin.
1. Dosyayı VDX olarak kaydedin.
#### **VSTO Programlama Örneği ile Şekil Özelliklerini Güncelleme**
{{% alert color="primary" %}}

Visio = Microsoft.Office.Interop.Visio kullanarak;
İthalatlar Visio = Microsoft.Office.Interop.Visio

{{% /alert %}}

**Örnek:**

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Knowledge-Base-UpdateShapePropsWithVSTO-UpdateShapePropsWithVSTO.cs" >}}
### **Aspose.Diagram for .NET ile Şekil Özelliklerini Güncelleme**
Aspose.Diagram API kullanarak geliştiriciler makinede Microsoft Office Visio'e ihtiyaç duymazlar ve Microsoft Office Otomasyondan bağımsız çalışabilirler.

Aspose.Diagram for .NET ile şekil özelliklerini güncellemek için:

1. Mevcut bir Visio VSD dosyasını açın.
1. Gerekli şekli bulun.
1. Şekil özelliklerini (metin, metin stili, konum ve boyut) güncelleyin.
1. Dosyayı VDX olarak kaydedin.
#### **Aspose.Diagram for .NET Programlama Örneği ile Şekil Özelliklerini Güncelleme**
{{% alert color="primary" %}}

Aspose.Diagram kullanarak;
İthal Aspose.Diagram

{{% /alert %}}

**Örnek:**

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Knowledge-Base-UpdateShapePropsWithAspose-UpdateShapePropsWithAspose.cs" >}}
