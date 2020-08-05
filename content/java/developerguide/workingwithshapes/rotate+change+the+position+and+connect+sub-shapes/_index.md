---
title : "Rotate Change the Position and Connect Sub-Shapes" 
description : "" 
weight : 12036 
toc : false
type: docs
url: /java/developerguide/workingwithshapes/rotate+change+the+position+and+connect+sub-shapes/
---

# Aspose.Diagram for Java : Rotate, Change the Position and Connect Sub-Shapes


{{< panel title="Contents Summary" style="primary" >}}
*   1 [Rotate a Shape with Suitable Angle](#rotate-a-shape-with-suitable-angle)
    *   1.1 [Rotate a Shape Programming Sample](#rotate-a-shape-programming-sample)
*   2 [Change the Position of a Shape](#change-the-position-of-a-shape)
    *   2.1 [Change Position Programming Sample](#change-position-programming-sample)
*   3 [Connect Sub-shapes of the Groups](#connect-sub-shapes-of-the-groups)
    *   3.1 [Connect Sub-shapes Programming Sample](#connect-sub-shapes-programming-sample)
*   4 [Get the Shapes Connected to a Particular Shape](#get-the-shapes-connected-to-a-particular-shape)
    *   4.1 [Get Shapes Programming Sample](#get-shapes-programming-sample)
{{< /panel >}}
 

 

## Rotate a Shape with Suitable Angle

Aspose.Diagram for Java allows you to rotate a shape to any angle. The `SetAngle` method exposed by the [Shape](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/shape) class can be used to rotate a shape to any desired angle. It takes a single parameter as an angle.

### Rotate a Shape Programming Sample

Use the following code in your Java application to rotate a shape using Aspose.Diagram for Java.

## Change the Position of a Shape

The [Shape](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/shape) Class allows you to change the position of a shape. The connector line automatically adjusts when the shape is moved to a different position.

The Move and MoveTo methods, exposed by the [Shape](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/shape) class, support changing the position of a shape as a part of a group or not.  
The code examples in this article move a shape on the page.  
**Input diagram**  
![image](http://i.imgur.com/cThgWnB.png)  
**The diagram after the shape is moved**  
![image](http://i.imgur.com/Q3QByqe.png)

The process for moving a shape is:

1.  Load a diagram.
2.  Find a particular shape.
3.  Move shape to a different location
4.  Save the diagram.

### Change Position Programming Sample

The code snippet below shows how to move the shape. The code retrieves a Visio page by name and shape by ID 16, and moves its position.

## Connect Sub-shapes of the Groups

This topic elaborates how to connect two sub-shapes of two different group shapes in Microsoft Visio diagrams using Aspose.Diagram for Java.

The `ConnectShapesViaConnector` method exposed by the [Page](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/page) class can be used to connect the shapes by their IDs. The `AddShape` method, exposed by the [Diagram](http://www.aspose.com/api/java/diagram/com.aspose.diagram/index) class, can be used to add a shape.

**The input diagram**  
![image](http://i.imgur.com/74rDby5.png)

**The diagram after the connection of sub-shapes**  
![image](http://i.imgur.com/c387dZJ.png)

The code below shows how to:

1.  Load a sample file.
2.  Access a particular page.
3.  Add dynamic connector shape to the selected page.
4.  Connect sub-shapes

### Connect Sub-shapes Programming Sample

Use the following code in your Java application to connect the sub-shapes of two different group shapes using Aspose.Diagram for Java.

## Get the Shapes Connected to a Particular Shape

[Add and Connect Visio Shapes](https://docs2.aspose.com/diagram/java/developerguide/technicalarticles/add+and+connect+visio+shapes) explains how to add a shape and connect it to other shapes in Microsoft Visio diagrams using Aspose.Diagram for Java. It is also possible to find shapes that are connected to a specific shape.

The `ConnectedShapes` method exposed by the [Shape](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/shape) class can be used to get the IDs of the shapes connected to a shape. The `GetShape` method, exposed by the [ShapeCollection](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/shapecollection) class, can then be used to find a shape by its ID.

The code below shows how to:

1.  Load a sample file.
2.  Access a particular shape.
3.  Get the names of all of the shapes connected to the selected shape.

### Get Shapes Programming Sample

Use the following code in your Java application to find all the shapes connected to a specific shape using Aspose.Diagram for Java.

