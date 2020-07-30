---
title : "Working with Shapes Gluing" 
description : "" 
weight : 12031 
toc : false
type: docs
url: /java/developerguide/workingwithshapes/working+with+shapes+gluing/
---

# Aspose.Diagram for Java : Working with Shapes Gluing


{{< panel title="Contents Summary" style="primary" >}}
*   1 [Get the Connectors Glued to a Particular Shape](#get-the-connectors-glued-to-a-particular-shape)
    *   1.1 [Getting Glued Shapes](#getting-glued-shapes)
        *   1.1.1 [Get Connectors Glued Programming Sample](#get-connectors-glued-programming-sample)
*   2 [Glue Visio Shapes Together with Connection Point](#glue-visio-shapes-together-with-connection-point)
    *   2.1 [Glue Shapes](#glue-shapes)
        *   2.1.1 [Glue Visio Shapes Programming Sample](#glue-visio-shapes-programming-sample)
*   3 [Glue Shapes Inside the Container](#glue-shapes-inside-the-container)
    *   3.1 [Glue Group Shape](#glue-group-shape)
        *   3.1.1 [Glue Shapes Inside Programming Sample](#glue-shapes-inside-programming-sample)
{{< /panel >}}
 

 

## Get the Connectors Glued to a Particular Shape

[Add and Connect Visio Shapes](https://docs2.aspose.com/diagram/java/developerguide/technicalarticles/add+and+connect+visio+shapes) explains how to add a shape and connect it to other shapes in Microsoft Visio diagrams using Aspose.Diagram for Java. It is also possible to find connectors that are glued to this shape.

### Getting Glued Shapes

The `GluedShapes` method exposed by the [Shape](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/shape) class can be used to get a list of the IDs of all the connectors glued to a shape, or, if the shape in question is a connector, the IDs of the shapes it's connected to.The `GetShape` method, exposed by the [ShapeCollection](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/shapecollection) class, can then be used to find a shape by its ID.

The code below shows how to:

1.  Load a sample file.
2.  Access a particular shape.
3.  Get a list of IDs of all the connectors glued to this shape.

#### Get Connectors Glued Programming Sample

Use the following code in your Java application to find all the connectors glued to a shape using Aspose.Diagram for Java.

## Glue Visio Shapes Together with Connection Point

Aspose.Diagram for Java allows developers glue shapes together through the connection points.

### Glue Shapes

The `GlueShapes` method exposed by the [Page](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/page) class can be used.

**Input diagram**  
![](http://i.imgur.com/Z69f4hg.png)

**The diagram after gluing the shapes**  
![](http://i.imgur.com/5TJpDwc.png)

The code below shows how to:

1.  Load a sample file.
2.  Glue shapes.
3.  Save diagram.

#### Glue Visio Shapes Programming Sample

Use the following code in your Java application to glue shapes through the connection points:

## Glue Shapes Inside the Container

Aspose.Diagram for Java enables developers to glue group shapes inside a container.

### Glue Group Shape

The `GlueShapesInContainer` method exposed by the [Page](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/page) class can be used.

**Input diagram**  
![](http://i.imgur.com/HRRzIEh.png)

**The diagram after gluing the group shapes**  
![](http://i.imgur.com/YxCiOgU.png)

The code below shows how to:

1.  Load a sample file.
2.  Glue group shapes.
3.  Save diagram.

#### Glue Shapes Inside Programming Sample

Use the following code in your Java application to glue group shape inside a container:

## Attachments:

![](https://docs2.aspose.com/diagram/java/images/icons/bullet_blue.gif) [Glue Visio Shapes Through the Connection Points-01.png](https://docs2.aspose.com/diagram/java/attachments/18612700/18808963.png) (image/png)  
![](https://docs2.aspose.com/diagram/java/images/icons/bullet_blue.gif) [Glue Visio Shapes Through the Connection Points-02.png](https://docs2.aspose.com/diagram/java/attachments/18612700/18808962.png) (image/png)  
![](https://docs2.aspose.com/diagram/java/images/icons/bullet_blue.gif) [Glue Group Shapes Inside the Container\_01.png](https://docs2.aspose.com/diagram/java/attachments/18612700/18808961.png) (image/png)  
![](https://docs2.aspose.com/diagram/java/images/icons/bullet_blue.gif) [Glue Group Shapes Inside the Container\_02.png](https://docs2.aspose.com/diagram/java/attachments/18612700/18808960.png) (image/png)  

