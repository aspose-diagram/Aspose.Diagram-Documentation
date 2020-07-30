---
title : "Working with Masters" 
description : "" 
weight : 8021 
toc : false
type: docs
url: /java/developerguide/working+with+masters/
---

# Aspose.Diagram for Java : Working with Masters


{{< panel title="Contents Summary" style="primary" >}}
*   1 [Retrieving Master Information](#retrieving-master-information)
    *   1.1 [Retrieving Master Information Programming Sample](#retrieving-master-information-programming-sample)
*   2 [Add Master from the Stencil of Shapes](#add-master-from-the-stencil-of-shapes)
    *   2.1 [Add Master](#add-master)
        *   2.1.1 [Add Master Programming Sample](#add-master-programming-sample)
*   3 [Create Master from Scratch](#create-master-from-scratch)
    *   3.1 [Create Master Programming Sample](#create-master-programming-sample)
*   4 [Get a Master from the Visio File](#get-a-master-from-the-visio-file)
    *   4.1 [Getting a Master Object by ID](#getting-a-master-object-by-id)
        *   4.1.1 [Master Object by ID Programming Sample](#master-object-by-id-programming-sample)
    *   4.2 [Getting a Master Object by Name](#getting-a-master-object-by-name)
        *   4.2.1 [Master Object by Name Programming Sample](#master-object-by-name-programming-sample)
*   5 [Check Presence of a Master in the Visio Drawing](#check-presence-of-a-master-in-the-visio-drawing)
    *   5.1 [Checking a Master Presence by ID](#checking-a-master-presence-by-id)
        *   5.1.1 [Master Presence by ID Programming Sample](#master-presence-by-id-programming-sample)
    *   5.2 [Checking a Master Presence by Name](#checking-a-master-presence-by-name)
        *   5.2.1 [Master Presence by Name Programming Sample](#master-presence-by-name-programming-sample)
{{< /panel >}}
 

 

## Retrieving Master Information

A shape master is another name for a Visio stencil. With Aspose.Diagram, it is possible to retrieve information about pages, connectors and also masters. This article explains how to get the ID and name from a diagram.

The [Master](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/master) object represents a [Shape](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/shape) object's master in a diagram. The `Masters` property, exposed by the `Diagram` class, supports a collection of `Aspose.Diagram.Master` objects. This property can be used to retrieve the masters’ information that is, the master ID and name.

Use the `Page.Shapes` property to determine which shape has been inherited by the master shape.

**A console window showing the output from the code.**  
![](http://i.imgur.com/DPn5sP9.png)

### Retrieving Master Information Programming Sample

The following piece of code retrieves the masters information from a diagram.

## Add Master from the Stencil of Shapes

A stencil is a collection of shapes associated with a particular Microsoft Office Visio template. With Aspose.Diagram, it is possible to add any shape master to a drawing from a stencil.

### Add Master

The [`Master`](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/master) object represents a [`Shape`](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/shape) object's master in a diagram. The `AddMaster` method, exposed by the `Diagram` class, allows adding a master from a stencil. It offers the following four ways:

*   Stencil file path and master ID.
*   Stencil file path and master name.
*   Stencil file stream and master ID.
*   Stencil file stream and master name.
*   Add master to diagram from source diagram

#### Add Master Programming Sample

## Create Master from Scratch

Aspose.Diagram API allows to create a [Master](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/master) from scratch without any stencil, drawing or template. Developers can customize the creation of Master. The `addMaster` method, exposed by the `Diagram` class, allows to add a master.

#### Create Master Programming Sample

## Get a Master from the Visio File

Sometimes, developers need to get the details of a Visio drawing's master. The Aspose.Diagram API supports this feature.

Aspose.Diagram for Java offers the [Diagram](http://www.aspose.com/api/java/diagram/com.aspose.diagram/index) class that represents a Visio drawing. The `Masters` property, exposed by the `Diagram` class, supports a collection of `Aspose.Diagram.Master` objects. This property can be used to retrieve a particular master's details. The `MasterCollection` class exposes the `GetMasterByName` and `GetMaster` methods which can be called to get a `Master` object.

### Getting a Master Object by ID

This example work as follows:

1.  Create an object of the `Diagram` class.
2.  Call the `Diagram.Masters` class' `GetMaster` method.

#### Master Object by ID Programming Sample

The following example shows how to get a master by ID from a Visio drawing.

### Getting a Master Object by Name

This example work as follows:

1.  Create an object of the `Diagram` class.
2.  Call the `Diagram.Masters` class' `GetMasterByName` method.

#### Master Object by Name Programming Sample

The following example shows how to get a master object by name from a Visio drawing.

## Check Presence of a Master in the Visio Drawing

The Aspose.Diagram API supports checking for the presence of a master in a Visio drawing. With the `MasterCollection` property, developers can check to see if a master is present by its name or ID.

Aspose.Diagram for Java offers the [Diagram](http://www.aspose.com/api/java/diagram/com.aspose.diagram/index) class that represents a Visio drawing. The `Masters` property, exposed by the `Diagram` class, supports a collection of `Aspose.Diagram.Master` objects. This property can be used to check for the presence of a particular master. The `MasterCollection` class exposes the `IsExist` method which can be called with the master name or ID parameter.

### Checking a Master Presence by ID

This example work as follows:

1.  Create an object of the `Diagram` class.
2.  Call the `Diagram.Masters` class' `IsExist` method.

#### Master Presence by ID Programming Sample

The following example shows how to check presence of a master by ID in a Visio drawing.

### Checking a Master Presence by Name

This example work as follows:

1.  Create an object of the `Diagram` class.
2.  Call the `Diagram.Masters` class' `IsExist` method.

#### Master Presence by Name Programming Sample

The following example shows how to check a master presence by name from Visio drawing.

## Attachments:

![](https://docs2.aspose.com/diagram/java/images/icons/bullet_blue.gif) [Retrieve the masters information-001.png](https://docs2.aspose.com/diagram/java/attachments/18612733/18808904.png) (image/png)  

