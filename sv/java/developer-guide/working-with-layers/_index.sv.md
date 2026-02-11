---
title: Arbeta med lager
type: docs
weight: 160
url: /sv/java/working-with-layers/
---
### **Konfigurera formobjekt med lager**
Aspose.Diagram for Java gör det möjligt att konfigurera formobjekt med lager i Microsoft Office Visio diagram. Varje form kan tillhöra flera lager så att utvecklare kan hantera former för att passa slutanvändarens behov.

 De[Form](https://reference.aspose.com/diagram/java/com.aspose.diagram/Shape) class object erbjuder LayerMember-egenskapen som gör det möjligt att lägga till/ta bort formobjekt till/från lagren i Visio-ritningen. Användare kan hantera dessa egenskaper programmatiskt med Aspose.Diagram API enligt följande:

**Lägg till, ta bort och flytta formobjekt till/från lager i diagram.** 

![todo:image_alt_text](working-with-layers_1.png)

Följande kodbit hjälper till att lägga till, ta bort och flytta formobjektegenskaper.
#### **Programmeringsexempel**

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

### **Lägg till ett lager i sidbladet Visio**
Aspose.Diagram for Java tillåter utvecklare att lägga till nya lager för att organisera anpassade kategorier av former och sedan tilldela former till dessa lager programmatiskt.

 De[LayerCollection](https://reference.aspose.com/diagram/java/com.aspose.diagram/LayerCollection) class erbjuder add-metod som gör det möjligt att lägga till en ny[Lager](https://reference.aspose.com/diagram/java/com.aspose.diagram/layer)klassobjekt i Visio-ritningen. Utvecklare kan ställa in lageregenskaper genom att initiera dess klassobjekt.

Följande kodbit hjälper till att lägga till Layer-objekt.
#### **Programmeringsexempel**

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

Aspose.Diagram for Java ger utvecklare tillgång till de befintliga lagren av Visio diagram.

{{% /alert %}} 
### **Få alla tillgängliga lager**
 De[PageSheet](https://reference.aspose.com/diagram/java/com.aspose.diagram/PageSheet) egendom av[Sida](https://reference.aspose.com/diagram/java/com.aspose.diagram/Page) klass gör det möjligt att hämta listan över tillgängliga lager från Visio diagram med[LayerCollection](https://reference.aspose.com/diagram/java/com.aspose.diagram/layercollection) klass.

Följande kodbit hjälper dig att få en lista över lager.
#### **Programmeringsexempel**

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

