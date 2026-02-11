---
title: Trabajar con capas
type: docs
weight: 160
url: /es/python-java/working-with-layers/
---
### **Configuración de objetos de forma con capas**
Aspose.Diagram for Python via Java allows to configure shape objects with layers in Microsoft Office Visio diagram. Each shape can belong to multiple layers so developers can manage shapes to suit end user needs.

 los[Forma](https://reference.aspose.com/diagram/java/com.aspose.diagram/Shape) El objeto de clase ofrece la propiedad LayerMember que permite agregar / eliminar objetos de forma a / desde las capas en el dibujo Visio. Los usuarios pueden administrar estas propiedades mediante programación usando Aspose.Diagram API de la siguiente manera:

**Agregue, elimine y mueva objetos de forma a / desde capas del diagram.** 

El siguiente fragmento de código ayuda a agregar, eliminar y mover propiedades de objetos de forma.
#### **Ejemplos de programación**

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

### **Agregar una capa en la hoja de página Visio**
Aspose.Diagram for Python via Java allows developers to add new layers to organize custom categories of shapes, and then assign shapes to those layers programmatically.

 los[LayerCollection](https://reference.aspose.com/diagram/java/com.aspose.diagram/LayerCollection) class ofrece un método add que permite agregar un nuevo[Capa](https://reference.aspose.com/diagram/java/com.aspose.diagram/layer) objeto de clase en[el dibujo Visio](DrawingFlowChart.vsdx). Los desarrolladores pueden establecer las propiedades de la capa inicializando su objeto de clase.

El siguiente fragmento de código ayuda a agregar objetos de capa.
#### **Ejemplos de programación**

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
### **Obtener todas las capas disponibles**
 los[PáginaHoja](https://reference.aspose.com/diagram/java/com.aspose.diagram/PageSheet) propiedad de la[Página](https://reference.aspose.com/diagram/java/com.aspose.diagram/Page) class permite recuperar la lista de capas disponibles de[el dibujo Visio](DrawingFlowChart.vsdx) usando[LayerCollection](https://reference.aspose.com/diagram/java/com.aspose.diagram/layercollection) clase.

El siguiente fragmento de código ayuda a obtener una lista de capas.
#### **Ejemplos de programación**

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

