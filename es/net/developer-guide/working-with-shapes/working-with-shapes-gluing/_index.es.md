---
title: Trabajar con el pegado de formas
type: docs
weight: 40
url: /es/net/working-with-shapes-gluing/
description: Esta sección explica cómo obtener formas que se pegan a una forma particular con Aspose.Diagram.
---
## **Obtenga los conectores pegados a una forma particular**
[Agregar y conectar Visio Formas](https://docs.aspose.com/diagram/net/add-retrieve-copy-and-read-visio-shape-data/) explica cómo agregar una forma y conectarla a otras formas en diagramas Microsoft Visio usando Aspose.Diagram for .NET. También es posible encontrar conectores que están pegados a esta forma.
### **Conseguir formas pegadas**
 El método GluedShapes expuesto por el[Forma](http://www.aspose.com/api/net/diagram/aspose.diagram/shape)La clase se puede usar para obtener una lista de los ID de todos los conectores pegados a una forma o, si la forma en cuestión es un conector, los ID de las formas a las que está conectado. El método GetShape, expuesto por el[ShapeCollection](http://www.aspose.com/api/net/diagram/aspose.diagram/shapecollection) class, se puede usar para encontrar una forma por su ID.

El siguiente código muestra cómo:

1. Cargue un archivo de muestra.
1. Accede a una forma particular.
1. Obtenga una lista de ID de todos los conectores pegados a esta forma.
#### **Obtenga una muestra de programación pegada de conectores**
Use el siguiente código en su aplicación .NET para encontrar todos los conectores pegados a una forma usando Aspose.Diagram for .NET.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSD diagram
Diagram diagram = new Diagram(dataDir + "RetrieveShapeInfo.vsd");
// Get shape by an ID
Shape shape = diagram.Pages[0].Shapes.GetShape(90);
// Get all glued 1D shapes
long[] gluedShapeIds = shape.GluedShapes(GluedShapesFlags.GluedShapesAll1D, null, null);

// Display shape ID and name
foreach (long id in gluedShapeIds)
{
    shape = diagram.Pages[0].Shapes.GetShape(id);
    Console.WriteLine("ID: " + shape.ID + "\t\t Name: " + shape.Name);
}

{{< /highlight >}}

## **Pegue las formas Visio junto con el punto de conexión**
Aspose.Diagram for .NET permite a los desarrolladores unir formas a través de los puntos de conexión.
### **Formas de pegamento**
 El método GlueShapes expuesto por el[Página](http://www.aspose.com/api/net/diagram/aspose.diagram/page) Se puede usar la clase.

|<p>**Entrada diagram** </p><p>![todo:imagen_alternativa_texto](working-with-shapes-gluing_1.png)</p>|<p>**El diagram después de pegar las formas.** </p><p>![todo:imagen_alternativa_texto](working-with-shapes-gluing_2.png)</p>|
|:- |:- |
El siguiente código muestra cómo:

1. Cargue un archivo de muestra.
1. Pega formas.
1. Guardar diagram.
#### **Pegamento Visio Muestra de programación de formas**
Use el siguiente código en su aplicación .NET para pegar formas a través de los puntos de conexión:


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get a particular page
Page page = diagram.Pages.GetPage("Page-1");
// Set shape id
long shape1_ID = 7;
long shape2_ID = 494;
// Glue shapes
page.GlueShapes(shape1_ID, Aspose.Diagram.Manipulation.ConnectionPointPlace.Center, shape2_ID);

// Save diagram
diagram.Save(dataDir + "GlueVisioShapes_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Pegue las formas dentro del recipiente**
Aspose.Diagram for .NET permite a los desarrolladores pegar formas grupales dentro de un contenedor.
### **Forma de grupo de pegamento**
 El método GlueShapesInContainer expuesto por el[Página](http://www.aspose.com/api/net/diagram/aspose.diagram/page) Se puede usar la clase.

|<p>**Entrada diagram** </p><p>![todo:imagen_alternativa_texto](working-with-shapes-gluing_3.png)</p>|<p>**El diagram después de pegar las formas del grupo.** </p><p>![todo:imagen_alternativa_texto](working-with-shapes-gluing_4.png)</p>|
|:- |:- |
El siguiente código muestra cómo:

1. Cargue un archivo de muestra.
1. Pegue las formas del grupo.
1. Guardar diagram.
#### **Muestra de programación de formas de pegamento en el interior**
Use el siguiente código en su aplicación .NET para pegar la forma del grupo dentro de un contenedor:


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get a particular page
Page page = diagram.Pages.GetPage("Page-1");

// The ID of shape which is glue from Aspose.Diagram.Shape.
long shapeFromId = 779;
// The location on the first connection index where to glue
int shapeToBeginConnectionIndex = 72;
// The location on the end connection index where to glue
int shapeToEndConnectionIndex = 73;
// The ID of shape where to glue to Aspose.Diagram.Shape.
long shapeToId = 743;

// Glue shapes in container
page.GlueShapesInContainer(shapeFromId, shapeToBeginConnectionIndex, shapeToEndConnectionIndex, shapeToId);

// Glue shapes in container using connection name
// Page.GlueShapesInContainer(fasId, "U05L", "U05R", cabinetId1);

// Save diagram
diagram.Save(dataDir + "GlueContainerShape_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

