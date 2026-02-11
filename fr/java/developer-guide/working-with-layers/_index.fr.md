---
title: Travailler avec des calques
type: docs
weight: 160
url: /fr/java/working-with-layers/
---
### **Configuration d'objets de forme avec des calques**
Aspose.Diagram for Java permet de configurer des objets de forme avec des couches dans Microsoft Office Visio diagram. Chaque forme peut appartenir à plusieurs couches afin que les développeurs puissent gérer les formes en fonction des besoins de l'utilisateur final.

 La[Forme](https://reference.aspose.com/diagram/java/com.aspose.diagram/Shape) L'objet de classe offre la propriété LayerMember qui permet d'ajouter/supprimer des objets de forme aux/des calques dans le dessin Visio. Les utilisateurs peuvent gérer ces propriétés par programmation en utilisant Aspose.Diagram API comme suit :

**Ajoutez, supprimez et déplacez des objets de forme vers / depuis les calques du diagram.** 

![tâche : image_autre_texte](working-with-layers_1.png)

Le morceau de code suivant permet d'ajouter, de supprimer et de déplacer les propriétés des objets de forme.
#### **Exemples de programmation**

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

### **Ajouter un calque dans la feuille de page Visio**
Aspose.Diagram for Java permet aux développeurs d'ajouter de nouveaux calques pour organiser des catégories personnalisées de formes, puis d'attribuer des formes à ces calques par programmation.

 La[LayerCollection](https://reference.aspose.com/diagram/java/com.aspose.diagram/LayerCollection) la classe propose une méthode add qui permet d'ajouter un nouveau[Couche](https://reference.aspose.com/diagram/java/com.aspose.diagram/layer)objet de classe dans le dessin Visio. Les développeurs peuvent définir les propriétés de la couche en initialisant son objet de classe.

Le morceau de code suivant permet d'ajouter des objets Layer.
#### **Exemples de programmation**

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

Aspose.Diagram for Java permet aux développeurs d'accéder aux couches existantes de Visio diagram.

{{% /alert %}} 
### **Obtenir toutes les couches disponibles**
 La[Feuille de page](https://reference.aspose.com/diagram/java/com.aspose.diagram/PageSheet) propriété de la[Page](https://reference.aspose.com/diagram/java/com.aspose.diagram/Page) class permet de récupérer la liste des calques disponibles depuis le Visio diagram en utilisant[LayerCollection](https://reference.aspose.com/diagram/java/com.aspose.diagram/layercollection) classer.

Le morceau de code suivant permet d'obtenir la liste des couches.
#### **Exemples de programmation**

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

