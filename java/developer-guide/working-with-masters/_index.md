---
title: Working with Masters
type: docs
weight: 30
url: /java/working-with-masters/
---

## **Retrieving Master Information**
A shape master is another name for a Visio stencil. With Aspose.Diagram, it is possible to retrieve information about pages, connectors, and also masters. This article explains how to get the ID and name from a diagram.

The [Master](https://apireference.aspose.com/diagram/java/com.aspose.diagram/master) object represents a [Shape](https://apireference.aspose.com/diagram/java/com.aspose.diagram/shape) object's master in a diagram. The Masters property, exposed by the Diagram class, supports a collection of Aspose.Diagram.Master objects. This property can be used to retrieve the masters’ information that is, the master ID and name.

Use the Page.Shapes property to determine which shape has been inherited by the master shape.

**A console window showing the output from the code.** 

![todo:image_alt_text](http://i.imgur.com/DPn5sP9.png)
### **Retrieving Master Information Programming Sample**
The following piece of code retrieves the masters information from a diagram.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Masters-RetrieveMasterInfo-RetrieveMasterInfo.java" >}}
## **Add Master from the Stencil of Shapes**
A stencil is a collection of shapes associated with a particular Microsoft Office Visio template. With Aspose.Diagram, it is possible to add any shape master to a drawing from a stencil.
### **Add Master**
The Master object represents a Shape object's master in a diagram. The AddMaster method, exposed by the Diagram class, allows adding a master from a stencil. It offers the following four ways:

- Stencil file path and master ID.
- Stencil file path and master name.
- Stencil file stream and master ID.
- Stencil file stream and master name.
- Add master to diagram from source diagram
#### **Add Master Programming Sample**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Masters-AddMasterFromStencil-AddMasterFromStencil.java" >}}
## **Create Master from Scratch**
Aspose.Diagram API allows to create a Master from scratch without any stencil, drawing or template. Developers can customize the creation of Master. The addMaster method, exposed by the Diagram class, allows to add a master.
#### **Create Master Programming Sample**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Masters-CreateMasterfromScratch-CreateMasterfromScratch.java" >}}

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Masters-BASE64Encoder-BASE64Encoder.java" >}}
## **Get a Master from the Visio File**
Sometimes, developers need to get the details of a Visio drawing's master. The Aspose.Diagram API supports this feature.

Aspose.Diagram for Java offers the [Diagram](https://apireference.aspose.com/diagram/java/com.aspose.diagram/diagram) class that represents a Visio drawing. The Masters property, exposed by the Diagram class, supports a collection of Aspose.Diagram.Master objects. This property can be used to retrieve a particular master's details. The MasterCollection class exposes the GetMasterByName and GetMaster methods which can be called to get a Master object.
### **Getting a Master Object by ID**
This example work as follows:

1. Create an object of the Diagram class.
1. Call the Diagram.Masters class' GetMaster method.
#### **Master Object by ID Programming Sample**
The following example shows how to get a master by ID from a Visio drawing.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Masters-GetMasterbyID-GetMasterbyID.java" >}}
### **Getting a Master Object by Name**
This example work as follows:

1. Create an object of the Diagram class.
1. Call the Diagram.Masters class' GetMasterByName method.
#### **Master Object by Name Programming Sample**
The following example shows how to get a master object by name from a Visio drawing.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Masters-GetMasterbyName-GetMasterbyName.java" >}}
## **Check Presence of a Master in the Visio Drawing**
The Aspose.Diagram API supports checking for the presence of a master in a Visio drawing. With the MasterCollection property, developers can check to see if a master is present by its name or ID.

Aspose.Diagram for Java offers the [Diagram](https://apireference.aspose.com/diagram/java/com.aspose.diagram/diagram) class that represents a Visio drawing. The Masters property, exposed by the Diagram class, supports a collection of Aspose.Diagram.Master objects. This property can be used to check for the presence of a particular master. The MasterCollection class exposes the IsExist method which can be called with the master name or ID parameter.
### **Checking a Master Presence by ID**
This example work as follows:

1. Create an object of the Diagram class.
1. Call the Diagram.Masters class' IsExist method.
#### **Master Presence by ID Programming Sample**
The following example shows how to check presence of a master by ID in a Visio drawing.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Masters-CheckMasterPresencebyID-CheckMasterPresencebyID.java" >}}
### **Checking a Master Presence by Name**
This example work as follows:

1. Create an object of the Diagram class.
1. Call the Diagram.Masters class' IsExist method.
#### **Master Presence by Name Programming Sample**
The following example shows how to check a master presence by name from Visio drawing.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Masters-CheckMasterPresencebyName-CheckMasterPresencebyName.java" >}}
