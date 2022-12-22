---
title: Working with Shapes Gluing
type: docs
weight: 10
url: /java/working-with-shapes-gluing/
---

## **Get the Connectors Glued to a Particular Shape**
[Add and Connect Visio Shapes](/diagram/java/add-and-connect-visio-shapes/) explains how to add a shape and connect it to other shapes in Microsoft Visio diagrams using Aspose.Diagram for Java. It is also possible to find connectors that are glued to this shape.
### **Getting Glued Shapes**
The GluedShapes method exposed by the [Shape](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) class can be used to get a list of the IDs of all the connectors glued to a shape, or, if the shape in question is a connector, the IDs of the shapes it's connected to.The GetShape method, exposed by the [ShapeCollection](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/shapecollection) class, can then be used to find a shape by its ID.

The code below shows how to:

1. Load a sample file.
1. Access a particular shape.
1. Get a list of IDs of all the connectors glued to this shape.
#### **Get Connectors Glued Programming Sample**
Use the following code in your Java application to find all the connectors glued to a shape using Aspose.Diagram for Java.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-Glue-GetGluedConnectors-GetGluedConnectors.java" >}}
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

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-Glue-GlueVisioShapes-GlueVisioShapes.java" >}}
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

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-Glue-GlueContainerShape-GlueContainerShape.java" >}}
