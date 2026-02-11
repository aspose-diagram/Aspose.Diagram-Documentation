---
title: Katmanlarla Çalışmak
type: docs
weight: 160
url: /tr/java/working-with-layers/
---
### **Şekil Nesnelerini Katmanlarla Yapılandırma**
Aspose.Diagram for Java, şekil nesnelerini Microsoft Office Visio diagram'de katmanlarla yapılandırmaya izin verir. Her şekil birden fazla katmana ait olabilir, böylece geliştiriciler son kullanıcı ihtiyaçlarına uygun şekilleri yönetebilir.

 bu[Şekil](https://reference.aspose.com/diagram/java/com.aspose.diagram/Shape) class nesnesi, Visio çiziminde katmanlara / katmanlardan şekil nesneleri eklemeye / kaldırmaya izin veren LayerMember özelliğini sunar. Kullanıcılar bu özellikleri programlı olarak Aspose.Diagram API kullanarak aşağıdaki gibi yönetebilir:

**diagram'in katmanlarına / katmanlarından şekil nesneleri ekleyin, kaldırın ve taşıyın.** 

![yapılacaklar:resim_alternatif_Metin](working-with-layers_1.png)

Aşağıdaki kod parçası, şekil nesneleri özelliklerini eklemeye, kaldırmaya ve taşımaya yardımcı olur.
#### **Programlama Örnekleri**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ConfigureShapeLayers.class);
        
//call the diagram constructor to load visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
        
// iterate through the shapes
for (Shape shape : (Iterable<Shape>) diagram.getPages().getPage("Page-1").getShapes())
{
    if (shape.getName().toLowerCase() == "shape1")
    {
        //Add shape1 in first two layers. Here "0;1" are indexes of the layers
        LayerMem layer = shape.getLayerMem();
        layer.getLayerMember().setValue("0;1");
    }
    else if (shape.getName().toLowerCase() == "shape2")
    {
        //Remove shape2 from all the layers
        LayerMem layer = shape.getLayerMem();
        layer.getLayerMember().setValue("");
    }
    else if (shape.getName().toLowerCase() == "shape3")
    {
        //Add shape3 in first layer. Here "0" is index of the first layer
        LayerMem layer = shape.getLayerMem();
        layer.getLayerMember().setValue("0");
    }
}
// save diagram
diagram.save(dataDir + "ConfigureShapeLayers_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

### **Visio Sayfa Sayfasına Katman Ekleme**
Aspose.Diagram for Java, geliştiricilerin özel şekil kategorilerini düzenlemek için yeni katmanlar eklemesine ve ardından bu katmanlara programlı olarak şekiller atamasına olanak tanır.

 bu[Katman Koleksiyonu](https://reference.aspose.com/diagram/java/com.aspose.diagram/LayerCollection) class, yeni bir tane eklemeye izin veren add yöntemini sunar.[Katman](https://reference.aspose.com/diagram/java/com.aspose.diagram/layer)Visio çizimindeki sınıf nesnesi. Geliştiriciler, sınıf nesnesini başlatarak Katman özelliklerini ayarlayabilir.

Aşağıdaki kod parçası, Katman nesneleri eklemeye yardımcı olur.
#### **Programlama Örnekleri**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getSharedDataDir(AddLayer.class) + "Layers/";

// load a source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get Visio page
Page page = diagram.getPages().getPage("Page-1");

// initialize a new Layer class object
Layer layer = new Layer();
// set Layer name
layer.getName().setValue("Layer1");
// set Layer Visibility
layer.getVisible().setValue(BOOL.TRUE);
// set the color checkbox of Layer
layer.setColorChecked(BOOL.TRUE);
// add Layer to the particular page sheet
page.getPageSheet().getLayers().add(layer);

// get shape by ID
Shape shape = page.getShapes().getShape(3);
// assign shape to this new Layer
shape.getLayerMem().getLayerMember().setValue(Integer.toString(layer.getIX()));
// save diagram
diagram.save(dataDir + "AddLayer_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}


{{% alert color="primary" %}} 

Aspose.Diagram for Java, geliştiricilere mevcut Visio diagram katmanlarına erişim sağlar.

{{% /alert %}} 
### **Mevcut Tüm Katmanları Alın**
 bu[Sayfa Sayfası](https://reference.aspose.com/diagram/java/com.aspose.diagram/PageSheet) mülkiyeti[Sayfa](https://reference.aspose.com/diagram/java/com.aspose.diagram/Page) class, kullanarak Visio diagram'den kullanılabilir katmanların listesini almaya izin verir.[Katman Koleksiyonu](https://reference.aspose.com/diagram/java/com.aspose.diagram/layercollection) sınıf.

Aşağıdaki kod parçası, Katmanların listesini almanıza yardımcı olur.
#### **Programlama Örnekleri**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(RetrieveAllLayers.class);  
// load Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get Visio page
Page page = diagram.getPages().getPage("Page-1");

// iterate through the layers
for (Layer layer : (Iterable<Layer>) page.getPageSheet().getLayers())
{
    System.out.println("Name: " + layer.getName().getValue());
    System.out.println("Visibility: " + layer.getVisible().getValue());
    System.out.println("Status: " + layer.getStatus().getValue());
}

{{< /highlight >}}

