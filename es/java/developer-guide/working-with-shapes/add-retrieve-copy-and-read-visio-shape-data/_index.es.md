---
title: Agregar, recuperar, copiar y leer datos de forma Visio
type: docs
weight: 10
url: /es/java/add-retrieve-copy-and-read-visio-shape-data/
description: Esta sección explica cómo agregar una forma, establecer la propiedad de la forma o copiar una forma con Aspose.Diagram.
---
## **Agregar una nueva forma en Visio**
Aspose.Diagram for Java le permite manipular Microsoft Visio diagramas de diferentes maneras. Una de las cosas que puede hacer es agregar nuevas formas a los diagramas. Aspose.Diagram for Java le permite agregar una nueva forma a un diagram. La forma agregada también se puede personalizar usando Aspose.Diagram for Java.

Este tema describe cómo agregar una nueva forma de rectángulo a un diagram.

Use Aspose.Diagram for Java API para crear nuevas formas y luego agregue estas formas a la colección de formas de diagram.

Para agregar una nueva forma:

1. **Encuentra la página** - Cada Visio diagram contiene una colección de páginas. Los desarrolladores pueden recuperar la página por ID o nombre de página y almacenar la página requerida en el[Página](https://reference.aspose.com/diagram/java/com.aspose.diagram/page)objeto de clase.
1. **Agregue el maestro requerido de una forma** - Cada Visio diagram contiene una colección de maestros. Los desarrolladores pueden agregar un maestro (por ID o nombre) del archivo de plantilla existente (por ruta directa o flujo de archivo).
1. **Añadir forma en el Visio diagram** - Los desarrolladores pueden colocar una nueva forma en el Visio diagram por índice de página (a partir de 0), nombre maestro, PinX, PinY, alto (opcional) y ancho (opcional).
1. **Establecer propiedades de forma** - El método AddShape de la clase Diagram devuelve el ID de la forma. Los desarrolladores pueden recuperar la forma de un Visio diagram usando este ID y luego establecer sus propiedades, por ejemplo, color, posición, alineación y texto.

|<p>**La entrada diagram** </p><p>![todo:imagen_alternativa_texto](add-retrieve-copy-and-read-visio-shape-data_1.png)</p>|<p>**El diagram con una forma añadida** </p><p>![todo:imagen_alternativa_texto](add-retrieve-copy-and-read-visio-shape-data_2.png)</p>|
|:- |:- |
### **Agregar muestra de programación**
El fragmento de código a continuación muestra cómo hacer cada paso.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(AddingNewShape.class);  
//Load a diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get page by name
Page page = diagram.getPages().getPage("Page-2");

// Add master with stencil file path and master id
String masterName = "Rectangle";
// Add master with stencil file path and master name
diagram.addMaster(dataDir + "Basic Shapes.vss", masterName);
            
// page indexing starts from 0
int PageIndex = 1;
double width = 2, height = 2, pinX = 4.25, pinY = 4.5;
//Add a new rectangle shape
long rectangleId = diagram.addShape(pinX, pinY, width, height, masterName, PageIndex);
            
// set shape properties 
Shape rectangle = page.getShapes().getShape(rectangleId);
rectangle.getXForm().getPinX().setValue(5);
rectangle.getXForm().getPinY().setValue(5);
rectangle.setType(TypeValue.SHAPE);
rectangle.getText().getValue().add(new Txt("Aspose Diagram"));
rectangle.setTextStyle(diagram.getStyleSheets().get(3));
rectangle.getLine().getLineColor().setValue("#ff0000");
rectangle.getLine().getLineWeight().setValue(0.03);
rectangle.getLine().getRounding().setValue(0.1);
rectangle.getFill().getFillBkgnd().setValue("#ff00ff");
rectangle.getFill().getFillForegnd().setValue("#ebf8df");

diagram.save(dataDir + "AddShape_Out.vsdx", SaveFileFormat.VSDX);
System.out.println("Shape has been added.");

{{< /highlight >}}


{{% alert color="primary" %}}

 Agradecemos sus consultas y sugerencias en[Aspose.Diagram Foro](https://forum.aspose.com/c/diagram/17). Responderemos a la brevedad.

{{% /alert %}}
## **Recuperación de información de forma**
[Trabajar con diagramas](/diagram/es/java/working-with-diagrams/)explica cómo crear diagramas, agregar formas y conectores, y luego cómo recuperar información sobre diagram elementos como[paginas](/diagram/es/java/retrieve-get-copy-and-insert-a-page/), [maestros](https://docs.aspose.com/diagram/java/working-with-masters/), [conectores](https://reference.aspose.com/diagram/java/com.aspose.diagram/ConnectCollection) y[fuentes](https://reference.aspose.com/diagram/java/com.aspose.diagram/FontCollection). Este artículo analiza cómo recuperar información sobre formas en un diagram.

Cada forma en un diagram tiene una identificación y un nombre. El ID es importante al programar con Visio: es el método principal para acceder a una forma. Cada forma también retiene información sobre de qué maestro (plantilla) está hecha.

 A[Forma](http://www.aspose.com/api/java/diagram/com.aspose.diagram/shape) es un objeto en un dibujo Visio. La propiedad Shapes, expuesta por la clase Page, admite una colección de objetos Aspose.Diagram.Shape. La propiedad Shapes se puede utilizar para recuperar información sobre una forma.

En la ventana de la consola a continuación, por ejemplo, puede ver la salida de información para un diagram que contenía cuatro formas: dos terminadores, un proceso y un conector dinámico. Cada uno tiene una identificación única, así como el nombre de la forma maestra (plantilla).

|**Una ventana de consola que muestra información de forma**|
|:- |
|![todo:imagen_alternativa_texto](add-retrieve-copy-and-read-visio-shape-data_3.png)|
Para recuperar la información de la página Visio:

1. Carga un diagram.
1. Configura un bucle foreach para recorrer todas las formas en el diagram.
1. Muestra información de forma.
### **Recuperar muestra de programación**
El siguiente fragmento de código recupera la información de la forma de un Visio diagram.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(RetrieveShapeInfo.class);

//Load diagram
Diagram diagram = new Diagram(dataDir+ "RetrieveShapeInfo.vsd");

for (com.aspose.diagram.Shape shape : (Iterable<Shape>) diagram.getPages().getPage(0).getShapes())
{
    //Display information about the shapes
    System.out.println("\nShape ID : " + shape.getID());
    System.out.println("Name : " + shape.getName());
    System.out.println("Master Shape : " + shape.getMaster().getName());
}

{{< /highlight >}}


## **Copie formas de un Visio existente**
Aspose.Diagram for Java API permite a los desarrolladores copiar formas de la página de origen Visio a la nueva página Visio diagram. También admite la copia de formas de grupos. Este artículo describe cómo copiar todas las formas desde la página fuente diagram.

Para copiar formas, los desarrolladores también deben copiar los temas de origen PageSheet y origen Visio para conservar el estilo de relleno de forma y otras propiedades de formato.

Este ejemplo funciona de la siguiente manera:

1. Cargue una fuente Visio.
1. Inicializar un nuevo Visio
1. Agregue maestros y temas de la fuente Visio.
1. Obtenga la página de la fuente Visio.
1. Copie su hoja de página en la nueva página Visio.
1. Iterar a través de las formas de la página fuente Visio.
1. Establezca su nueva identificación y agréguela a la nueva página Visio.
1. Guarde el nuevo Visio en el almacenamiento local.
### **Ejemplo de programación de copias**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(CopyShape.class); 
// load a source Visio
Diagram srcVisio = new Diagram(dataDir + "Drawing1.vsdx");
        
// initialize a new Visio
Diagram newDiagram = new Diagram();

// add all masters from the source Visio diagram
MasterCollection originalMasters = srcVisio.getMasters();
for (Master master : (Iterable<Master>) originalMasters)
    newDiagram.addMaster(srcVisio, master.getName());

// get the page object from the original diagram
Page SrcPage = srcVisio.getPages().getPage("Page-1");
// copy themes from the source diagram
newDiagram.copyTheme(srcVisio);
// copy pagesheet of the source Visio page
newDiagram.getPages().get(0).getPageSheet().copy(SrcPage.getPageSheet());

// copy shapes from the source Visio page
for (Shape shape :(Iterable<Shape>) SrcPage.getShapes())
{
    newDiagram.getPages().get(0).getShapes().add(shape);
}
// save the new Visio
newDiagram.save(dataDir + "CopyShapes_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}



{{% alert color="primary" %}}

 Agradecemos sus consultas y sugerencias en[Aspose.Diagram Foro](https://forum.aspose.com/c/diagram/17). Responderemos a la brevedad.

{{% /alert %}}
## **Copie una forma Visio en otra instancia de forma**
El método Copy de la clase Shape toma una instancia de forma para clonar.

## **Lectura de datos de forma Visio**
 La colección Props expuesta por el[Forma](http://www.aspose.com/api/java/diagram/com.aspose.diagram/shape) la clase apoya la[Aspose.Diagram.Prop](http://www.aspose.com/api/java/diagram/com.aspose.diagram/prop) objeto. La propiedad se puede utilizar para leer los datos de una forma (propiedades personalizadas).
### **Leer todas las propiedades de forma**
Para identificar propiedades personalizadas en Microsoft Visio:

1. En un diagram, haga clic derecho en una forma.
1.  Seleccione**Datos** , después**Datos de forma** del menú.
 Todas las propiedades existentes se enumeran en el cuadro de diálogo.

|**Los datos de una forma, como se ve en Microsoft Visio.**|** |
|:- |:- |
|![todo:imagen_alternativa_texto](add-retrieve-copy-and-read-visio-shape-data_4.png)||


|**Una ventana de consola que muestra la salida de datos de forma.**|** |
|:- |:- |
|![todo:imagen_alternativa_texto](add-retrieve-copy-and-read-visio-shape-data_5.png)||
#### **Leer muestra de programación**
Los fragmentos de código a continuación leen datos de formas (propiedades personalizadas).


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ReadAllShapeProps.class);  

// call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get page by name
Page page = diagram.getPages().getPage("Page-3");

for (Shape shape :(Iterable<Shape>) page.getShapes())
{
    if (shape.getName() == "Process1")
    {
        for (Prop property :(Iterable<Prop>) shape.getProps())
        {
            System.out.println(property.getLabel().getValue() + ": " + property.getValue().getVal());
        }
        break;
    }
}

{{< /highlight >}}


### **Leer una propiedad de forma por nombre**
El fragmento de código siguiente lee una propiedad de forma por nombre (propiedad personalizada).
#### **Ejemplo de programación de lectura por nombre**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ReadShapePropByName.class);   
// call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get page by name
Page page = diagram.getPages().getPage("Page-3");

for (Shape shape :(Iterable<Shape>) page.getShapes())
{
    if (shape.getName() == "Process1")
    {
        Prop property = shape.getProps().getProp("Name1");
        System.out.println(property.getLabel().getValue() + ": " + property.getValue().getVal());
    }
}

{{< /highlight >}}


## **Usar índices de conexión para conectar formas**
Aspose.Diagram for Java API ya permite a los desarrolladores agregar nuevos puntos de conexión en la forma, y los desarrolladores ahora pueden conectar formas mediante índices de conexión.
### **Usar índices de conexión para conectar formas**
El miembro ConnectShapesViaConnectorIndex expuesto por el[Página](https://reference.aspose.com/diagram/java/com.aspose.diagram/page)La clase se puede usar para conectar formas usando índices de conexión.

1. Inicializar un nuevo dibujo.
1. Coloca cuatro formas rectangulares.
1. Agregue dos puntos de conexión adicionales, de modo que haya tres puntos de conexión en la línea del borde inferior
1. Conecte la primera forma de cada conexión inferior a otras tres formas rectangulares desde la parte superior con conectores dinámicos
1. Guardar dibujo
#### **Use índices de conexión para conectar formas Ejemplo de programación**
Use el siguiente código en su aplicación Java para conectar formas usando índices de conexión con Aspose.Diagram for Java API.

## **Recuperar la forma principal de una subforma**
Aspose.Diagram for Java permite a los desarrolladores recuperar la forma principal de una subforma.
### **Obtener la forma principal**
los[Forma](http://www.aspose.com/api/java/diagram/com.aspose.diagram/shape)La clase ofrece la propiedad ParentShape para recuperar la forma principal.
#### **Obtenga la muestra de programación de formas principales**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getSharedDataDir(RetrieveTheParentShape.class) + "Shapes\\";
		
// Call a Diagram class constructor to load the VSD diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get a sub-shape by page name, group shape ID, and then sub-shape ID
Shape shape = diagram.getPages().getPage("Page-3").getShapes().getShape(13).getShapes().getShape(2);
Shape parentShape = shape.getParentShape();
System.out.println("Parent Shape's Properties:");
System.out.println("Shape ID: " + parentShape.getID());
System.out.println("Shape Name: " + parentShape.getName());
System.out.println("Shape Type: " + parentShape.getType());
{{< /highlight >}}


