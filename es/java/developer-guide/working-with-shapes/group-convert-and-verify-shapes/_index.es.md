---
title: Agrupar, convertir y verificar formas
type: docs
weight: 50
url: /es/java/group-convert-and-verify-shapes/
---
## **Agrupe varias formas juntas en el dibujo Visio**
Aspose.Diagram API permite a los desarrolladores agrupar formas para moverlas todas a la vez. Cada forma en un grupo mantiene una identidad única y tiene su propio conjunto de propiedades. Cuando cambiamos el formato de un grupo de formas, asigna la nueva propiedad a cada forma.
### **Cómo agrupar formas**
El método Group expuesto por la clase ShapeCollection se puede usar para agrupar formas.

El siguiente código muestra cómo:

1. Cargue una muestra diagram.
1. inicializó una matriz de las formas
1. obtener una forma particular por id.
1. obtener otra forma particular particular por id.
1. asignar formas a la matriz.
1. formas de grupo llamando al método Group.
1. guardar diagram
#### **Ejemplo de programación de formas grupales**
Use el siguiente código en su aplicación Java para agrupar formas usando Aspose.Diagram for Java API.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(GroupShapes.class);
// load a Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get page by name
Page page = diagram.getPages().getPage("Page-3");

// Initialize an array of shapes
Shape[] ss = new Shape[3];

// extract and assign shapes to the array
ss[0] = page.getShapes().getShape(15);
ss[1] = page.getShapes().getShape(16);
ss[2] = page.getShapes().getShape(17);

// mark array shapes as group
page.getShapes().group(ss);

// save visio diagram
diagram.save(dataDir + "GroupShapes_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Convierta una forma Visio a otros formatos de archivo**
Aspose.Diagram for Java API permite a los desarrolladores convertir una sola forma Visio a cualquier otro formato de archivo compatible. En este artículo, eliminamos todas las demás formas Visio de la página y personalizamos la configuración de la página según el tamaño de la forma de origen.
### **Convertir una forma particular Visio**
Developers can convert a Visio shape to PDF, HTML, Image, SVG, and SWF by [especificando las opciones de guardado Visio]().
Este código de ejemplo funciona de la siguiente manera:

1. Cargue una fuente Visio.
1. Obtener una página en particular.
1. Eliminar la página de fondo.
1. Cree una tabla hash de todas las formas que contenga las identificaciones y los nombres.
1. Iterar a través de la tabla hash
1. Elimina todas las formas de la página Visio, excepto la particular.
1. Establezca el tamaño de la página.
1. Guarde la página Visio en cualquier formato de archivo compatible.
#### **Ejemplo de programación de conversión de formas**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(SaveVisioShapeInOtherFormats.class);   
        
double shapeWidth = 0;
double shapeHeight = 0;

// call a Diagram class constructor to load the VSDX diagram
Diagram srcVisio = new Diagram(dataDir + "Drawing1.vsdx");
// get Visio page
Page srcPage = srcVisio.getPages().get(1);
// remove background page
srcPage.setBackPage(null);

// get hash table of shapes, it holds id and name
Hashtable<Long, String> remShapes = new Hashtable<Long, String>();
for (Shape shape : (Iterable<Shape>)srcPage.getShapes())
    // for the normal shape
    remShapes.put(shape.getID(), shape.getName());
        

// iterate through the hash table
Enumeration<Long> enumKey = remShapes.keys();
while(enumKey.hasMoreElements())
{
    Long key = enumKey.nextElement();
    String val = remShapes.get(key);
    Shape shape = srcPage.getShapes().getShape(key);
    // check of the shape name
    if(val.equals("GroupShape1"))
    {
        // move shape to the origin corner
        shapeWidth = shape.getXForm().getWidth().getValue();
        shapeHeight = shape.getXForm().getHeight().getValue();
        shape.moveTo(shapeWidth*0.5, shapeHeight*0.5);
        // trim page size
        srcPage.getPageSheet().getPageProps().getPageWidth().setValue(shapeWidth);
        srcPage.getPageSheet().getPageProps().getPageHeight().setValue(shapeHeight);
    }
    else
    {
        // remove shape from the Visio page and hash table
        srcPage.getShapes().remove(shape);
        remShapes.remove(key);
    }
}

// specify saving options
PdfSaveOptions opts = new PdfSaveOptions();
// set page count to save
opts.setPageCount(1);
// set starting index of the page
opts.setPageIndex(1);
// save it
srcVisio.save(dataDir + "SaveVisioShapeInOtherFormats_Out.pdf", opts);

{{< /highlight >}}

### **Convert Visio Shape to PDF**
The ToPdf method of the Shape class allows to convert a shape into the PDF format.

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// save a shape in the PDF format

diagram.getPages().get(0).getShapes().getShape(59).toPdf(dataDir + "out.pdf");

{{< /highlight >}}
### **Convert Visio Shape to HTML**
The ToHTML method of the Shape class allows to convert a shape into the HTML format.

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

HTMLSaveOptions hs = new HTMLSaveOptions();

// save a shape in the PDF format

diagram.getPages().get(0).getShapes().getShape(59).toHTML(dataDir + "out.pdf", hs);

{{< /highlight >}}

{{% alert color="primary" %}} 

 Agradecemos sus consultas y sugerencias en[Aspose.Diagram Foro](https://forum.aspose.com/c/diagram/17). Responderemos a la brevedad.

{{% /alert %}} 
## **Verifique si dos formas Visio están conectadas o pegadas**
 Aspose.Diagram for Java API permite a los desarrolladores verificar que las dos formas Visio estén pegadas o conectadas. Anteriormente, hemos visto cómo podemos conectar o pegar dos formas en estos temas de ayuda:[Agregar y conectar Visio Formas](/diagram/es/java/add-and-connect-visio-shapes/) y[Pegue las formas dentro del recipiente](/diagram/es/java/working-with-shapes-gluing/).
### **Verificación de las Formas Conectadas o Pegadas**
 los[Forma](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) class ofrece las propiedades IsGlued e IsConnected para determinar si dos formas están pegadas o conectadas.
#### **Muestra de Programación de Verificación de Formas Conectadas o Pegadas**
El siguiente fragmento de código verifica si dos formas están conectadas o pegadas.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(VerifyConnectedOrGluedShapes.class);  
// call a Diagram class constructor to load the VSD diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// set two shape ids
long ShapeIdOne = 15;
long ShapeIdTwo = 16;

// get Visio page by name
Page page = diagram.getPages().getPage("Page-3");

// get Visio shapes by ids
Shape ShapedOne = page.getShapes().getShape(ShapeIdOne);
Shape ShapedTwo = page.getShapes().getShape(ShapeIdTwo);

// determine whether shapes are connected
boolean connected = ShapedOne.isConnected(ShapedTwo);
System.out.println("Shapes are connected: " + connected);

// determine whether shapes are glued
boolean glued = ShapedOne.isGlued(ShapedTwo);
System.out.println("Shapes are Glued: " + glued);

{{< /highlight >}}

## **Verifique si la forma Visio está en un grupo de formas**
Aspose.Diagram for Java API permite a los desarrolladores verificar si la forma Visio está en un grupo de formas o no.
### **Verificación de Forma en el Grupo de Formas**
La clase Shape ofrece propiedades IsInGroup para determinar si la forma Visio está en una forma de grupo.
#### **Verificación de la forma en el ejemplo de programación del grupo de formas**
El siguiente fragmento de código verifica si la forma está en una forma de grupo.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getSharedDataDir(RetrieveTheParentShape.class) + "Shapes\\";
				
// Call a Diagram class constructor to load the VSD diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get a sub-shape by page name, group shape ID, and then sub-shape ID
Shape shape = diagram.getPages().getPage("Page-3").getShapes().getShape(13).getShapes().getShape(2);
System.out.println("Is it in a Group: " + shape.isInGroup());
{{< /highlight >}}


{{% alert color="primary" %}} 

 Agradecemos sus consultas y sugerencias en[Aspose.Diagram Foro](https://forum.aspose.com/c/diagram/17). Responderemos a la brevedad.

{{% /alert %}}
