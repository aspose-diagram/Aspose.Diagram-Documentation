---
title: Şekilleri Oluşturun, Düzenleyin ve Otomatik Sığdırın
type: docs
weight: 10
url: /tr/java/create-layout-and-auto-fit-shapes/
---
## **Diagram oluşturma**
 Aspose.Diagram for Java, Microsoft Office Otomasyon olmadan kendi uygulamalarınız içinden Microsoft Visio diyagramlarını okumanızı ve oluşturmanızı sağlar. Yeni belgeler oluştururken ilk adım, bir diagram oluşturmaktır. Ardından[şekiller ve bağlayıcılar ekleyin](/diagram/tr/java/add-and-connect-visio-shapes/)diagram'i oluşturmak için.[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) yeni bir diagram oluşturmak için sınıf.
### **Programlama Örneği**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Diagrams-CreateDiagram-CreateDiagram.java" >}}
## **Akış Şeması Stilinde Yerleşim Şekilleri**
 Akış şemaları ve ağ şemaları gibi belirli bağlantılı çizimlerle,**Düzen Şekilleri** şekilleri otomatik olarak konumlandırma özelliği. Otomatik olarak konumlandırma, her şekli manuel olarak yeni bir konuma sürüklemekten daha hızlıdır.

Örneğin, yeni bir süreci dahil etmek için büyük bir akış şemasını güncelliyorsanız, süreci oluşturan şekilleri ekleyip bağlayabilir ve ardından güncellenen çizimin mizanpajını otomatik olarak düzenlemek için mizanpaj özelliğini kullanabilirsiniz.

 Tarafından sunulan Düzen yöntemi[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) class, diagram'in tüm sayfalarında şekilleri düzenler ve/veya bağlayıcıları yeniden yönlendirir. Bu yöntem, bir LayoutOptions nesnesini bağımsız değişken olarak kabul eder. Şekilleri otomatik olarak düzenlemek için LayoutOptions sınıfı tarafından sunulan farklı özellikleri kullanın.

Aşağıdaki resim, otomatik düzen uygulanmadan önce bu makaledeki kod parçacıkları tarafından yüklenen diagram'i göstermektedir. Kod parçacıkları nasıl uygulanacağını gösterir[akış şeması düzenleri](/diagram/tr/java/create-2c-layout-and-auto-fit-shapes/) ve[kompakt ağaç düzenleri](/diagram/tr/java/create-2c-layout-and-auto-fit-shapes/).

**Kaynak diagram.** 

![yapılacaklar:resim_alternatif_Metin](create-layout-and-auto-fit-shapes_1.png)

Bu makaledeki kod parçacıkları, diagram kaynağını alır ve her birini ayrı bir dosyaya kaydederek ona birkaç otomatik düzen türü uygular.

|<p>**Düzen aşağıdan yukarıya şekillenir** </p><p>![yapılacaklar:resim_alternatif_Metin](create-layout-and-auto-fit-shapes_2.png)</p>|<p>**Yerleşim şekilleri yukarıdan aşağıya** </p><p>![yapılacaklar:resim_alternatif_Metin](create-layout-and-auto-fit-shapes_3.png)</p>|
|:- |:- |
|<p>**Düzen şekilleri soldan sağa** </p><p>![yapılacaklar:resim_alternatif_Metin](create-layout-and-auto-fit-shapes_4.png)</p>|<p>**Düzen şekilleri sağdan sola** </p><p>![yapılacaklar:resim_alternatif_Metin](create-layout-and-auto-fit-shapes_5.png)</p>|
Şekilleri akış şeması stilinde düzenlemek için:

1. Diagram sınıfının bir örneğini oluşturun.
1. LayoutOptions sınıfının bir örneğini oluşturun ve Flowchart stiliyle ilgili özellikleri ayarlayın.
1. LayoutOptions'ı geçirerek Diagram sınıfının Layout yöntemini çağırın.
1. Visio çizimini yazmak için Diagram sınıfının Save yöntemini çağırın.
### **Akış Şeması Stili Programlama Örneği**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Diagrams-LayOutShapesInFlowchartStyle-LayOutShapesInFlowchartStyle.java" >}}
### **Şekilleri Kompakt Ağaç Stilinde Yerleştirme**
 Kompakt ağaç düzeni stili, bir ağaç yapısı oluşturmaya çalışır. ile aynı girdi dosyasını kullanır.[yukarıdaki örnek](/diagram/tr/java/create-2c-layout-and-auto-fit-shapes/)ve birkaç farklı kompakt ağaç stiline kaydeder.

|<p>**Kompakt ağaç düzeni - aşağı ve sağ** </p><p>![yapılacaklar:resim_alternatif_Metin](create-layout-and-auto-fit-shapes_6.png)</p>|
|:- |
|<p>**Kompakt ağaç düzeni - aşağı ve sola** </p><p>![yapılacaklar:resim_alternatif_Metin](create-layout-and-auto-fit-shapes_7.png)</p>|


|<p>**Kompakt ağaç düzeni - sağa ve aşağıya** </p><p>![yapılacaklar:resim_alternatif_Metin](create-layout-and-auto-fit-shapes_8.png)</p>|<p>**Kompakt ağaç düzeni - sol ve aşağı** </p><p>![yapılacaklar:resim_alternatif_Metin](create-layout-and-auto-fit-shapes_9.png)</p>|
|:- |:- |
Şekilleri kompakt ağaç stilinde düzenlemek için:

1.  örneğini oluşturun[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) sınıf.
1. LayoutOptions sınıfının bir örneğini oluşturun ve kompakt ağaç stili özelliklerini ayarlayın.
1. LayoutOptions'ı geçirerek Diagram sınıfının Layout yöntemini çağırın.
1. Visio dosyasını yazmak için Diagram sınıfının Save yöntemini çağırın.
#### **Kompakt Ağaç Stili Programlama Örneği**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Diagrams-LayOutShapesInCompactTreeStyle-LayOutShapesInCompactTreeStyle.java" >}}
## **Visio Diagram'i otomatik sığdır**
Aspose.Diagram API, Visio çiziminin otomatik sığdırılmasını destekler. Bu özellik işlemi, dış şekilleri Visio sayfa sınırının içine getirmeye yardımcı olur.

Aspose.Diagram for Java API, bir Visio çizimini temsil eden Diagram sınıfına sahiptir. DiagramSaveOptions sınıfı, Visio çizimine otomatik sığdırmak için AutoFitPageToDrawingContent özelliğini gösterir.

Bu örnek şu şekilde çalışır:

1. Diagram sınıfından bir nesne oluşturun.
1. DiagramSaveOptions sınıfından bir nesne oluşturun ve ortaya çıkan dosya biçimini iletin.
1. DiagramSaveOptions nesnesinin AutoFitPageToDrawingContent özelliğini ayarlayın.
1. Diagram sınıf nesnesinin Kaydetme yöntemini çağırın ve ayrıca tam dosya yolunu ve DiagramSaveOptions nesnesini iletin.
### **Otomatik Sığdırma Programlama Örneği**
Aşağıdaki örnek kod, Visio diagram'de şekillerin nasıl otomatik sığdırılacağını gösterir.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Diagrams-AutoFitShapesInVisio-AutoFitShapesInVisio.java" >}}
## **VBA Project ile Çalışmak**
### **Visio Diagram'de VBA Modül Kodunu Değiştirin**
Bu makale, Aspose.Diagram for Java kullanılarak bir VBA modülü kodunun otomatik olarak nasıl değiştirileceğini gösterir.

VbaModule, VbaModuleCollection, VbaProject, VbaProjectReference ve VbaProjectReferenceCollection sınıflarını ekledik. Bu sınıflar, VBA projesi üzerinde kontrol sahibi olmanıza yardımcı olur. Geliştiriciler, VBA modül kodunu çıkarabilir ve değiştirebilir.
### **VBA Modülü Kod Programlama Örneği Değiştirin**
Lütfen bu kod örneğini kontrol edin:

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Diagrams-ModifyVBAModuleCode-ModifyVBAModuleCode.java" >}}
### **Visio Diagram'den Tüm Makroları Kaldır**
Aspose.Diagram for Java, geliştiricilerin Visio diagram'deki tüm makroları kaldırmasına olanak tanır.

Tarafından sunulan JavaProjectData özelliği[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) sınıfı, Visio çiziminden tüm makroları kaldırmanıza olanak tanır.
### **Tüm Makroları Kaldır Programlama Örneği**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Diagrams-RemoveMacrosFromVisio-RemoveMacrosFromVisio.java" >}}
