---
title : "Add Retrieve Copy and Read Visio Shape Data" 
description : "" 
weight : 12022 
toc : false
type: docs
url: /net/developerguide/workingwithshapes/add+retrieve+copy+and+read+visio+shape+data/
---

# Aspose.Diagram for .NET : Add, Retrieve, Copy and Read Visio Shape Data


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
    *   5.3 [Read InheritProps of Shape](#read-inheritprops-of-shape)
*   6 [Add and Connect Visio Shapes](#add-and-connect-visio-shapes)
    *   6.1 [Adding and Connecting Shapes](#adding-and-connecting-shapes)
        *   6.1.1 [Adding and Connecting Shapes Programming Sample](#adding-and-connecting-shapes-programming-sample)
*   7 [Use Connection indexes to connect shapes](#use-connection-indexes-to-connect-shapes)
    *   7.1 [Use Connection indexes to connect shapes](#use-connection-indexes-to-connect-shapes)
        *   7.1.1 [Use connection indexes to connect shapes Programming Sample](#use-connection-indexes-to-connect-shapes-programming-sample)
*   8 [Retrieve the Parent Shape of a Sub-Shape](#retrieve-the-parent-shape-of-a-sub-shape)
    *   8.1 [Get the Parent Shape ](#get-the-parent-shape )
        *   8.1.1 [Get the Parent Shape Programming Sample](#get-the-parent-shape-programming-sample)
{{< /panel >}}
 

 

## Adding a New Shape in Visio

Aspose.Diagram for .NET allows you to manipulate Microsoft Visio diagrams in different ways. One of the things you can do is add new shapes to a diagrams. Aspose.Diagram for .NET lets you to add a new shape to a diagram. The added shape can also be customized using Aspose.Diagram for .NET.

This topic describes how to add a new rectangle shape to a diagram.

Use Aspose.Diagram for .NET API to create new shapes and then add these shapes to a diagram's shapes collection.

To add a new shape:

1.  **Find the page** - Each Visio diagram contains a collection of pages. Developers may retrieve the page by page ID or Name and store the required page in the [Page](http://www.aspose.com/api/net/diagram/aspose.diagram/page) class object.
2.  **Add the require Master of a Shape** - Each Visio diagram contains a collection of masters. Developers may add a Master (by ID or Name) from the existing stencil file (by direct path or file stream).
3.  **Add shape in the Visio diagram** - Developers can place a new shape in the Visio diagram by page index (starting from 0), master name, PinX, PinY, height (optional) and width (optional).
4.  **Set shape properties** - `AddShape` method of the Diagram class returns the shape ID. Developers can retrieve shape from a Visio diagram by using this ID, and then set its properties, e.g. color, position, alignment and text.

{{< table style="table-striped" >}}
|**The input diagram**  |**The diagram with a shape added** |
|:---|:----|
|![image](18547041.png)|![image](18547021.png)|
{{< /table >}}

### Add Programming Sample

The code snippet below shows how to do each step.

![image](ri.png)We welcome your queries and suggestions at [Aspose.Diagram Forum](http://www.aspose.com/community/forums/aspose.diagram-for-.net/489/showforum.aspx). We'll reply promptly.

## Retrieving Shape Information

[Working with Diagrams](https://docs2.aspose.com/diagram/net/developerguide/workingwithdiagrams/) explains how to create diagrams, add shapes and connectors, and then how to retrieve information about diagram elements such as [pages](https://docs2.aspose.com/diagram/net/developerguide/workingwithpages/retrieve+get+copy+and+insert+a+page), [masters](http://www.aspose.com/docs/display/diagramnet/Working+with+Masters#WorkingwithMasters-RetrievingMasterInformation), [connectors](https://docs2.aspose.com/diagram/net/plugins/vsto/codecomparison/retrieving+connector+information) and [fonts](https://docs2.aspose.com/diagram/net/plugins/vsto/codecomparison/retrieving+font+information). This article looks at how to retrieve information about shapes in a diagram.

Each shape in a diagram has an ID and a name. The ID is important when programming with Visio: it is the main method for accessing a shape. Each shape also retains information about what master (stencil) it is made from.

A [Shape](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) is an object in a Visio drawing. The `Shapes` property, exposed by the `Page` class, supports a collection of `Aspose.Diagram.Shape` objects. The `Shapes` property can be used to retrieve information about a shape.

In the console window below, for example, you can see information output for a diagram that contained four shapes: two terminators, a process and a dynamic connector. Each has a unique ID as well as the name of the master (stencil) shape.

{{< table style="table-striped" >}}
|A console window showing shape information|
|:----|
|![image](18546689.png)|
{{< /table >}}

To retrieve Visio page information:

1.  Loads a diagram.
2.  Sets up a foreach loop to loop through all the shapes in the diagram.
3.  Displays shape information.

### Retrieve Programming Sample

The following piece of code retrieve the shape information from a Visio diagram.

## Copy Shapes from an Existing Visio

Aspose.Diagram for .NET API allows developers to copy shapes from the source Visio page to the new Visio diagram page. It also supports copying group shapes. This article describes how to copy all shapes from the the source diagram page.

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

![image](ri.png)We welcome your queries and suggestions at [Aspose.Diagram Forum](http://www.aspose.com/community/forums/aspose.diagram-for-.net/489/showforum.aspx). We'll reply promptly.

## Copy a Visio Shape to another Shape instance

The Copy method of the Shape class takes a shape instance to clone.

{{< code lang="cs" >}}
// import diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
Shape newShape = new Shape();
// copy diagram
newShape.Copy(diagram.Pages[0].Shapes[0]);
newShape.ID = 3;
newShape.XForm.PinX.Value = 1;
newShape.XForm.PinY.Value = 1;
{{< /code >}}

## Reading Visio Shape Data

The `Props` collection exposed by the [Shape](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class supports the [Aspose.Diagram.Prop](http://www.aspose.com/api/net/diagram/aspose.diagram/prop) object. The property can be used to read a shape's data (custom properties).

### Read All Shape Properties

To identify custom properties in Microsoft Visio:

1.  In a diagram, right-click a shape.
2.  Select **Data**, then **Shape Data** from the menu.  
    Any existing properties are listed in the dialog.

{{< table style="table-striped" >}}
|A shape's data, as seen in Microsoft Visio.|
|:----|
|![image](18547236.png)|
{{< /table >}}

{{< table style="table-striped" >}}
|A console window showing the shape data output.|
|:----|
|![image](18547237.png)|
{{< /table >}}

#### Read Programming Sample

The code snippets below reads shape data (custom properties).

### Read a Shape Property by Name

The code snippet below reads a shape property by name (custom property).

#### Read by Name Programming Sample

### Read InheritProps of Shape

The code snippet below reads InheritProps of a shape. 

## Add and Connect Visio Shapes

Aspose.Diagram for .NET allows you to add customized shapes and connect them in [diagrams you create](https://docs2.aspose.com/diagram/net/developerguide/workingwithdiagrams/create+update+layout+and+auto-fit+shapes).

### Adding and Connecting Shapes

The code in the samples below show how to:

1.  Create a diagram.
2.  Add and customize shapes (rectangle, star, hexagon).
3.  Connect the star and hexagon shapes to the rectangle.
4.  Save the diagram.

#### Adding and Connecting Shapes Programming Sample

## Use Connection indexes to connect shapes

Aspose.Diagram for .NET API already allows developers to add new connecting points on the shape, and developers can now connect shapes using connection indexes.

### Use Connection indexes to connect shapes

The `ConnectShapesViaConnectorIndex` member exposed by the [Page](https://apireference.aspose.com/net/diagram/aspose.diagram/page) class can be used to connect shapes using connection indexes. The following code shows how to connect shapes:

1.  Initialize a new drawing.
2.  Place four rectangle shapes
3.  Add two additional connection points, so that there would be three connection points on the bottom border line
4.  Connect first shape from each bottom connection to other three rectangle shapes from Top with dynamic connectors
5.  Save drawing

#### Use connection indexes to connect shapes Programming Sample

Use the following code in your .NET application to connect shapes using connection indexes with Aspose.Diagram for .NET API.

**C#**

{{< code lang="c#" >}}
// initialize a new drawing
Diagram diagram = new Diagram();
// get page by index
Aspose.Diagram.Page page = diagram.Pages[0];
// add masters
string connectorMaster = "Dynamic connector", rectangle = "Rectangle";
int pageNumber = 0;
double width = 2, height = 2, pinX = 4.25, pinY = 9.5;
diagram.AddMaster(@"C:\temp\Basic Shapes.vss", rectangle);
diagram.AddMaster(@"C:\temp\Basic Shapes.vss", connectorMaster);
// add shapes
long shape1_ID = diagram.AddShape(4.5, 7, rectangle, pageNumber);
long shape2_ID = diagram.AddShape(2.25, 4.5, rectangle, pageNumber);
long shape3_ID = diagram.AddShape(4.5, 4.5, rectangle, pageNumber);
long shape4_ID = diagram.AddShape(6.75, 4.5, rectangle, pageNumber);
// get shapes by ID
Aspose.Diagram.Shape shape1 = page.Shapes.GetShape(shape1_ID);
Aspose.Diagram.Shape shape2 = page.Shapes.GetShape(shape2_ID);
Aspose.Diagram.Shape shape3 = page.Shapes.GetShape(shape3_ID);
Aspose.Diagram.Shape shape4 = page.Shapes.GetShape(shape4_ID);
// add two more connection points
Connection connection1 = new Connection();
connection1.X.Ufe.F = "Width*0.33";
connection1.Y.Ufe.F = "Height*0";
Connection connection3 = new Connection();
connection3.X.Ufe.F = "Width*0.66";
connection3.Y.Ufe.F = "Height*0";
shape1.Connections.Add(connection1);
shape1.Connections.Add(connection3);
            
// add connector shapes
Aspose.Diagram.Shape connector1 = new Aspose.Diagram.Shape();
Aspose.Diagram.Shape connector2 = new Aspose.Diagram.Shape();
Aspose.Diagram.Shape connector3 = new Aspose.Diagram.Shape();
long connecter1Id = diagram.AddShape(connector1, connectorMaster, 0);
long connecter2Id = diagram.AddShape(connector2, connectorMaster, 0);
long connecter3Id = diagram.AddShape(connector3, connectorMaster, 0);
// connect shapes by index of conneecting points
page.ConnectShapesViaConnectorIndex(shape1.ID, 6, shape2.ID, 3, connecter1Id);
page.ConnectShapesViaConnectorIndex(shape1.ID, 1, shape3.ID, 3, connecter2Id);
page.ConnectShapesViaConnectorIndex(shape1.ID, 7, shape4.ID, 3, connecter3Id);
// save drawing
diagram.Save(@"C:\temp\Drawing1_out.vsdx", SaveFileFormat.VSDX);
{{< /code >}}

## Retrieve the Parent Shape of a Sub-Shape

Aspose.Diagram for .NET allows developers to retrieve the parent shape of a sub-shape.

### Get the Parent Shape 

The [Shape](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class offers `ParentShape` property to retrieve the parent shape.

#### Get the Parent Shape Programming Sample

