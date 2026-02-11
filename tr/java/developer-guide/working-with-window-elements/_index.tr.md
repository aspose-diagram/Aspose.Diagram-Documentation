---
title: Pencere Elemanlarıyla Çalışmak
type: docs
weight: 130
url: /tr/java/working-with-window-elements/
---
## **Visio Çiziminden Pencere Elemanlarını Alın**
 Ana Visio uygulama penceresi, herhangi bir açık Visio dosyasını içerebilir, tıpkı modern web tarayıcılarının bir pencerede birden çok sekmeli web sayfasına izin vermesi gibi. Geliştiriciler, Windows nesnelerini aşağıdakileri kullanarak alabilir:[Aspose.Diagram for Java API](https://products.aspose.com/diagram/java/).

 bu[Pencere Koleksiyonu](https://reference.aspose.com/diagram/java/com.aspose.diagram/windowcollection) nesne bir listesini temsil eder[pencere](https://reference.aspose.com/diagram/java/com.aspose.diagram/window)çizimde mevcut nesneler. Diagram sınıfı tarafından sunulan Windows özelliği, Aspose.Diagram.Window nesnelerinin bir koleksiyonunu destekler. Bu özellik, Pencere kimliği, türü, yüksekliği, genişliği ve durumu olan pencere bilgilerini almak için kullanılabilir.

**Kodun çıktısını gösteren bir konsol penceresi.**

![yapılacaklar:resim_alternatif_Metin](http://i.imgur.com/zduARGh.png)
### **Pencere Elemanları Programlama Örneği Al**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(RetrieveWindowElementsOfDiagram.class);    
// load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// iterate through the window elements
for (Window window :(Iterable<Window>) diagram.getWindows())
{
    System.out.println("ID: " + window.getID());
    System.out.println("Type: " + window.getWindowType());
    System.out.println("Window height: " + window.getWindowHeight());
    System.out.println("Window width: " + window.getWindowWidth());
    System.out.println("Window state: " + window.getWindowState());
}

{{< /highlight >}}
```
## **Visio Diagram'e Pencere Elemanı Ekleyin**
 Ana Visio uygulama penceresi, herhangi bir açık Visio dosyasını içerebilir, tıpkı modern web tarayıcılarının bir pencerede birden çok sekmeli web sayfasına izin vermesi gibi. Geliştiriciler artık kullanarak bir Microsoft Visio örneğine yeni bir Window nesnesi ekleyebilir.[Aspose.Diagram for Java API](https://products.aspose.com/diagram/java/).

Window nesnesi, bir Microsoft Visio örneğindeki açık bir pencereyi temsil eder. WindowCollection sınıfı tarafından sunulan Add yöntemi, yeni bir Window nesnesi eklenmesine izin verir.
### **Pencere Elemanı Programlama Örneği Ekleme**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(AddWindowElementInVisio.class); 
// load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// initialize window object
Window window = new Window();
// set window state
window.setWindowState(WindowStateValue.MAXIMIZED);
// set window height
window.setWindowHeight(500);
// set window width
window.setWindowWidth(500);
// set window type
window.setWindowType(WindowTypeValue.STENCIL);
// add window object
diagram.getWindows().add(window);

// save in any supported format
diagram.save(dataDir + "AddWindowElementInVisio_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Dinamik Izgaralar ve Bağlantı Noktaları Desteği Ekleyin**
Dinamik ızgara, çizime zaten yerleştirdiğiniz şekillere göre yeni şekilleri dikey ve yatay olarak konumlandırmanıza yardımcı olur. Bağlantı noktaları ile ilgili olarak, işaretli olarak işaretlendikten sonra, onlara bağlanırken bağlantı noktalarını görmemize yardımcı olacaktır. kullanarak her iki seçeneği de elde edebiliriz.[Aspose.Diagram for Java API](https://products.aspose.com/diagram/java/).
### **Visio Teknik Resimlerinde Dinamik Izgaralar ve Bağlantı Noktaları Desteği**
Window sınıfı, DynamicGridEnabled ve ShowConnectionPoints özellikleri sunar. Bu özellikler, dinamik ızgaraları desteklemek ve bağlantı noktaları seçeneklerini göstermek için ayarları uygulamak için kullanılabilir.

**Visio'deki seçenekleri gösteren bir Visio uygulaması.**

![yapılacaklar:resim_alternatif_Metin](http://i.imgur.com/bxsJIwF.png)
#### **Destek Programlama Örneği Ekle**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(AddSupportOfVisualAids.class);
// load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// get window object by index
Window window = diagram.getWindows().get(0);
// check dynamic grid option
window.setDynamicGridEnabled(BOOL.TRUE);
// check connection points option
window.setShowConnectionPoints(BOOL.TRUE);
        
// save visio drawing
diagram.save(dataDir + "AddSupportOfVisualAids_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Visio Diagram'in Izgaralarını, Cetvellerini, Kılavuzlarını ve Sayfa Sonlarını Gösterme ve Gizleme**
 Microsoft Office Visio'de bir çift cetvel, bir ızgara ve iki tür kılavuz ve her sayfada ne yazdırılacağını görmek için sayfa sonu bayrağı bulunur. Geliştiriciler bu ayarları kullanarak uygulayabilir[Aspose.Diagram for Java API](https://products.aspose.com/diagram/java/)Ayarlar genel olarak tek bir sayfaya uygulanır.

Window sınıfı, ShowGrid, ShowGuides, ShowRulers ve ShowPageBreaks özelliklerini sunar. Bu özellikler ızgaraları, kılavuzları, cetvelleri ve sayfa sonlarını göstermek ve gizlemek için ayarları uygulamak için kullanılabilir.

**Visio'deki seçenekleri gösteren bir Visio uygulaması.**

![yapılacaklar:resim_alternatif_Metin](http://i.imgur.com/E0pvXbP.png)
### **Programlama Örneği**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(DisplayGridsRulersGuidesAndPageBreaks.class);     
// load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// get window object by index
Window window = diagram.getWindows().get(0);
// set visibility of grid
window.setShowGrid(BOOL.TRUE);
// set visibility of guides
window.setShowGuides(BOOL.TRUE);
// set visibility of rulers
window.setShowRulers(BOOL.TRUE);
// set visibility of page breaks
window.setShowPageBreaks(BOOL.TRUE);

// save diagram
diagram.save(dataDir + "DisplayGridsRulersGuidesAndPageBreaks_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
