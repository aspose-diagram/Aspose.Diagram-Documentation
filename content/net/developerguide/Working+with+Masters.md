+++
title = "Working with Masters" 
description = "" 
weight = 8039 
+++

Aspose.Diagram for .NET : Working with Masters  

# Aspose.Diagram for .NET : Working with Masters


{{< panel title="Contents Summary" style="primary" >}}
*   1 [Retrieving Master Information](#WorkingwithMasters-RetrievingMasterInformation)
    *   1.1 [Retrieving Master Information Programming Sample](#WorkingwithMasters-RetrievingMasterInformationProgrammingSample)
*   2 [Add Master from the Stencil of Shapes](#WorkingwithMasters-AddMasterfromtheStencilofShapes)
    *   2.1 [Add Master](#WorkingwithMasters-AddMaster)
        *   2.1.1 [Add Master Programming Sample](#WorkingwithMasters-AddMasterProgrammingSample)
*   3 [Create Master from Scratch](#WorkingwithMasters-CreateMasterfromScratch)
    *   3.1 [Create Master Programming Sample](#WorkingwithMasters-CreateMasterProgrammingSample)
*   4 [Get a Master from the Visio File](#WorkingwithMasters-GetaMasterfromtheVisioFile)
    *   4.1 [Getting a Master Object by ID](#WorkingwithMasters-GettingaMasterObjectbyID)
        *   4.1.1 [Master Object by ID Programming Sample](#WorkingwithMasters-MasterObjectbyIDProgrammingSample)
    *   4.2 [Getting a Master Object by Name](#WorkingwithMasters-GettingaMasterObjectbyName)
        *   4.2.1 [Master Object by Name Programming Sample](#WorkingwithMasters-MasterObjectbyNameProgrammingSample)
*   5 [Check Presence of a Master in the Visio Drawing](#WorkingwithMasters-CheckPresenceofaMasterintheVisioDrawing)
    *   5.1 [Checking a Master Presence by ID](#WorkingwithMasters-CheckingaMasterPresencebyID)
        *   5.1.1 [Master Presence by ID Programming Sample](#WorkingwithMasters-MasterPresencebyIDProgrammingSample)
    *   5.2 [Checking a Master Presence by Name](#WorkingwithMasters-CheckingaMasterPresencebyName)
        *   5.2.1 [Master Presence by Name Programming Sample](#WorkingwithMasters-MasterPresencebyNameProgrammingSample)
{{< /panel >}}
 

 

## Retrieving Master Information

A shape master is another name for a Visio stencil. With Aspose.Diagram, it is possible to retrieve information about pages, connectors and also masters. This article explains how to get the ID and name from a diagram.

The [Master](http://www.aspose.com/api/net/diagram/aspose.diagram/master) object represents a [Shape](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) object's master in a diagram. The `Masters` property, exposed by the `Diagram` class, supports a collection of `Aspose.Diagram.Master` objects. This property can be used to retrieve the masters’ information that is, the master ID and name. Use the `Page.Shapes` property to determine which shape has been inherited by the master shape.

### Retrieving Master Information Programming Sample

The following piece of code retrieves the masters information from a diagram.

## Add Master from the Stencil of Shapes

A stencil is a collection of shapes associated with a particular Microsoft Office Visio template. With Aspose.Diagram, it is possible to add any shape master to a drawing from a stencil.

### Add Master

The [`Master`](http://www.aspose.com/api/net/diagram/aspose.diagram/master) object represents a [`Shape`](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) object's master in a diagram. The `AddMaster` method, exposed by the `Diagram` class, allows adding a master from a stencil. It offers the following four ways:

*   Stencil file path and master ID.
*   Stencil file path and master name.
*   Stencil file stream and master ID.
*   Stencil file stream and master name.
*   Add master to diagram from source diagram

#### Add Master Programming Sample

## Create Master from Scratch

Aspose.Diagram API allows to create a [Master](http://www.aspose.com/api/net/diagram/aspose.diagram/master) from scratch without any stencil, drawing or template. Developers can customize the creation of Master. The `AddMaster` method, exposed by the `Diagram` class, allows to add a master.

### Create Master Programming Sample

## Get a Master from the Visio File

Sometimes, developers need to get the details of a Visio drawing's master. The Aspose.Diagram API supports this feature.

Aspose.Diagram for .NET offers the [Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) class that represents a Visio drawing. The `Masters` property, exposed by the `Diagram` class, supports a collection of `Aspose.Diagram.Master` objects. This property can be used to retrieve a particular master's details. The `MasterCollection` class exposes the `GetMasterByName` and `GetMaster` methods which can be called to get a `Master` object.

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

Aspose.Diagram for .NET offers the [Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) class that represents a Visio drawing. The `Masters` property, exposed by the `Diagram` class, supports a collection of `Aspose.Diagram.Master` objects. This property can be used to check for the presence of a particular master. The `MasterCollection` class exposes the `IsExist` method which can be called with the master name or ID parameter.

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

![](https://docs2.aspose.com/diagram/net/images/icons/bullet_blue.gif) [Retrieving masters information-001.png](https://docs2.aspose.com/diagram/net/attachments/18350098/18547070.png) (image/png)  

