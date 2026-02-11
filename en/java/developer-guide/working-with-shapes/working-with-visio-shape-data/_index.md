---
title: Working with Visio Shape Data
type: docs
weight: 30
url: /java/working-with-visio-shape-data/
---

## **Adding a New Shape in Visio**
Aspose.Diagram for Java allows you to manipulate Microsoft Visio diagrams in different ways. One of the things you can do is add new shapes to a diagrams. Aspose.Diagram for Java lets you to add a new shape to a diagram. The added shape can also be customized using Aspose.Diagram for Java.

This topic describes how to add a new rectangle shape to a diagram.

Use Aspose.Diagram for Java's API to create new shapes and then add these shapes to a diagram's shapes collection.

To add a new shape:

1. **Find the page** - Each Visio diagram contains a collection of pages. Developers may retrieve the page by page ID or Name and store the required page in the [Page](https://reference.aspose.com/diagram//java/com.aspose.diagram/page) class object.
1. **Add the require Master of a Shape** - Each Visio diagram contains a collection of masters. Developers may add a Master (by ID or Name) from the existing stencil file (by direct path or file stream).
1. **Add shape in the Visio diagram** - Developers can place a new shape in the Visio diagram by page index (starting from 0), master name, PinX, PinY, height (optional) and width (optional).
1. **Set shape properties** - AddShape method of the Diagram class returns the shape ID. Developers can retrieve shape from a Visio diagram by using this ID, and then set its properties, e.g. color, position, alignment and text.

|<p>**The input diagram** </p><p>![todo:image_alt_text](working-with-visio-shape-data_1.png)</p>|<p>**The diagram with a shape added** </p><p>![todo:image_alt_text](working-with-visio-shape-data_2.png)</p>|
| :- | :- |
### **Add Programming Sample**
The code snippet below shows how to do each step.

```
{{< highlight "java" >}}
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
```

{{% alert color="primary" %}}

We welcome your queries and suggestions at [Aspose.Diagram Forum](https://forum.aspose.com/c/diagram/17). We'll reply promptly.

{{% /alert %}}
## **Retrieving Shape Information**
[Working with Diagrams](/diagram/java/working-with-diagrams/) explains how to create diagrams, add shapes and connectors, and then how to retrieve information about diagram elements such as [pages](/diagram/java/retrieve-get-copy-and-insert-a-page/), [masters](/diagram/java/working-with-masters/), connectors and [fonts](/diagram/java/aspose-diagram-font-operations/). This article looks at how to retrieve information about shapes in a diagram.

Each shape in a diagram has an ID and a name. The ID is important when programming with Visio: it is the main method for accessing a shape. Each shape also retains information about what master (stencil) it is made from.

A [Shape](https://reference.aspose.com/diagram//java/com.aspose.diagram/shape) is an object in a Visio drawing. The Shapes property, exposed by the Page class, supports a collection of Aspose.Diagram.Shape objects. The Shapes property can be used to retrieve information about a shape.

In the console window below, for example, you can see information output for a diagram that contained four shapes: two terminators, a process and a dynamic connector. Each has a unique ID as well as the name of the master (stencil) shape.

**A console window showing shape information**

![todo:image_alt_text](working-with-visio-shape-data_3.png)

To retrieve Visio page information:

1. Loads a diagram.
1. Sets up a foreach loop to loop through all the shapes in the diagram.
1. Displays shape information.
### **Retrieve Programming Sample**
The following piece of code retrieve the shape information from a Visio diagram.

```
{{< highlight "java" >}}
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
```
## **Copy Shapes from an Existing Visio**
Aspose.Diagram for Java API allows developers to copy shapes from the source Visio page to the new Visio diagram page. It also supports copying group shapes. This article describes how to copy all shapes from the the source diagram page.

To copy shapes, developers should also copy source PageSheet and source Visio themes to preserve shape fill style and other formatting properties.

This example work as follows:

1. Load a source Visio.
1. Initialize a new Visio
1. Add masters and themes from the source Visio.
1. Get page from the source Visio.
1. Copy its PageSheet to the new Visio Page.
1. Iterate through the shapes of the source Visio page.
1. Set its new id and add to the new Visio page.
1. Save the new Visio in the local storage.
### **Copy Programming Sample**
```
{{< highlight "java" >}}
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
```

{{% alert color="primary" %}}

We welcome your queries and suggestions at [Aspose.Diagram Forum](https://forum.aspose.com/c/diagram/17). We'll reply promptly.

{{% /alert %}}
## **Copy a Visio Shape to another Shape instance**
The copy method of the Shape class takes a shape instance to clone.

{{< highlight java >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

Shape newShape = new Shape();

// copy diagram

newShape.copy(diagram.getPages().get(0).getShapes().get(0));

newShape.setID(3);

newShape.getXForm().getPinX().setValue(1);

newShape.getXForm().getPinY().setValue(1);

{{< /highlight >}}
## **Reading Visio Shape Data**
The Props collection exposed by the Shape class supports the [Aspose.Diagram.Prop](https://reference.aspose.com/diagram/java/com.aspose.diagram/prop) object. The property can be used to read a shape's data (custom properties).
### **Read All Shape Properties**
To identify custom properties in Microsoft Visio:

1. In a diagram, right-click a shape.
1. Select **Data**, then **Shape Data** from the menu.
   Any existing properties are listed in the dialog.

|**A shape's data, as seen in Microsoft Visio.**|** |
| :- | :- |
|![todo:image_alt_text](http://i.imgur.com/2loM7b0.png)| |


|**A console window showing the shape data output.**|** |
| :- | :- |
|![todo:image_alt_text](http://i.imgur.com/kmAKNrx.png)| |
#### **Read Programming Sample**
The code snippets below reads shape data (custom properties).

```
{{< highlight "java" >}}
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
```
### **Read a Shape Property by Name**
The code snippet below reads a shape property by name (custom property).
#### **Read by Name Programming Sample**
```
{{< highlight "java" >}}
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
```
## **Use Connection indexes to connect shapes**
Aspose.Diagram for Java API already allows developers to add new connecting points on the shape, and developers can now connect shapes using connection indexes.
### **Use Connection indexes to connect shapes**
The connectShapesViaConnectorIndex member exposed by the Page class can be used to connect shapes using connection indexes. The following code shows how to connect shapes:

1. Initialize a new drawing.
1. Place four rectangle shapes
1. Add two additional connection points, so that there would be three connection points on the bottom border line
1. Connect first shape from each bottom connection to other three rectangle shapes from Top with dynamic connectors
1. Save drawing
#### **Use connection indexes to connect shapes Programming Sample**
Use the following code in your Java application to connect shapes using connection indexes with Aspose.Diagram for Java API.

**Java**

{{< highlight java >}}

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

{{< /highlight >}}
## **Retrieve the Parent Shape of a Sub-Shape**
Aspose.Diagram for Java allows developers to retrieve the parent shape of a sub-shape.
### **Get the Parent Shape**
The Shape class offers getParentShape property to retrieve the parent shape.
#### **Get the Parent Shape Programming Sample**
```
{{< highlight "java" >}}
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
```
