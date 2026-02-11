---
title: Pencere Elemanlarıyla Çalışmak
type: docs
weight: 100
url: /tr/net/working-with-window-elements/
description: Bu bölümde, visio ile Aspose.Diagram'deki pencere öğelerinin alma özelliği açıklanmaktadır.
---
## **Visio Çiziminden Pencere Elemanlarını Alın**
 Ana Visio uygulama penceresi, herhangi bir açık Visio dosyasını içerebilir, tıpkı modern web tarayıcılarının bir pencerede birden çok sekmeli web sayfasına izin vermesi gibi. Geliştiriciler, Windows nesnelerini aşağıdakileri kullanarak alabilir:[Aspose.Diagram for .NET API](https://products.aspose.com/diagram/net/).

 bu[Pencere Koleksiyonu](http://www.aspose.com/api/net/diagram/aspose.diagram/windowcollection) nesne bir listesini temsil eder[pencere](http://www.aspose.com/api/net/diagram/aspose.diagram/window)çizimde mevcut nesneler. Diagram sınıfı tarafından sunulan Windows özelliği, Aspose.Diagram.Window nesnelerinin bir koleksiyonunu destekler. Bu özellik, Pencere kimliği, türü, yüksekliği, genişliği ve durumu olan pencere bilgilerini almak için kullanılabilir.
### **Pencere Elemanları Programlama Örneği Al**
```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_WindowElements();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Iterate through the window elements
foreach (Window window in diagram.Windows)
{
    Console.WriteLine("ID: " + window.ID);
    Console.WriteLine("Type: " + window.WindowType);
    Console.WriteLine("Window height: " + window.WindowHeight);
    Console.WriteLine("Window width: " + window.WindowWidth);
    Console.WriteLine("Window state: " + window.WindowState);
}

{{< /highlight >}}
```
## **Visio Diagram'e Pencere Elemanı Ekleyin**
 Ana Visio uygulama penceresi, herhangi bir açık Visio dosyasını içerebilir, tıpkı modern web tarayıcılarının bir pencerede birden çok sekmeli web sayfasına izin vermesi gibi. Geliştiriciler artık kullanarak bir Microsoft Visio örneğine yeni bir Window nesnesi ekleyebilir.[Aspose.Diagram for .NET API](https://products.aspose.com/diagram/net/).

 bu[pencere](http://www.aspose.com/api/net/diagram/aspose.diagram/window) nesne, bir Microsoft Visio örneğinde açık bir pencereyi temsil eder. bu[Ekle](http://www.aspose.com/api/net/diagram/aspose.diagram/windowcollection/methods/add) tarafından ortaya çıkarılan yöntem,[Pencere Koleksiyonu](http://www.aspose.com/api/net/diagram/aspose.diagram/windowcollection) class, yeni bir Window nesnesi eklemeye izin verir.
### **Pencere Elemanı Programlama Örneği Ekleme**
```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_WindowElements();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Initialize window object
Window window = new Window();
// Set window state
window.WindowState = WindowStateValue.Maximized;
// Set window height
window.WindowHeight = 500;
// Set window width
window.WindowWidth = 500;
// Set window type
window.WindowType = WindowTypeValue.Stencil;
// Add window object
diagram.Windows.Add(window);

// Save in any supported format
diagram.Save(dataDir + "AddWindowElementInVisio_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Dinamik Izgaralar ve Bağlantı Noktaları Desteği Ekleyin**
Dinamik ızgara, çizime zaten yerleştirdiğiniz şekillere göre yeni şekilleri dikey ve yatay olarak konumlandırmanıza yardımcı olur. Bağlantı noktaları ile ilgili olarak, işaretli olarak işaretlendikten sonra, onlara bağlanırken bağlantı noktalarını görmemize yardımcı olacaktır. kullanarak her iki seçeneği de elde edebiliriz.[Aspose.Diagram for .NET API](https://products.aspose.com/diagram/net/).
### **Visio Teknik Resimlerinde Dinamik Izgaralar ve Bağlantı Noktaları Desteği**
 bu[pencere](http://www.aspose.com/api/net/diagram/aspose.diagram/window) class, DynamicGridEnabled ve ShowConnectionPoints özelliklerini sunar. Bu özellikler, dinamik ızgaraları desteklemek ve bağlantı noktaları seçeneklerini göstermek için ayarları uygulamak için kullanılabilir.
#### **Destek Programlama Örneği Ekle**
```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_WindowElements();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get window object by index
Window window = diagram.Windows[0];
// Check dynamic grid option
window.DynamicGridEnabled = BOOL.True;
// Check connection points option
window.ShowConnectionPoints = BOOL.True;
            
// Save visio drawing
diagram.Save(dataDir + "AddSupportOfVisualAids_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Visio Diagram'in Izgaralarını, Cetvellerini, Kılavuzlarını ve Sayfa Sonlarını Gösterme ve Gizleme**
 Microsoft Office Visio'de bir çift cetvel, bir ızgara ve iki tür kılavuz ve her sayfada ne yazdırılacağını görmek için sayfa sonu bayrağı bulunur. Geliştiriciler bu ayarları kullanarak uygulayabilir[Aspose.Diagram for .NET API](https://products.aspose.com/diagram/net/)Ayarlar genel olarak tek bir sayfaya uygulanır.

 bu[pencere](http://www.aspose.com/api/net/diagram/aspose.diagram/window)class, ShowGrid, ShowGuides, ShowRulers ve ShowPageBreaks özelliklerini sunar. Bu özellikler ızgaraları, kılavuzları, cetvelleri ve sayfa sonlarını göstermek ve gizlemek için ayarları uygulamak için kullanılabilir.
### **Programlama Örneği**
```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_WindowElements();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get window object by index
Window window = diagram.Windows[0];
// Set visibility of grid
window.ShowGrid = BOOL.True;
// Set visibility of guides
window.ShowGuides = BOOL.True;
// Set visibility of rulers
window.ShowRulers = BOOL.True;
// Set visibility of page breaks
window.ShowPageBreaks = BOOL.True;

// Save diagram
diagram.Save(dataDir + "DisplayGridsRulersGuidesAndPageBreaks_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
