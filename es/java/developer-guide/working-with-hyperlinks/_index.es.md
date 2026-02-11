---
title: Trabajar con hipervínculos
type: docs
weight: 110
url: /es/java/working-with-hyperlinks/
---
## **Agregar hipervínculo a una forma Visio**
Es un enfoque fácil agregar un hipervínculo a la forma Microsoft Visio dinámicamente.

En los dibujos de varias páginas Visio, los hipervínculos pueden moverlo de una página a otra. También puede vincular su dibujo a una página web o un archivo en su sistema.

Estas propiedades son expuestas por la[Forma](https://reference.aspose.com/diagram/java/com.aspose.diagram/Shape) la clase apoya la[com.aspose.diagram.Hyperlink](https://reference.aspose.com/diagram/java/com.aspose.diagram/hyperlink) objeto. El método add se puede usar para agregar datos de hipervínculo de una forma.

Para identificar propiedades en Microsoft Visio:

1. En un diagram, haga clic derecho en una forma.
1.  Seleccione**Hipervínculo**.
1. Establecer propiedades existentes
1.  Prensa**OK** botón

**Los datos del hipervínculo de una forma, como se ve en Microsoft Visio**

![todo:imagen_alternativa_texto](working-with-hyperlinks_1.png)

Los fragmentos de código a continuación agregan los datos del hipervínculo de la forma.
### **Agregar muestra de programación de hipervínculo**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(AddHyperlinkToShape.class);   
// load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get page by name
Page page = diagram.getPages().getPage("Page-1");
// get shape by ID
Shape shape = page.getShapes().getShape(2);

//initialize Hyperlink object
Hyperlink hyperlink = new Hyperlink();
//set address value
hyperlink.getAddress().setValue("http://www.google.com/");
//set sub address value
hyperlink.getSubAddress().setValue("Sub address here");
//set description value
hyperlink.getDescription().setValue("Description here");
//set name
hyperlink.setName("MyHyperLink");

//add hyperlink to the shape
shape.getHyperlinks().add(hyperlink);            
//save diagram to local space
diagram.save(dataDir + "AddHyperlinkToShape_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Obtener datos de hipervínculos de las formas Visio**
 Es posible obtener los datos del hipervínculo de una forma de forma similar a como[leyendo Visio datos de forma]().

Los desarrolladores pueden recuperar todos los hipervínculos de una forma Visio de la misma manera que[leer Visio datos de forma]() usando[Aspose.Diagram for Java API](https://products.aspose.com/diagram/java/)

En los dibujos de varias páginas Visio, los hipervínculos pueden moverlo de una página a otra. También puede vincular su dibujo a una página web o un archivo en su sistema.

Estas propiedades son expuestas por la[Forma](https://reference.aspose.com/diagram/java/com.aspose.diagram/Shape) la clase apoya la[com.aspose.diagram.Hyperlink](https://reference.aspose.com/diagram/java/com.aspose.diagram/hyperlink)objeto. La propiedad se puede utilizar para leer los datos de hipervínculo de una forma.

Para identificar propiedades en Microsoft Visio:

1. En un diagram, haga clic derecho en una forma.
1.  Seleccione**Hipervínculo.**
 Todas las propiedades existentes se enumeran en el cuadro de diálogo.

**Los datos del hipervínculo de una forma, como se ve en Microsoft Visio**

![todo:imagen_alternativa_texto](working-with-hyperlinks_2.png)

**Una ventana de consola que muestra la salida de datos de forma**

![todo:imagen_alternativa_texto](working-with-hyperlinks_3.png)

Los fragmentos de código a continuación leen los datos del hipervínculo de la forma.
### **Obtener muestra de programación de hipervínculos**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(GetHyperlinks.class);  
// load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get page by name
Page page = diagram.getPages().getPage("Page-1");
// get shape by ID
Shape shape = page.getShapes().getShape(1);
// iterate through the hyperlinks
for (Hyperlink hyperlink :(Iterable<Hyperlink>) shape.getHyperlinks())
{
    System.out.println("Address: " + hyperlink.getAddress().getValue());
    System.out.println("Sub Address: " + hyperlink.getSubAddress().getValue());
    System.out.println("Description: " + hyperlink.getDescription().getValue());
}

{{< /highlight >}}

