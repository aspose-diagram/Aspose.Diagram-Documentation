---
title : "Working with Shapes Gluing" 
description : "" 
weight : 12025 
toc : false
type: docs
url: /net/developerguide/workingwithshapes/working+with+shapes+gluing/
---

# Aspose.Diagram for .NET : Working with Shapes Gluing


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

[Add and Connect Visio Shapes](/pages/createpage.action?spaceKey=diagramnet&title=Add+and+Connect+Visio+Shapes&linkCreation=true&fromPageId=18350189) explains how to add a shape and connect it to other shapes in Microsoft Visio diagrams using Aspose.Diagram for .NET. It is also possible to find connectors that are glued to this shape.

### Getting Glued Shapes

The `GluedShapes` method exposed by the [Shape](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class can be used to get a list of the IDs of all the connectors glued to a shape, or, if the shape in question is a connector, the IDs of the shapes it's connected to.The `GetShape` method, exposed by the [ShapeCollection](http://www.aspose.com/api/net/diagram/aspose.diagram/shapecollection) class, can then be used to find a shape by its ID.

The code below shows how to:

1.  Load a sample file.
2.  Access a particular shape.
3.  Get a list of IDs of all the connectors glued to this shape.

#### Get Connectors Glued Programming Sample

Use the following code in your .NET application to find all the connectors glued to a shape using Aspose.Diagram for .NET.

## Glue Visio Shapes Together with Connection Point

Aspose.Diagram for .NET allows developers glue shapes together through the connection points.

### Glue Shapes

The `GlueShapes` method exposed by the [Page](http://www.aspose.com/api/net/diagram/aspose.diagram/page) class can be used.

**Input diagram**  
![image](18547240.png)

**The diagram after gluing the shapes**  
![image](18547243.png)

The code below shows how to:

1.  Load a sample file.
2.  Glue shapes.
3.  Save diagram.

#### Glue Visio Shapes Programming Sample

Use the following code in your .NET application to glue shapes through the connection points:

## Glue Shapes Inside the Container

Aspose.Diagram for .NET enables developers to glue group shapes inside a container.

### Glue Group Shape

The `GlueShapesInContainer` method exposed by the [Page](http://www.aspose.com/api/net/diagram/aspose.diagram/page) class can be used.

**Input diagram**  
![image](18547242.png)

**The diagram after gluing the group shapes**  
![image](18547241.png)

The code below shows how to:

1.  Load a sample file.
2.  Glue group shapes.
3.  Save diagram.

#### Glue Shapes Inside Programming Sample

Use the following code in your .NET application to glue group shape inside a container:

