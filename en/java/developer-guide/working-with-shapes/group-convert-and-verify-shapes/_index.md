---
title: Group, Convert and Verify Shapes
type: docs
weight: 50
url: /java/group-convert-and-verify-shapes/
---

## **Group Multiple Shapes Together in the Visio Drawing**
Aspose.Diagram API allows developers in grouping shapes together to move them all at once. Each shape in a group maintains a unique identity and has its own set of properties. When we change the formatting of a group of shapes, it assigns the new property to each shape.
### **How to Group Shapes**
The Group method exposed by the ShapeCollection class can be used to group shapes together.

The code below shows how to:

1. Load a sample diagram.
1. initialized an array of the shapes
1. get a particular shape by id.
1. get another particular particular shape by id.
1. assign shapes to the array.
1. group shapes by calling the Group method.
1. save diagram
#### **Group Shapes Programming Sample**
Use the following code in your Java application to group shapes together using Aspose.Diagram for Java API.

```
{{< highlight "java" >}}
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
```
## **Convert a Visio Shape to Other File Formats**
Aspose.Diagram for Java API allows developers to convert a single Visio shape to any other supported file format. In this article, we remove all other Visio shapes from the page and customize page setting according to the source Shape size. 
### **Converting a Particular Visio Shape**
Developers can convert a Visio shape to PDF, HTML, Image, SVG, and SWF by [specifying the Visio save options]().
This example code work as follows:

1. Load a source Visio.
1. Get a particular page.
1. Remove the background page.
1. Build a hash table of all shapes holding the ids and names.
1. Iterate through the hash table
1. Remove all shapes from the Visio page, except the particular one.
1. Set the page size.
1. Save the Visio page in any supported file format.
#### **Convert Shape Programming Sample**
```
{{< highlight "java" >}}
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
```
### **Convert Visio Shape to PDF**
The ToPdf method of the Shape class allows to convert a shape into the PDF format.

{{< highlight java >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// save a shape in the PDF format

diagram.getPages().get(0).getShapes().getShape(59).toPdf(dataDir + "out.pdf");

{{< /highlight >}}
### **Convert Visio Shape to HTML**
The ToHTML method of the Shape class allows to convert a shape into the HTML format.

{{< highlight java >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

HTMLSaveOptions hs = new HTMLSaveOptions();

// save a shape in the PDF format

diagram.getPages().get(0).getShapes().getShape(59).toHTML(dataDir + "out.pdf", hs);

{{< /highlight >}}

{{% alert color="primary" %}} 

We welcome your queries and suggestions at [Aspose.Diagram Forum](https://forum.aspose.com/c/diagram/17). We'll reply promptly.

{{% /alert %}} 
## **Verify Whether Two Visio Shapes are Connected or Glued**
Aspose.Diagram for Java API allows developers to verify that the two Visio shapes are glued or connected. Previously, we have seen that how we can connect or glue two shapes in these help topics: [Add and Connect Visio Shapes](/diagram/java/add-and-connect-visio-shapes/) and [Glue Shapes Inside the Container](/diagram/java/working-with-shapes-gluing/).
### **Verification of the Connected or Glued Shapes**
The [Shape](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) class offers IsGlued and IsConnected properties to determine whether two shapes are glued or connected.
#### **Verification of Connected or Glued Shapes Programming Sample**
The following piece of code verifies whether two shapes are connected or glued.

```
{{< highlight "java" >}}
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
```
## **Verify Whether the Visio Shape is in a Group of Shapes**
Aspose.Diagram for Java API allows developers to verify that the Visio shape is in a group of shapes or not.
### **Verification of Shape in the Group of Shapes**
The Shape class offers IsInGroup properties to determine whether the Visio shape is in a group shape.
#### **Verification of Shape in the Group of Shapes Programming Sample**
The following piece of code verifies whether the shape is in a group shape.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getSharedDataDir(RetrieveTheParentShape.class) + "Shapes\\";
				
// Call a Diagram class constructor to load the VSD diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get a sub-shape by page name, group shape ID, and then sub-shape ID
Shape shape = diagram.getPages().getPage("Page-3").getShapes().getShape(13).getShapes().getShape(2);
System.out.println("Is it in a Group: " + shape.isInGroup());
{{< /highlight >}}
```

{{% alert color="primary" %}} 

We welcome your queries and suggestions at [Aspose.Diagram Forum](https://forum.aspose.com/c/diagram/17). We'll reply promptly.

{{% /alert %}}
