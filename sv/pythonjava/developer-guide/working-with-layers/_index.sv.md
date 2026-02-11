---
title: Arbeta med lager
type: docs
weight: 160
url: /sv/python-java/working-with-layers/
---
### **Konfigurera formobjekt med lager**
Aspose.Diagram för Python via Java gör det möjligt att konfigurera formobjekt med lager i Microsoft Office Visio diagram. Varje form kan hantera flera lagers behov så att användaren kan hantera flera lagers behov.

 De[Form](https://reference.aspose.com/diagram/java/com.aspose.diagram/Shape) class object erbjuder LayerMember-egenskapen som gör det möjligt att lägga till/ta bort formobjekt till/från lagren i Visio-ritningen. Användare kan hantera dessa egenskaper programmatiskt med Aspose.Diagram API enligt följande:

**Lägg till, ta bort och flytta formobjekt till/från lager i diagram.** 

Följande kodbit hjälper till att lägga till, ta bort och flytta formobjektegenskaper.
#### **Programmeringsexempel**
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
### **Lägg till ett lager i sidbladet Visio**
Aspose.Diagram för Python via Java tillåter utvecklare att lägga till nya lager för att organisera anpassade kategorier av former och sedan tilldela former till dessa lager programmatiskt.

 De[LayerCollection](https://reference.aspose.com/diagram/java/com.aspose.diagram/LayerCollection) class erbjuder add-metod som gör det möjligt att lägga till en ny[Lager](https://reference.aspose.com/diagram/java/com.aspose.diagram/layer) klassobjekt i[Visio ritningen](DrawingFlowChart.vsdx). Utvecklare kan ställa in lageregenskaper genom att initiera dess klassobjekt.

Följande kodbit hjälper till att lägga till Layer-objekt.
#### **Programmeringsexempel**
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

Aspose.Diagram för Python via Java ger utvecklare tillgång till de befintliga lagren av Visio diagram.

{{% /alert %}} 
### **Få alla tillgängliga lager**
 De[PageSheet](https://reference.aspose.com/diagram/java/com.aspose.diagram/PageSheet) egendom av[Sida](https://reference.aspose.com/diagram/java/com.aspose.diagram/Page) klass gör det möjligt att hämta listan över tillgängliga lager från[Visio ritningen](DrawingFlowChart.vsdx) använder sig av[LayerCollection](https://reference.aspose.com/diagram/java/com.aspose.diagram/layercollection) klass.

Följande kodbit hjälper dig att få en lista över lager.
#### **Programmeringsexempel**
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
