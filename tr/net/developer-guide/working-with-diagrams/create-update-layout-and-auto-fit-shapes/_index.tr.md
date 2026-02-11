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

{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Diagrams();

// Create directory if it is not already present.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
    System.IO.Directory.CreateDirectory(dataDir);
// Initialize a new Visio
Diagram diagram = new Diagram();
dataDir = dataDir + "CreateDiagram_out.vsdx";
// Save in the VSDX format
diagram.Save(dataDir, SaveFileFormat.VSDX);

{{< /highlight >}}

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

{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Diagrams();

// Load an existing Visio diagram
string fileName = "LayOutShapesInFlowchartStyle.vdx";
Diagram diagram = new Diagram(dataDir + fileName);

// Set layout options 
LayoutOptions flowChartOptions = new LayoutOptions();
flowChartOptions.LayoutStyle = LayoutStyle.FlowChart;
flowChartOptions.SpaceShapes = 1f;
flowChartOptions.EnlargePage = true;

// Set layout direction as BottomToTop and then save
flowChartOptions.Direction = LayoutDirection.BottomToTop;
diagram.Layout(flowChartOptions);
diagram.Save(dataDir + "sample_btm_top_out.vdx", SaveFileFormat.VDX);

// Set layout direction as TopToBottom and then save
diagram = new Diagram(dataDir + fileName);
flowChartOptions.Direction = LayoutDirection.TopToBottom;
diagram.Layout(flowChartOptions);
diagram.Save(dataDir + "sample_top_btm_out.vdx", SaveFileFormat.VDX);

// Set layout direction as LeftToRight and then save
diagram = new Diagram(dataDir + fileName);
flowChartOptions.Direction = LayoutDirection.LeftToRight;
diagram.Layout(flowChartOptions);
diagram.Save(dataDir + "sample_left_right_out.vdx", SaveFileFormat.VDX);

// Set layout direction as RightToLeft and then save
diagram = new Diagram(dataDir + fileName);
flowChartOptions.Direction = LayoutDirection.RightToLeft;
diagram.Layout(flowChartOptions);
diagram.Save(dataDir + "sample_right_left_out.vdx", SaveFileFormat.VDX);

{{< /highlight >}}

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

{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Diagrams();

string fileName = "LayOutShapesInCompactTreeStyle.vdx";
// Load an existing Visio diagram
Diagram diagram = new Diagram(dataDir + fileName);

// Set layout options 
LayoutOptions compactTreeOptions = new LayoutOptions();
compactTreeOptions.LayoutStyle = LayoutStyle.CompactTree;
compactTreeOptions.EnlargePage = true;

// Set layout direction as DownThenRight and then save
compactTreeOptions.Direction = LayoutDirection.DownThenRight;
diagram.Layout(compactTreeOptions);
diagram.Save(dataDir + "sample_down_right.vdx", SaveFileFormat.VDX);

// Set layout direction as DownThenLeft and then save
diagram = new Diagram(dataDir + fileName);
compactTreeOptions.Direction = LayoutDirection.DownThenLeft;
diagram.Layout(compactTreeOptions);
diagram.Save(dataDir + "sample_down_left.vdx", SaveFileFormat.VDX);

// Set layout direction as RightThenDown and then save
diagram = new Diagram(dataDir + fileName);
compactTreeOptions.Direction = LayoutDirection.RightThenDown;
diagram.Layout(compactTreeOptions);
diagram.Save(dataDir + "sample_right_down.vdx", SaveFileFormat.VDX);

// Set layout direction as LeftThenDown and then save
diagram = new Diagram(dataDir + fileName);
compactTreeOptions.Direction = LayoutDirection.LeftThenDown;
diagram.Layout(compactTreeOptions);
diagram.Save(dataDir + "sample_left_down.vdx", SaveFileFormat.VDX);

{{< /highlight >}}

## **Visio Diagram'i otomatik sığdır**
 Aspose.Diagram API, Visio çiziminin otomatik sığdırılmasını destekler. Bu özellik işlemi, dış şekilleri Visio sayfa sınırının içine getirmeye yardımcı olur. Aspose.Diagram for .NET API var[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) Visio çizimini temsil eden sınıf. bu[DiyagramKaydetmeSeçenekleri](https://reference.aspose.com/diagram/net/aspose.diagram.saving/diagramsaveoptions) class, Visio çizimine otomatik sığdırmak için AutoFitPageToDrawingContent özelliğini gösterir.

Bu örnek şu şekilde çalışır:

1. Diagram sınıfından bir nesne oluşturun.
1. DiagramSaveOptions sınıfından bir nesne oluşturun ve ortaya çıkan dosya biçimini iletin.
1. DiagramSaveOptions nesnesinin AutoFitPageToDrawingContent özelliğini ayarlayın.
1. Diagram sınıf nesnesinin Kaydetme yöntemini çağırın ve ayrıca tam dosya yolunu ve DiagramSaveOptions nesnesini iletin.
### **Otomatik Sığdırma Programlama Örneği**
Aşağıdaki örnek kod, Visio diagram'de şekillerin nasıl otomatik sığdırılacağını gösterir.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Diagrams();

// Load a Visio diagram
Diagram diagram = new Diagram(dataDir + "BFlowcht.vsdx");

// Use saving options
DiagramSaveOptions options = new DiagramSaveOptions(SaveFileFormat.VSDX);
// Set Auto fit page property
options.AutoFitPageToDrawingContent = true;

// Save Visio diagram
diagram.Save(dataDir + "AutoFitShapesInVisio_out.vsdx", options);

{{< /highlight >}}

## **VBA Project ile Çalışmak**
### **Visio Diagram'de VBA Modül Kodunu Değiştirin**
 Bu makale, Aspose.Diagram for .NET kullanılarak bir VBA modül kodunun otomatik olarak nasıl değiştirileceğini gösterir.[Vba Modülü](http://www.aspose.com/api/net/diagram/aspose.diagram.vba/VbaModule), [VbaModül Koleksiyonu](http://www.aspose.com/api/net/diagram/aspose.diagram.vba/VbaModuleCollection), [Vba Projesi](http://www.aspose.com/api/net/diagram/aspose.diagram.vba/VbaProject), [VbaProje Referansı](http://www.aspose.com/api/net/diagram/aspose.diagram.vba/VbaProjectReference) ve[VbaProjectReferenceCollection](http://www.aspose.com/api/net/diagram/aspose.diagram.vba/VbaProjectReferenceCollection) sınıflar. Bu sınıflar, VBA projesi üzerinde kontrol sahibi olmanıza yardımcı olur. Geliştiriciler, VBA modül kodunu çıkarabilir ve değiştirebilir.
### **VBA Modülü Kod Programlama Örneği Değiştirin**
Lütfen bu kod örneğini kontrol edin:


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Diagrams();

// Load an existing Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdm", LoadFileFormat.VSDM);
// Extract VBA project
Aspose.Diagram.Vba.VbaProject v = diagram.VbaProject;
// Iterate through the modules and modify VBA module code
foreach (VbaModule module in diagram.VbaProject.Modules)
{
    string code = module.Codes;
    if (code.Contains("This is test message."))
        code = code.Replace("This is test message.", "This is Aspose.Diagram message.");
    module.Codes = code;
}
// Save the Visio diagram
diagram.Save(dataDir + "ModifyVBAModule_out.vssm", SaveFileFormat.VSSM);

{{< /highlight >}}

### **Visio Diagram'den Tüm Makroları Kaldır**
 Aspose.Diagram for .NET, geliştiricilerin Visio diagram'den tüm makroları kaldırmasına olanak tanır.[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) sınıfı, Visio çiziminden tüm makroları kaldırmanıza olanak tanır.
### **Tüm Makroları Kaldır Programlama Örneği**

{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Diagrams();

// Load a Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Remove all macros
diagram.VbProjectData = null;

// Save diagram
diagram.Save(dataDir + "RemoveMacrosFromVisio_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

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


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_KnowledgeBase();

Visio.Application vdxApp = null;
Visio.Document vdxDoc = null;
try
{
    // Create Visio Application Object
    vdxApp = new Visio.Application();

    // Make Visio Application Invisible
    vdxApp.Visible = false;

    // Create a new diagram
    vdxDoc = vdxApp.Documents.Add("");

    // Load Visio Stencil
    Visio.Documents visioDocs = vdxApp.Documents;
    Visio.Document visioStencil = visioDocs.OpenEx("Basic Shapes.vss",
        (short)Microsoft.Office.Interop.Visio.VisOpenSaveArgs.visOpenHidden);

    // Set active page
    Visio.Page visioPage = vdxApp.ActivePage;

    // Add a new rectangle shape
    Visio.Master visioRectMaster = visioStencil.Masters.get_ItemU(@"Rectangle");
    Visio.Shape visioRectShape = visioPage.Drop(visioRectMaster, 4.25, 5.5);
    visioRectShape.Text = @"Rectangle text.";

    // Add a new star shape
    Visio.Master visioStarMaster = visioStencil.Masters.get_ItemU(@"Star 7");
    Visio.Shape visioStarShape = visioPage.Drop(visioStarMaster, 2.0, 5.5);
    visioStarShape.Text = @"Star text.";

    // Add a new hexagon shape
    Visio.Master visioHexagonMaster = visioStencil.Masters.get_ItemU(@"Hexagon");
    Visio.Shape visioHexagonShape = visioPage.Drop(visioHexagonMaster, 7.0, 5.5);
    visioHexagonShape.Text = @"Hexagon text.";


    // Save diagram as VDX
    vdxDoc.SaveAs(dataDir + "CreatingDiagramWithVSTO_out.vdx");
}
catch (Exception ex)
{
    Console.WriteLine(ex.Message + "\nThis example will only work if you apply a valid Aspose License. You can purchase full license or get 30 day temporary license from http:// Www.aspose.com/purchase/default.aspx.");
}
            

{{< /highlight >}}

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


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_KnowledgeBase();

// Create a new diagram
Diagram diagram = new Diagram(dataDir + "Basic Shapes.vss");

// Add a new rectangle shape
long shapeId = diagram.AddShape(4.25, 5.5, 2, 1, @"Rectangle", 0);
Shape shape = diagram.Pages[0].Shapes.GetShape(shapeId);
shape.Text.Value.Add(new Txt(@"Rectangle text."));

// Add a new star shape
shapeId = diagram.AddShape(2.0, 5.5, 2, 2, @"Star 7", 0);
shape = diagram.Pages[0].Shapes.GetShape(shapeId);
shape.Text.Value.Add(new Txt(@"Star text."));

// Add a new hexagon shape
shapeId = diagram.AddShape(7.0, 5.5, 2, 2, @"Hexagon", 0);
shape = diagram.Pages[0].Shapes.GetShape(shapeId);
shape.Text.Value.Add(new Txt(@"Hexagon text."));

// Save the new diagram
diagram.Save(dataDir + "CreatingDiagramWithAspose_out.vdx", SaveFileFormat.VDX);

{{< /highlight >}}

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


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_KnowledgeBase();

Visio.Application vsdApp = null;
Visio.Document vsdDoc = null;
try
{
    // Create Visio Application Object
    vsdApp = new Visio.Application();

    // Make Visio Application Invisible
    vsdApp.Visible = false;

    // Create a document object and load a diagram
    vsdDoc = vsdApp.Documents.Open(dataDir + "Drawing1.vsd");

    // Create page object to get required page
    Visio.Page page = vsdApp.ActivePage;

    // Create shape object to get required shape
    Visio.Shape shape = page.Shapes["Process1"];

    // Set shape text and text style
    shape.Text = "Hello World";
    shape.TextStyle = "CustomStyle1";

    // Set shape's position
    shape.get_Cells("PinX").ResultIU = 5;
    shape.get_Cells("PinY").ResultIU = 5;

    // Set shape's height and width
    shape.get_Cells("Height").ResultIU = 2;
    shape.get_Cells("Width").ResultIU = 3;

    // Save file as VDX
    vsdDoc.SaveAs(dataDir + "Drawing1.vdx");
}
catch (Exception ex)
{
    Console.WriteLine(ex.Message + "\nThis example will only work if you apply a valid Aspose License. You can purchase full license or get 30 day temporary license from http:// Www.aspose.com/purchase/default.aspx.");
}           

{{< /highlight >}}

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


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
try
{
    // The path to the documents directory.
    string dataDir = RunExamples.GetDataDir_KnowledgeBase();

    // Save the uploaded file as PDF
    Diagram diagram = new Diagram(dataDir + "Drawing1.vsd");

    // Find a particular shape and update its properties
    foreach (Aspose.Diagram.Shape shape in diagram.Pages[0].Shapes)
    {
        if (shape.Name.ToLower() == "process1")
        {
            shape.Text.Value.Clear();
            shape.Text.Value.Add(new Txt("Hello World"));

            // Find custom style sheet and set as shape's text style
            foreach (StyleSheet styleSheet in diagram.StyleSheets)
            {
                if (styleSheet.Name == "CustomStyle1")
                {
                    shape.TextStyle = styleSheet;
                }
            }

            // Set horizontal and vertical position of the shape
            shape.XForm.PinX.Value = 5;
            shape.XForm.PinY.Value = 5;

            // Set height and width of the shape
            shape.XForm.Height.Value = 2;
            shape.XForm.Width.Value = 3;
        }
    }

    // Save shape as VDX
    diagram.Save(dataDir + "UpdateShapePropsWithAspose_out.vdx", SaveFileFormat.VDX);
}
catch (Exception ex)
{
    Console.WriteLine(ex.Message);
}

{{< /highlight >}}

