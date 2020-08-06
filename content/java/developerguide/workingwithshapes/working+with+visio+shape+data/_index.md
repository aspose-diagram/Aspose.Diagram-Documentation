---
title : "Working with Visio Shape Data" 
description : "" 
weight : 12033 
toc : false
type: docs
url: /java/developerguide/workingwithshapes/working+with+visio+shape+data/
---

# Aspose.Diagram for Java : Working with Visio Shape Data


{{< panel title="Contents Summary" style="primary" >}}
*   1 [Adding a New Shape in Visio](#adding-a-new-shape-in-visio)
    *   1.1 [Add Programming Sample](#add-programming-sample)
*   2 [Retrieving Shape Information](#retrieving-shape-information)
    *   2.1 [Retrieve Programming Sample](#retrieve-programming-sample)
*   3 [Copy Shapes from an Existing Visio](#copy-shapes-from-an-existing-visio)
    *   3.1 [Copy Programming Sample](#copy-programming-sample)
*   4 [Copy a Visio Shape to another Shape instance](#copy-a-visio-shape-to-another-shape-instance)
*   5 [Reading Visio Shape Data](#reading-visio-shape-data)
    *   5.1 [Read All Shape Properties](#read-all-shape-properties)
        *   5.1.1 [Read Programming Sample](#read-programming-sample)
    *   5.2 [Read a Shape Property by Name](#read-a-shape-property-by-name)
        *   5.2.1 [Read by Name Programming Sample](#read-by-name-programming-sample)
*   6 [Use Connection indexes to connect shapes](#use-connection-indexes-to-connect-shapes)
    *   6.1 [Use Connection indexes to connect shapes](#use-connection-indexes-to-connect-shapes)
        *   6.1.1 [Use connection indexes to connect shapes Programming Sample](#use-connection-indexes-to-connect-shapes-programming-sample)
*   7 [Retrieve the Parent Shape of a Sub-Shape](#retrieve-the-parent-shape-of-a-sub-shape)
    *   7.1 [Get the Parent Shape ](#get-the-parent-shape )
        *   7.1.1 [Get the Parent Shape Programming Sample](#get-the-parent-shape-programming-sample)
{{< /panel >}}
 

 

## Adding a New Shape in Visio

Aspose.Diagram for Java allows you to manipulate Microsoft Visio diagrams in different ways. One of the things you can do is add new shapes to a diagrams. Aspose.Diagram for Java lets you to add a new shape to a diagram. The added shape can also be customized using Aspose.Diagram for Java.

This topic describes how to add a new rectangle shape to a diagram.

Use Aspose.Diagram for Java's API to create new shapes and then add these shapes to a diagram's shapes collection.

To add a new shape:

1.  **Find the page** - Each Visio diagram contains a collection of pages. Developers may retrieve the page by page ID or Name and store the required page in the [Page](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/Page) class object.
2.  **Add the require Master of a Shape** - Each Visio diagram contains a collection of masters. Developers may add a Master (by ID or Name) from the existing stencil file (by direct path or file stream).
3.  **Add shape in the Visio diagram** - Developers can place a new shape in the Visio diagram by page index (starting from 0), master name, PinX, PinY, height (optional) and width (optional).
4.  **Set shape properties** - `AddShape` method of the Diagram class returns the shape ID. Developers can retrieve shape from a Visio diagram by using this ID, and then set its properties, e.g. color, position, alignment and text.

{{< table style="table-striped" >}}
|**The input diagram** |**The diagram with a shape added** |
|:----|:----|
|![image](18809114.png)|![image](18809118.png)|
{{< /table >}}

### Add Programming Sample

The code snippet below shows how to do each step.

We welcome your queries and suggestions at [Aspose.Diagram Forum](http://www.aspose.com/community/forums/aspose.diagram-for-java/489/showforum.aspx). We'll reply promptly.

## Retrieving Shape Information

[Working with Diagrams](https://docs2.aspose.com/diagram/java/developerguide/workingwithdiagrams/) explains how to create diagrams, add shapes and connectors, and then how to retrieve information about diagram elements such as [pages](https://docs2.aspose.com/diagram/java/developerguide/workingwithpages/retrieve+get+copy+and+insert+a+page), [masters](#), [connectors](/pages/createpage.action?spaceKey=diagramjava&title=Retrieving+Connector+Information&linkCreation=true&fromPageId=18612227) and [fonts](/pages/createpage.action?spaceKey=diagramjava&title=Retrieving+Font+Information&linkCreation=true&fromPageId=18612227). This article looks at how to retrieve information about shapes in a diagram.

Each shape in a diagram has an ID and a name. The ID is important when programming with Visio: it is the main method for accessing a shape. Each shape also retains information about what master (stencil) it is made from.

A [Shape](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/Shape) is an object in a Visio drawing. The `Shapes` property, exposed by the `Page` class, supports a collection of `Aspose.Diagram.Shape` objects. The `Shapes` property can be used to retrieve information about a shape.

In the console window below, for example, you can see information output for a diagram that contained four shapes: two terminators, a process and a dynamic connector. Each has a unique ID as well as the name of the master (stencil) shape.

**A console window showing shape information**

![image](18809117.png)

To retrieve Visio page information:

1.  Loads a diagram.
2.  Sets up a foreach loop to loop through all the shapes in the diagram.
3.  Displays shape information.

### Retrieve Programming Sample

The following piece of code retrieve the shape information from a Visio diagram.

## Copy Shapes from an Existing Visio

Aspose.Diagram for Java API allows developers to copy shapes from the source Visio page to the new Visio diagram page. It also supports copying group shapes. This article describes how to copy all shapes from the the source diagram page.

To copy shapes, developers should also copy source PageSheet and source Visio themes to preserve shape fill style and other formatting properties.

This example work as follows:

1.  Load a source Visio.
2.  Initialize a new Visio
3.  Add masters and themes from the source Visio.
4.  Get page from the source Visio.
5.  Copy its PageSheet to the new Visio Page.
6.  Iterate through the shapes of the source Visio page.
7.  Set its new id and add to the new Visio page.
8.  Save the new Visio in the local storage.

### Copy Programming Sample

We welcome your queries and suggestions at [Aspose.Diagram Forum](http://www.aspose.com/community/forums/aspose.diagram-for-java/489/showforum.aspx). We'll reply promptly.

## Copy a Visio Shape to another Shape instance

The copy method of the Shape class takes a shape instance to clone.

{{< code lang="cs" >}}
// import diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
Shape newShape = new Shape();
// copy diagram
newShape.copy(diagram.getPages().get(0).getShapes().get(0));
newShape.setID(3);
newShape.getXForm().getPinX().setValue(1);
newShape.getXForm().getPinY().setValue(1);
{{< /code >}}

## Reading Visio Shape Data

The `Props` collection exposed by the [Shape](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/Shape) class supports the [Aspose.Diagram.Prop](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/prop) object. The property can be used to read a shape's data (custom properties).

### Read All Shape Properties

To identify custom properties in Microsoft Visio:

1.  In a diagram, right-click a shape.
2.  Select **Data**, then **Shape Data** from the menu.  
    Any existing properties are listed in the dialog.

{{< table style="table-striped" >}}
|A shape's data, as seen in Microsoft Visio. |
|:----|
|![image](http://i.imgur.com/2loM7b0.png)|
{{< /table >}}

{{< table style="table-striped" >}}
|A console window showing the shape data output.|
|:----|
|![image](http://i.imgur.com/2loM7b0.png)|
{{< /table >}}

#### Read Programming Sample

The code snippets below reads shape data (custom properties).

### Read a Shape Property by Name

The code snippet below reads a shape property by name (custom property).

#### Read by Name Programming Sample

## Use Connection indexes to connect shapes

Aspose.Diagram for Java API already allows developers to add new connecting points on the shape, and developers can now connect shapes using connection indexes.

### Use Connection indexes to connect shapes

The `connectShapesViaConnectorIndex` member exposed by the [Page](https://apireference.aspose.com/java/diagram/com.aspose.diagram/Page) class can be used to connect shapes using connection indexes. The following code shows how to connect shapes:

1.  Initialize a new drawing.
2.  Place four rectangle shapes
3.  Add two additional connection points, so that there would be three connection points on the bottom border line
4.  Connect first shape from each bottom connection to other three rectangle shapes from Top with dynamic connectors
5.  Save drawing

#### Use connection indexes to connect shapes Programming Sample

Use the following code in your Java application to connect shapes using connection indexes with Aspose.Diagram for Java API.

**Java**

{{< code lang="java" >}}
// initialize a new drawing
Diagram diagram = new Diagram();
// get page by index
Page page = diagram.getPages().get(0);
// add masters
String connectorMaster = "Dynamic connector", rectangle = "Rectangle";
int pageNumber = 0;
double width = 2, height = 2, pinX = 4.25, pinY = 9.5;
diagram.addMaster("C:\\temp\\Basic Shapes.vss", rectangle);
diagram.addMaster("C:\\temp\\Basic Shapes.vss", connectorMaster);
// add shapes
long shape1_ID = diagram.addShape(4.5, 7, rectangle, pageNumber);
long shape2_ID = diagram.addShape(2.25, 4.5, rectangle, pageNumber);
long shape3_ID = diagram.addShape(4.5, 4.5, rectangle, pageNumber);
long shape4_ID = diagram.addShape(6.75, 4.5, rectangle, pageNumber);
// get shapes by ID
Shape shape1 = page.getShapes().getShape(shape1_ID);
Shape shape2 = page.getShapes().getShape(shape2_ID);
Shape shape3 = page.getShapes().getShape(shape3_ID);
Shape shape4 = page.getShapes().getShape(shape4_ID);
// add two more connection points
Connection connection1 = new Connection();
connection1.getX().getUfe().setF("Width*0.33");
connection1.getY().getUfe().setF("Height*0");
Connection connection3 = new Connection();
connection3.getX().getUfe().setF("Width*0.66");
connection3.getY().getUfe().setF("Height*0");
shape1.getConnections().add(connection1);
shape1.getConnections().add(connection3);
            
// add connector shapes
Shape connector1 = new Shape();
Shape connector2 = new Shape();
Shape connector3 = new Shape();
long connecter1Id = diagram.addShape(connector1, connectorMaster, 0);
long connecter2Id = diagram.addShape(connector2, connectorMaster, 0);
long connecter3Id = diagram.addShape(connector3, connectorMaster, 0);
// connect shapes by index of conneecting points
page.connectShapesViaConnectorIndex(shape1.getID(), 6, shape2.getID(), 3, connecter1Id);
page.connectShapesViaConnectorIndex(shape1.getID(), 1, shape3.getID(), 3, connecter2Id);
page.connectShapesViaConnectorIndex(shape1.getID(), 7, shape4.getID(), 3, connecter3Id);
// save drawing
diagram.save("C:\\temp\\Drawing1_out.vsdx", SaveFileFormat.VSDX);
{{< /code >}}

## Retrieve the Parent Shape of a Sub-Shape

Aspose.Diagram for Java allows developers to retrieve the parent shape of a sub-shape.

### Get the Parent Shape 

The [Shape](https://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/shape) class offers `getParentShape` property to retrieve the parent shape.

#### Get the Parent Shape Programming Sample

