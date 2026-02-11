---
title: Working with Shapes Gluing
type: docs
weight: 10
url: /java/working-with-shapes-gluing/
---

## **Get the Connectors Glued to a Particular Shape**
[Add and Connect Visio Shapes](/diagram/java/add-and-connect-visio-shapes/) explains how to add a shape and connect it to other shapes in Microsoft Visio diagrams using Aspose.Diagram for Java. It is also possible to find connectors that are glued to this shape.
### **Getting Glued Shapes**
The GluedShapes method exposed by the [Shape](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) class can be used to get a list of the IDs of all the connectors glued to a shape, or, if the shape in question is a connector, the IDs of the shapes it's connected to.The GetShape method, exposed by the [ShapeCollection](https://reference.aspose.com/diagram/java/com.aspose.diagram/shapecollection/) class, can then be used to find a shape by its ID.

The code below shows how to:

1. Load a sample file.
1. Access a particular shape.
1. Get a list of IDs of all the connectors glued to this shape.
#### **Get Connectors Glued Programming Sample**
Use the following code in your Java application to find all the connectors glued to a shape using Aspose.Diagram for Java.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(GetGluedConnectors.class);   
// call a Diagram class constructor to load the VSD diagram
Diagram diagram = new Diagram(dataDir + "RetrieveShapeInfo.vsd");
// get shape by an ID
Shape shape = diagram.getPages().get(0).getShapes().getShape(90);
// get all glued 1D shapes
long[] gluedShapeIds = shape.gluedShapes(GluedShapesFlags.GLUED_SHAPES_ALL_1_D, null, null);

// display shape ID and name
for (long id : gluedShapeIds)
{
    shape = diagram.getPages().get(0).getShapes().getShape(id);
    System.out.println("ID: " + shape.getID() + "\t\t Name: " + shape.getName());
}

{{< /highlight >}}

## **Glue Visio Shapes Together with Connection Point**
Aspose.Diagram for Java allows developers glue shapes together through the connection points.
### **Glue Shapes**
The GlueShapes method exposed by the [Page](https://reference.aspose.com/diagram/java/com.aspose.diagram/page) class can be used.

|<p>**Input diagram** </p><p>![todo:image_alt_text](http://i.imgur.com/Z69f4hg.png)</p>|<p>**The diagram after gluing the shapes** </p><p>![todo:image_alt_text](http://i.imgur.com/5TJpDwc.png)</p>|
| :- | :- |
The code below shows how to:

1. Load a sample file.
1. Glue shapes.
1. Save diagram.
#### **Glue Visio Shapes Programming Sample**
Use the following code in your Java application to glue shapes through the connection points:


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(GlueVisioShapes.class);
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get a particular page
Page page = diagram.getPages().getPage("Page-1");
// set shape id
long shape1_ID = 7;
long shape2_ID = 494;
// Glue shapes
page.glueShapes(shape1_ID, ConnectionPointPlace.CENTER, shape2_ID);

// Save diagram
diagram.save(dataDir + "GlueVisioShapes_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Glue Shapes Inside the Container**
Aspose.Diagram for Java enables developers to glue group shapes inside a container.
### **Glue Group Shape**
The GlueShapesInContainer method exposed by the Page class can be used.

|<p>**Input diagram** </p><p>![todo:image_alt_text](http://i.imgur.com/HRRzIEh.png)</p>|<p>**The diagram after gluing the group shapes** </p><p>![todo:image_alt_text](http://i.imgur.com/YxCiOgU.png)</p>|
| :- | :- |
The code below shows how to:

1. Load a sample file.
1. Glue group shapes.
1. Save diagram.
#### **Glue Shapes Inside Programming Sample**
Use the following code in your Java application to glue group shape inside a container:


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(GlueContainerShape.class);   
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get a particular page
Page page = diagram.getPages().getPage("Page-1");

// The ID of shape which is glue from Aspose.Diagram.Shape.
long shapeFromId = 779;
// The location on the first connection index where to glue
int shapeToBeginConnectionIndex = 72;
// The location on the end connection index where to glue
int shapeToEndConnectionIndex = 73;
// The ID of shape where to glue to Aspose.Diagram.Shape.
long shapeToId = 743;

// Glue shapes in container
page.glueShapesInContainer(shapeFromId, shapeToBeginConnectionIndex, shapeToEndConnectionIndex, shapeToId);

// Glue shapes in container using connection name
// page.GlueShapesInContainer(fasId, "U05L", "U05R", cabinetId1);

// Save diagram
diagram.save(dataDir + "GlueContainerShape_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

