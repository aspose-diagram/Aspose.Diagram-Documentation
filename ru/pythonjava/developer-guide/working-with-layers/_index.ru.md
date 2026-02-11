---
title: Работа со слоями
type: docs
weight: 160
url: /ru/python-java/working-with-layers/
---
### **Настройка объектов Shape со слоями**
Aspose.Diagram для Python via Java позволяет настраивать объекты формы со слоями в Microsoft Office Visio diagram. Каждая фигура может принадлежать нескольким слоям, поэтому разработчики могут управлять формами в соответствии с потребностями конечного пользователя.

[Форма](https://reference.aspose.com/diagram/java/com.aspose.diagram/Shape) Объект класса предлагает свойство LayerMember, которое позволяет добавлять/удалять объекты формы в/из слоев в чертеже Visio. Пользователи могут программно управлять этими свойствами с помощью Aspose.Diagram API следующим образом:

**Добавляйте, удаляйте и перемещайте объекты формы в/из слоев diagram.** 

Следующий фрагмент кода помогает добавлять, удалять и перемещать свойства объектов формы.
#### **Примеры программирования**

{{< highlight python >}}
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

### **Добавьте слой на странице Visio.**
Aspose.Diagram для Python via Java позволяет разработчикам добавлять новые слои для организации пользовательских категорий фигур, а затем программно назначать фигуры этим слоям.

[СлойКоллекция](https://reference.aspose.com/diagram/java/com.aspose.diagram/LayerCollection) класс предлагает метод add, который позволяет добавить новый[Слой](https://reference.aspose.com/diagram/java/com.aspose.diagram/layer) объект класса в[чертеж Visio](DrawingFlowChart.vsdx). Разработчики могут устанавливать свойства слоя, инициализируя его объект класса.

Следующий фрагмент кода помогает добавить объекты слоя.
#### **Примеры программирования**

{{< highlight python >}}
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


{{% alert color="primary" %}} 

Aspose.Diagram для Python via Java предоставляет разработчикам доступ к существующим уровням Visio diagram.

{{% /alert %}} 
### **Получить все доступные слои**
[СтраницаЛист](https://reference.aspose.com/diagram/java/com.aspose.diagram/PageSheet) собственность[Страница](https://reference.aspose.com/diagram/java/com.aspose.diagram/Page) класс позволяет получить список доступных слоев из[чертеж Visio](DrawingFlowChart.vsdx) с использованием[СлойКоллекция](https://reference.aspose.com/diagram/java/com.aspose.diagram/layercollection) учебный класс.

Следующий фрагмент кода помогает получить список слоев.
#### **Примеры программирования**

{{< highlight python >}}
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

