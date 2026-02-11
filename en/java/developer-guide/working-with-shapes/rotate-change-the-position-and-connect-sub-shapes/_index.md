---
title: Rotate, Change the Position and Connect Sub-Shapes
type: docs
weight: 60
url: /java/rotate-change-the-position-and-connect-sub-shapes/
---

## **Rotate a Shape with Suitable Angle**
Aspose.Diagram for Java allows you to rotate a shape to any angle. The SetAngle method exposed by the [Shape](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) class can be used to rotate a shape to any desired angle. It takes a single parameter as an angle.
### **Rotate a Shape Programming Sample**
Use the following code in your Java application to rotate a shape using Aspose.Diagram for Java.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(RotateVisioShape.class); 
// call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get page by name
Page page = diagram.getPages().getPage("Page-3");
// get shape by id
Shape shape = page.getShapes().getShape(16);

// Add a shape and set the angle
shape.setAngle(190);

// Save diagram
diagram.save(dataDir + "RotateVisioShape_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Change the Position of a Shape**
The Shape Class allows you to change the position of a shape. The connector line automatically adjusts when the shape is moved to a different position.

The Move and MoveTo methods, exposed by the Shape class, support changing the position of a shape as a part of a group or not.
The code examples in this article move a shape on the page.
**Input diagram** 

![todo:image_alt_text](http://i.imgur.com/cThgWnB.png)


**The diagram after the shape is moved** 

![todo:image_alt_text](http://i.imgur.com/Q3QByqe.png)

The process for moving a shape is:

1. Load a diagram.
1. Find a particular shape.
1. Move shape to a different location
1. Save the diagram.
### **Change Position Programming Sample**
The code snippet below shows how to move the shape. The code retrieves a Visio page by name and shape by ID 16, and moves its position.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(MoveVisioShape.class);  
// call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get page by name
Page page = diagram.getPages().getPage("Page-3");
// get shape by id
Shape shape = page.getShapes().getShape(16);
// move shape from its position, it adds values in coordinates
shape.move(1, 1);

// save diagram
diagram.save(dataDir + "MoveVisioShape_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Connect Sub-shapes of the Groups**
This topic elaborates how to connect two sub-shapes of two different group shapes in Microsoft Visio diagrams using Aspose.Diagram for Java.

The ConnectShapesViaConnector method exposed by the [Page](https://reference.aspose.com/diagram/java/com.aspose.diagram/page) class can be used to connect the shapes by their IDs. The AddShape method, exposed by the [Diagram](https://reference.aspose.com/diagram/java) class, can be used to add a shape.

|<p>**The input diagram** </p><p>![todo:image_alt_text](http://i.imgur.com/74rDby5.png)</p>|<p>**The diagram after the connection of sub-shapes** </p><p>![todo:image_alt_text](http://i.imgur.com/c387dZJ.png)</p>|
| :- | :- |
The code below shows how to:

1. Load a sample file.
1. Access a particular page.
1. Add dynamic connector shape to the selected page.
1. Connect sub-shapes
### **Connect Sub-shapes Programming Sample**
Use the following code in your Java application to connect the sub-shapes of two different group shapes using Aspose.Diagram for Java.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ConnectVisioSubShapes.class);   
// set sub shape ids
long shapeFromId = 2;
long shapeToId = 4;

// load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// access a particular page
Page page = diagram.getPages().getPage("Page-3");
       
// initialize connector shape
Shape shape = new Shape();
shape.getLine().getEndArrow().setValue(4);
shape.getLine().getLineWeight().setValue(0.01388);

// add shape
long connecter1Id = diagram.addShape(shape, "Dynamic connector", page.getID());
// connect sub-shapes
page.connectShapesViaConnector(shapeFromId, ConnectionPointPlace.RIGHT, shapeToId, ConnectionPointPlace.LEFT, connecter1Id);
// save Visio drawing
diagram.save(dataDir + "ConnectVisioSubShapes_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Get the Shapes Connected to a Particular Shape**
[Add and Connect Visio Shapes](/diagram/java/add-and-connect-visio-shapes/) explains how to add a shape and connect it to other shapes in Microsoft Visio diagrams using Aspose.Diagram for Java. It is also possible to find shapes that are connected to a specific shape.

The ConnectedShapes method exposed by the [Shape](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) class can be used to get the IDs of the shapes connected to a shape. The GetShape method, exposed by the [ShapeCollection](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/shapecollection) class, can then be used to find a shape by its ID.

The code below shows how to:

1. Load a sample file.
1. Access a particular shape.
1. Get the names of all of the shapes connected to the selected shape.
### **Get Shapes Programming Sample**
Use the following code in your Java application to find all the shapes connected to a specific shape using Aspose.Diagram for Java.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(GetAllConnectedShapes.class);
// call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get shape by id
Shape shape = diagram.getPages().getPage("Page-3").getShapes().getShape(16);
// get connected shapes
long[] connectedShapeIds = shape.connectedShapes(ConnectedShapesFlags.CONNECTED_SHAPES_ALL_NODES, null);

for (long id : connectedShapeIds)
{
    shape = diagram.getPages().getPage("Page-3").getShapes().getShape(id);
    System.out.println("ID: " + shape.getID() + "\t\t Name: " + shape.getName());
}

{{< /highlight >}}

