---
title: Lavorare con i livelli
type: docs
weight: 160
url: /it/python-java/working-with-layers/
---
### **Configurazione di oggetti forma con livelli**
Aspose.Diagram for Python via Java allows to configure shape objects with layers in Microsoft Office Visio diagram. Each shape can belong to multiple layers so developers can manage shapes to suit end user needs.

 Il[Forma](https://reference.aspose.com/diagram/java/com.aspose.diagram/Shape) L'oggetto class offre la proprietà LayerMember che consente di aggiungere/rimuovere oggetti forma a/dai livelli nel disegno Visio. Gli utenti possono gestire queste proprietà a livello di codice utilizzando Aspose.Diagram API come segue:

**Aggiungi, rimuovi e sposta oggetti forma a/da livelli di diagram.** 

Il seguente pezzo di codice aiuta ad aggiungere, rimuovere e spostare le proprietà degli oggetti forma.
#### **Esempi di programmazione**
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
### **Aggiungi un livello nel foglio di pagina Visio**
Aspose.Diagram for Python via Java allows developers to add new layers to organize custom categories of shapes, and then assign shapes to those layers programmatically.

 Il[Raccolta livelli](https://reference.aspose.com/diagram/java/com.aspose.diagram/LayerCollection) class offre il metodo add che consente di aggiungere un nuovo file[Strato](https://reference.aspose.com/diagram/java/com.aspose.diagram/layer) oggetto di classe in[il disegno Visio](DrawingFlowChart.vsdx). Gli sviluppatori possono impostare le proprietà del livello inizializzando il suo oggetto di classe.

Il seguente pezzo di codice aiuta ad aggiungere oggetti Layer.
#### **Esempi di programmazione**
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
### **Ottieni tutti i livelli disponibili**
 Il[PaginaFoglio](https://reference.aspose.com/diagram/java/com.aspose.diagram/PageSheet) proprietà del[Pagina](https://reference.aspose.com/diagram/java/com.aspose.diagram/Page) class consente di recuperare l'elenco dei layer disponibili da[il disegno Visio](DrawingFlowChart.vsdx) utilizzando[Raccolta livelli](https://reference.aspose.com/diagram/java/com.aspose.diagram/layercollection) classe.

Il seguente pezzo di codice aiuta a ottenere l'elenco dei livelli.
#### **Esempi di programmazione**
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
