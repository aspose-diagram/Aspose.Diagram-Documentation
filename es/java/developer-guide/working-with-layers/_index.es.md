---
title: Trabajar con capas
type: docs
weight: 160
url: /es/java/working-with-layers/
---
### **Configuración de objetos de forma con capas**
Aspose.Diagram for Java permite configurar objetos de forma con capas en Microsoft Office Visio diagram. Cada forma puede pertenecer a varias capas para que los desarrolladores puedan administrar las formas para satisfacer las necesidades del usuario final.

 los[Forma](https://reference.aspose.com/diagram/java/com.aspose.diagram/Shape) El objeto de clase ofrece la propiedad LayerMember que permite agregar / eliminar objetos de forma a / desde las capas en el dibujo Visio. Los usuarios pueden administrar estas propiedades mediante programación usando Aspose.Diagram API de la siguiente manera:

**Agregue, elimine y mueva objetos de forma a / desde capas del diagram.** 

![todo:imagen_alternativa_texto](working-with-layers_1.png)

El siguiente fragmento de código ayuda a agregar, eliminar y mover propiedades de objetos de forma.
#### **Ejemplos de programación**
```
{{< highlight "java" >}}
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
```
### **Agregar una capa en la hoja de página Visio**
Aspose.Diagram for Java permite a los desarrolladores agregar nuevas capas para organizar categorías personalizadas de formas y luego asignar formas a esas capas mediante programación.

 los[LayerCollection](https://reference.aspose.com/diagram/java/com.aspose.diagram/LayerCollection) class ofrece un método add que permite agregar un nuevo[Capa](https://reference.aspose.com/diagram/java/com.aspose.diagram/layer)objeto de clase en el dibujo Visio. Los desarrolladores pueden establecer las propiedades de la capa inicializando su objeto de clase.

El siguiente fragmento de código ayuda a agregar objetos de capa.
#### **Ejemplos de programación**
```
{{< highlight "java" >}}
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
```

{{% alert color="primary" %}} 

Aspose.Diagram for Java brinda a los desarrolladores acceso a las capas existentes de Visio diagram.

{{% /alert %}} 
### **Obtener todas las capas disponibles**
 los[PáginaHoja](https://reference.aspose.com/diagram/java/com.aspose.diagram/PageSheet) propiedad de la[Página](https://reference.aspose.com/diagram/java/com.aspose.diagram/Page) class permite recuperar la lista de capas disponibles del Visio diagram usando[LayerCollection](https://reference.aspose.com/diagram/java/com.aspose.diagram/layercollection) clase.

El siguiente fragmento de código ayuda a obtener una lista de capas.
#### **Ejemplos de programación**
```
{{< highlight "java" >}}
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
```
