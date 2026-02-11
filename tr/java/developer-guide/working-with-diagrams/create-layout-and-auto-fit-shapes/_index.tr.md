---
title: Şekilleri Oluşturun, Düzenleyin ve Otomatik Sığdırın
type: docs
weight: 10
url: /tr/java/create-layout-and-auto-fit-shapes/
---
## **Diagram oluşturma**
 Aspose.Diagram for Java, Microsoft Office Otomasyon olmadan kendi uygulamalarınız içinden Microsoft Visio diyagramlarını okumanızı ve oluşturmanızı sağlar. Yeni belgeler oluştururken ilk adım, bir diagram oluşturmaktır. Ardından[şekiller ve bağlayıcılar ekleyin](/diagram/tr/java/add-and-connect-visio-shapes/)diagram'i oluşturmak için.[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) yeni bir diagram oluşturmak için sınıf.
### **Programlama Örneği**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(CreateDiagram.class);
// Create directory if it is not already present.
File file = new File(dataDir);
if (!file.exists())
	file.mkdir();
// initialize a new Diagram
Diagram diagram = new Diagram();
// save in the VSDX format
diagram.save(dataDir + "CreateDiagram_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

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

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(LayOutShapesInFlowchartStyle.class);     

// load an existing Visio diagram
String fileName = "LayOutShapesInFlowchartStyle.vdx";
Diagram diagram = new Diagram(dataDir + fileName);

// set layout options 
LayoutOptions flowChartOptions = new LayoutOptions();
flowChartOptions.setLayoutStyle(LayoutStyle.FLOW_CHART);
flowChartOptions.setSpaceShapes(1f);
flowChartOptions.setEnlargePage(true);

// set layout direction as BottomToTop and then save
flowChartOptions.setDirection(LayoutDirection.BOTTOM_TO_TOP);
diagram.layout(flowChartOptions);
diagram.save(dataDir + "sample_btm_top.vdx", SaveFileFormat.VDX);

// set layout direction as TopToBottom and then save
diagram = new Diagram(dataDir + fileName);
flowChartOptions.setDirection(LayoutDirection.TOP_TO_BOTTOM);
diagram.layout(flowChartOptions);
diagram.save(dataDir + "sample_top_btm.vdx", SaveFileFormat.VDX);

// set layout direction as LeftToRight and then save
diagram = new Diagram(dataDir + fileName);
flowChartOptions.setDirection(LayoutDirection.LEFT_TO_RIGHT);
diagram.layout(flowChartOptions);
diagram.save(dataDir + "sample_left_right.vdx", SaveFileFormat.VDX);

// set layout direction as RightToLeft and then save
diagram = new Diagram(dataDir + fileName);
flowChartOptions.setDirection(LayoutDirection.RIGHT_TO_LEFT);
diagram.layout(flowChartOptions);
diagram.save(dataDir + "sample_right_left.vdx", SaveFileFormat.VDX);

{{< /highlight >}}

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

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(LayOutShapesInCompactTreeStyle.class);
        
String fileName = "LayOutShapesInCompactTreeStyle.vdx";
// load an existing Visio diagram
Diagram diagram = new Diagram(dataDir + fileName);

// set layout options 
LayoutOptions compactTreeOptions = new LayoutOptions();
compactTreeOptions.setLayoutStyle(LayoutStyle.COMPACT_TREE);
compactTreeOptions.setEnlargePage(true);

// set layout direction as DownThenRight and then save
compactTreeOptions.setDirection(LayoutDirection.DOWN_THEN_RIGHT);
diagram.layout(compactTreeOptions);
diagram.save(dataDir + "sample_down_right.vdx", SaveFileFormat.VDX);

// set layout direction as DownThenLeft and then save
diagram = new Diagram(dataDir + fileName);
compactTreeOptions.setDirection(LayoutDirection.DOWN_THEN_LEFT);
diagram.layout(compactTreeOptions);
diagram.save(dataDir + "sample_down_left.vdx", SaveFileFormat.VDX);

// set layout direction as RightThenDown and then save
diagram = new Diagram(dataDir + fileName);
compactTreeOptions.setDirection(LayoutDirection.RIGHT_THEN_DOWN);
diagram.layout(compactTreeOptions);
diagram.save(dataDir + "sample_right_down.vdx", SaveFileFormat.VDX);

// set layout direction as LeftThenDown and then save
diagram = new Diagram(dataDir + fileName);
compactTreeOptions.setDirection(LayoutDirection.LEFT_THEN_DOWN);
diagram.layout(compactTreeOptions);
diagram.save(dataDir + "sample_left_down.vdx", SaveFileFormat.VDX);

{{< /highlight >}}

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


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(AutoFitShapesInVisio.class);
// load a Visio diagram
Diagram diagram = new Diagram(dataDir + "BFlowcht.vsdx");

// use saving options
DiagramSaveOptions options = new DiagramSaveOptions(SaveFileFormat.VSDX);
// set Auto fit page property
options.setAutoFitPageToDrawingContent(true);

// save Visio diagram
diagram.save(dataDir + "AutoFitShapesInVisio_Out.vsdx", options);

{{< /highlight >}}

## **VBA Project ile Çalışmak**
### **Visio Diagram'de VBA Modül Kodunu Değiştirin**
Bu makale, Aspose.Diagram for Java kullanılarak bir VBA modülü kodunun otomatik olarak nasıl değiştirileceğini gösterir.

VbaModule, VbaModuleCollection, VbaProject, VbaProjectReference ve VbaProjectReferenceCollection sınıflarını ekledik. Bu sınıflar, VBA projesi üzerinde kontrol sahibi olmanıza yardımcı olur. Geliştiriciler, VBA modül kodunu çıkarabilir ve değiştirebilir.
### **VBA Modülü Kod Programlama Örneği Değiştirin**
Lütfen bu kod örneğini kontrol edin:


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// load an existing Visio diagram
String dataDir = Utils.getDataDir(ModifyVBAModuleCode.class);
InputStream input = new FileInputStream(dataDir + "macro.vsdm");
Diagram diagram = new Diagram(input);
// extract VBA project
VbaProject v = diagram.getVbaProject();
// Iterate through the modules and modify VBA macro code
for (int i = 0; i < diagram.getVbaProject().getModules().getCount(); i++) {
	VbaModule module = diagram.getVbaProject().getModules().get(i);
	String code = module.getCodes();
	if (code.contains("This is test message."))
		code = code.replace("This is test message.", "This is Aspose.Diagram message.");
	module.setCodes(code);
}
// save the Visio diagram
diagram.save(dataDir + "out.vssm", SaveFileFormat.VSSM);

{{< /highlight >}}

### **Visio Diagram'den Tüm Makroları Kaldır**
Aspose.Diagram for Java, geliştiricilerin Visio diagram'deki tüm makroları kaldırmasına olanak tanır.

Tarafından sunulan JavaProjectData özelliği[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) sınıfı, Visio çiziminden tüm makroları kaldırmanıza olanak tanır.
### **Tüm Makroları Kaldır Programlama Örneği**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(RemoveMacrosFromVisio.class);  
// load a Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// remove all macros
diagram.setVbProjectData(null);

// Save diagram
diagram.save(dataDir + "RemoveMacrosFromVisio_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

