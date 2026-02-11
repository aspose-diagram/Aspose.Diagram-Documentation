---
title: Katmanlarla Çalışmak
type: docs
weight: 160
url: /tr/python-java/working-with-layers/
---
### **Şekil Nesnelerini Katmanlarla Yapılandırma**
Python via Java için Aspose.Diagram, şekil nesnelerinin Microsoft Office Visio diagram'deki katmanlarla yapılandırılmasına olanak tanır. Her şekil birden fazla katmana ait olabilir, böylece geliştiriciler son kullanıcı ihtiyaçlarına uygun şekilleri yönetebilir.

 bu[Şekil](https://reference.aspose.com/diagram/java/com.aspose.diagram/Shape) class nesnesi, Visio çiziminde katmanlara / katmanlardan şekil nesneleri eklemeye / kaldırmaya izin veren LayerMember özelliğini sunar. Kullanıcılar bu özellikleri programlı olarak Aspose.Diagram API kullanarak aşağıdaki gibi yönetebilir:

**diagram'in katmanlarına / katmanlarından şekil nesneleri ekleyin, kaldırın ve taşıyın.** 

Aşağıdaki kod parçası, şekil nesneleri özelliklerini eklemeye, kaldırmaya ve taşımaya yardımcı olur.
#### **Programlama Örnekleri**
```
{{< highlight "python" >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")
        
# call the diagram constructor to load visio diagram
diagram = Diagram("DrawingFlowChart.vsdx")
        
# iterate through the shapes
for shape in diagram.getPages().getPage("Page-1").getShapes():
    if shape.getName().toLowerCase() == "shape1":
        # Add shape1 in first two layers. Here "0;1" are indexes of the layers
        layer = shape.getLayerMem()
        layer.getLayerMember().setValue("0;1")
    elif shape.getName().toLowerCase() == "shape2":
        # Remove shape2 from all the layers
        layer = shape.getLayerMem()
        layer.getLayerMember().setValue("")
    elif shape.getName().toLowerCase() == "shape3":
        # Add shape3 in first layer. Here "0" is index of the first layer
        layer = shape.getLayerMem()
        layer.getLayerMember().setValue("0")

# save diagram
diagram.save("ConfigureShapeLayers_Out.vsdx", SaveFileFormat.VSDX)

jpype.shutdownJVM()

{{< /highlight >}}
```
### **Visio Sayfa Sayfasına Katman Ekleme**
Python via Java için Aspose.Diagram, geliştiricilerin özel şekil kategorilerini düzenlemek için yeni katmanlar eklemesine ve ardından bu katmanlara programlı olarak şekiller atamasına olanak tanır.

 bu[Katman Koleksiyonu](https://reference.aspose.com/diagram/java/com.aspose.diagram/LayerCollection) class, yeni bir tane eklemeye izin veren add yöntemini sunar.[Katman](https://reference.aspose.com/diagram/java/com.aspose.diagram/layer) sınıf nesnesi[Visio çizimi](DrawingFlowChart.vsdx). Geliştiriciler, sınıf nesnesini başlatarak Katman özelliklerini ayarlayabilir.

Aşağıdaki kod parçası, Katman nesneleri eklemeye yardımcı olur.
#### **Programlama Örnekleri**
```
{{< highlight "python" >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# load a source Visio diagram
diagram = Diagram("DrawingFlowChart.vsdx")
# get Visio page
page = diagram.getPages().getPage("Page-1")

# initialize a new Layer class object
layer = Layer()
# set Layer name
layer.getName().setValue("Layer1")
# set Layer Visibility
layer.getVisible().setValue(BOOL.TRUE)
# set the color checkbox of Layer
layer.setColorChecked(BOOL.TRUE)
# add Layer to the particular page sheet
page.getPageSheet().getLayers().add(layer)

# get shape by ID
shape = page.getShapes().getShape(3)
# assign shape to this new Layer
shape.getLayerMem().getLayerMember().setValue(str(layer.getIX()))
# save diagram
diagram.save("AddLayer_Out.vsdx", SaveFileFormat.VSDX)

jpype.shutdownJVM()

{{< /highlight >}}
```

{{% alert color="primary" %}} 

Python via Java için Aspose.Diagram, geliştiricilere mevcut Visio diagram katmanlarına erişim sağlar.

{{% /alert %}} 
### **Mevcut Tüm Katmanları Alın**
 bu[Sayfa Sayfası](https://reference.aspose.com/diagram/java/com.aspose.diagram/PageSheet) mülkiyeti[Sayfa](https://reference.aspose.com/diagram/java/com.aspose.diagram/Page) class, kullanılabilir katmanların listesinin alınmasına izin verir.[Visio çizimi](DrawingFlowChart.vsdx) kullanarak[Katman Koleksiyonu](https://reference.aspose.com/diagram/java/com.aspose.diagram/layercollection) sınıf.

Aşağıdaki kod parçası, Katmanların listesini almanıza yardımcı olur.
#### **Programlama Örnekleri**
```
{{< highlight "python" >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# load Visio diagram
diagram = Diagram("DrawingFlowChart.vsdx")
# get Visio page
page = diagram.getPages().getPage("Page-1")

# iterate through the layers
for layer in page.getPageSheet().getLayers():
    print("Name: " + str(layer.getName().getValue()))
    print("Visibility: " + str(layer.getVisible().getValue()))
    print("Status: " + str(layer.getStatus().getValue()))

jpype.shutdownJVM()

{{< /highlight >}}
```
