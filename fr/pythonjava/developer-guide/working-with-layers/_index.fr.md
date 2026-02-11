---
title: Travailler avec des calques
type: docs
weight: 160
url: /fr/python-java/working-with-layers/
---
### **Configuration d'objets de forme avec des calques**
Aspose.Diagram for Python via Java allows to configure shape objects with layers in Microsoft Office Visio diagram. Each shape can belong to multiple layers so developers can manage shapes to suit end user needs.

 La[Forme](https://reference.aspose.com/diagram/java/com.aspose.diagram/Shape) L'objet de classe offre la propriété LayerMember qui permet d'ajouter/supprimer des objets de forme aux/des calques dans le dessin Visio. Les utilisateurs peuvent gérer ces propriétés par programmation en utilisant Aspose.Diagram API comme suit :

**Ajoutez, supprimez et déplacez des objets de forme vers / depuis les calques du diagram.** 

Le morceau de code suivant permet d'ajouter, de supprimer et de déplacer les propriétés des objets de forme.
#### **Exemples de programmation**
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
### **Ajouter un calque dans la feuille de page Visio**
Aspose.Diagram for Python via Java allows developers to add new layers to organize custom categories of shapes, and then assign shapes to those layers programmatically.

 La[LayerCollection](https://reference.aspose.com/diagram/java/com.aspose.diagram/LayerCollection) la classe propose une méthode add qui permet d'ajouter un nouveau[Couche](https://reference.aspose.com/diagram/java/com.aspose.diagram/layer) objet de classe dans[le dessin Visio](DrawingFlowChart.vsdx). Les développeurs peuvent définir les propriétés de la couche en initialisant son objet de classe.

Le morceau de code suivant permet d'ajouter des objets Layer.
#### **Exemples de programmation**
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
### **Obtenir toutes les couches disponibles**
 La[Feuille de page](https://reference.aspose.com/diagram/java/com.aspose.diagram/PageSheet) propriété de la[Page](https://reference.aspose.com/diagram/java/com.aspose.diagram/Page) class permet de récupérer la liste des couches disponibles à partir de[le dessin Visio](DrawingFlowChart.vsdx) utilisant[LayerCollection](https://reference.aspose.com/diagram/java/com.aspose.diagram/layercollection) classer.

Le morceau de code suivant permet d'obtenir la liste des couches.
#### **Exemples de programmation**
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
