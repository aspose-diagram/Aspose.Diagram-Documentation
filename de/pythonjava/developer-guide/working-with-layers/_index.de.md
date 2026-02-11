---
title: Arbeiten mit Ebenen
type: docs
weight: 160
url: /de/python-java/working-with-layers/
---
### **Konfigurieren von Formobjekten mit Ebenen**
Aspose.Diagram for Python via Java allows to configure shape objects with layers in Microsoft Office Visio diagram. Each shape can belong to multiple layers so developers can manage shapes to suit end user needs.

 Das[Form](https://reference.aspose.com/diagram/java/com.aspose.diagram/Shape) Das Klassenobjekt bietet die LayerMember-Eigenschaft, mit der Formobjekte zu den Ebenen in der Visio-Zeichnung hinzugefügt / entfernt werden können. Benutzer können diese Eigenschaften programmgesteuert mit Aspose.Diagram API wie folgt verwalten:

**Hinzufügen, Entfernen und Verschieben von Formobjekten zu / von Ebenen des diagram.** 

Der folgende Codeabschnitt hilft beim Hinzufügen, Entfernen und Verschieben von Formobjekteigenschaften.
#### **Programmierbeispiele**
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
### **Fügen Sie eine Ebene im PageSheet Visio hinzu**
Aspose.Diagram for Python via Java allows developers to add new layers to organize custom categories of shapes, and then assign shapes to those layers programmatically.

 Das[LayerCollection](https://reference.aspose.com/diagram/java/com.aspose.diagram/LayerCollection) Die Klasse bietet die Methode add an, mit der Sie eine neue hinzufügen können[Schicht](https://reference.aspose.com/diagram/java/com.aspose.diagram/layer) Klassenobjekt ein[die Zeichnung Visio](DrawingFlowChart.vsdx). Entwickler können Layer-Eigenschaften festlegen, indem sie ihr Klassenobjekt initialisieren.

Der folgende Codeabschnitt hilft beim Hinzufügen von Layer-Objekten.
#### **Programmierbeispiele**
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

Aspose.Diagram for Python via Java gives developers access to the existing layers of Visio diagram.

{{% /alert %}} 
### **Holen Sie sich alle verfügbaren Ebenen**
 Das[Seitenblatt](https://reference.aspose.com/diagram/java/com.aspose.diagram/PageSheet) Eigentum der[Buchseite](https://reference.aspose.com/diagram/java/com.aspose.diagram/Page) -Klasse ermöglicht es, die Liste der verfügbaren Layer abzurufen[die Zeichnung Visio](DrawingFlowChart.vsdx) verwenden[LayerCollection](https://reference.aspose.com/diagram/java/com.aspose.diagram/layercollection) Klasse.

Der folgende Codeabschnitt hilft, eine Liste der Ebenen zu erhalten.
#### **Programmierbeispiele**
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
