---
title: Rotate, Change the Position and Connect Sub-Shapes
type: docs
weight: 60
url: /java/rotate-change-the-position-and-connect-sub-shapes/
---

## **Rotate a Shape with Suitable Angle**
Aspose.Diagram for Java allows you to rotate a shape to any angle. The SetAngle method exposed by the [Shape](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/shape) class can be used to rotate a shape to any desired angle. It takes a single parameter as an angle.
### **Rotate a Shape Programming Sample**
Use the following code in your Java application to rotate a shape using Aspose.Diagram for Java.

{{< gist "aspose-diagram" "92a05cb833bad6d60de2968c96b40ee4" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-RotateVisioShape-RotateVisioShape.java" >}}
## **Change the Position of a Shape**
The [Shape](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/shape) Class allows you to change the position of a shape. The connector line automatically adjusts when the shape is moved to a different position.

The Move and MoveTo methods, exposed by the [Shape](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/shape) class, support changing the position of a shape as a part of a group or not.
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

{{< gist "aspose-diagram" "92a05cb833bad6d60de2968c96b40ee4" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-MoveVisioShape-MoveVisioShape.java" >}}
## **Connect Sub-shapes of the Groups**
This topic elaborates how to connect two sub-shapes of two different group shapes in Microsoft Visio diagrams using Aspose.Diagram for Java.

The ConnectShapesViaConnector method exposed by the [Page](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/page) class can be used to connect the shapes by their IDs. The AddShape method, exposed by the [Diagram](http://www.aspose.com/api/java/diagram/com.aspose.diagram/index) class, can be used to add a shape.

|<p>**The input diagram** </p><p>![todo:image_alt_text](http://i.imgur.com/74rDby5.png)</p>|<p>**The diagram after the connection of sub-shapes** </p><p>![todo:image_alt_text](http://i.imgur.com/c387dZJ.png)</p>|
| :- | :- |
The code below shows how to:

1. Load a sample file.
1. Access a particular page.
1. Add dynamic connector shape to the selected page.
1. Connect sub-shapes
### **Connect Sub-shapes Programming Sample**
Use the following code in your Java application to connect the sub-shapes of two different group shapes using Aspose.Diagram for Java.

{{< gist "aspose-diagram" "92a05cb833bad6d60de2968c96b40ee4" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-ConnectVisioSubShapes-ConnectVisioSubShapes.java" >}}
## **Get the Shapes Connected to a Particular Shape**
[Add and Connect Visio Shapes](/diagram/java/add-and-connect-visio-shapes-html/) explains how to add a shape and connect it to other shapes in Microsoft Visio diagrams using Aspose.Diagram for Java. It is also possible to find shapes that are connected to a specific shape.

The ConnectedShapes method exposed by the [Shape](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/shape) class can be used to get the IDs of the shapes connected to a shape. The GetShape method, exposed by the [ShapeCollection](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/shapecollection) class, can then be used to find a shape by its ID.

The code below shows how to:

1. Load a sample file.
1. Access a particular shape.
1. Get the names of all of the shapes connected to the selected shape.
### **Get Shapes Programming Sample**
Use the following code in your Java application to find all the shapes connected to a specific shape using Aspose.Diagram for Java.

{{< gist "aspose-diagram" "92a05cb833bad6d60de2968c96b40ee4" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-GetAllConnectedShapes-GetAllConnectedShapes.java" >}}
