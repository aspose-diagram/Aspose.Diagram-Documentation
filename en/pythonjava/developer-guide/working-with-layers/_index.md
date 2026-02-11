---
title: Working with Layers
type: docs
weight: 160
url: /python-java/working-with-layers/
---

### **Configuring Shape Objects with Layers**
Aspose.Diagram for Python via Java allows to configure shape objects with layers in Microsoft Office Visio diagram. Each shape can belong to multiple layers so developers can manage shapes to suit end user needs.

The [Shape](https://reference.aspose.com/diagram/java/com.aspose.diagram/Shape) class object offers LayerMember property which allows to add / remove shape objects to / from the layers in Visio drawing. Users can manage these properties programmatically using Aspose.Diagram API as follows:

**Add, remove and move shape objects to / from layers of the diagram.** 

The following piece of code helps to add, remove and move shape objects properties.
#### **Programming Samples**

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

### **Add a Layer in the Visio PageSheet**
Aspose.Diagram for Python via Java allows developers to add new layers to organize custom categories of shapes, and then assign shapes to those layers programmatically.

The [LayerCollection](https://reference.aspose.com/diagram/java/com.aspose.diagram/LayerCollection) class offers add method which allows to add a new [Layer](https://reference.aspose.com/diagram/java/com.aspose.diagram/layer) class object in [the Visio drawing](DrawingFlowChart.vsdx). Developers can set Layer properties by initializing its class object.

The following piece of code helps to add Layer objects.
#### **Programming Samples**

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

Aspose.Diagram for Python via Java gives developers access to the existing layers of Visio diagram.

{{% /alert %}} 
### **Get All Available Layers**
The [PageSheet](https://reference.aspose.com/diagram/java/com.aspose.diagram/PageSheet) property of the [Page](https://reference.aspose.com/diagram/java/com.aspose.diagram/Page) class allows to retrieve the list of available layers from [the Visio drawing](DrawingFlowChart.vsdx) using [LayerCollection](https://reference.aspose.com/diagram/java/com.aspose.diagram/layercollection) class.

The following piece of code helps to get list of Layers.
#### **Programming Samples**

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

