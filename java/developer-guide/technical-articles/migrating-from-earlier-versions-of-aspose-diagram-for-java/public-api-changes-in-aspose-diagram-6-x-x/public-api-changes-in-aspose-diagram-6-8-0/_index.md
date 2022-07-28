---
title: Public API Changes in Aspose.Diagram 6.8.0
type: docs
weight: 10
url: /java/public-api-changes-in-aspose-diagram-6-8-0/
---

{{% alert color="primary" %}} 

This document describes changes to the Aspose.Diagram API from version 6.7.0 to 6.8.0, that may be of interest to module/application developers. It includes not only new and updated public methods, but also a description of any changes in the behavior behind the scenes in Aspose.Diagram. 

{{% /alert %}} 
### **Insert an ActiveX Control**
Developers may insert an ActiveX control in the Visio diagram. We have added addActiveXControl method in the [Page](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/Page) class. Please check this code example:

**Java**

{{< highlight java >}}

 // load an existing Visio diagram

Diagram diagram = new Diagram();

// insert an ActiveX control

diagram.getPages().get(0).addActiveXControl(ControlType.IMAGE, 1, 1, 1, 1);

// save diagram

diagram.save("C:\\temp\\MyOutput.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
### **Set the Color CheckBox of Layer**
Developers can set or get the Color CheckBox of Layer using Aspose.Diagram API. Please check this code example:

**Java**

{{< highlight java >}}

 // Load source Visio diagram

Diagram diagram = new Diagram("c:\\temp\\Drawing1.vsdx");

// Get Visio page

Page page = diagram.getPages().getPage("Page-1");

// Initialize a new Layer class object

Layer layer = new Layer();

// set Layer name

layer.getName().setValue("Layer1");

// Set Layer Visibility

layer.getVisible().setValue(BOOL.TRUE);

// set the color checkbox of Layer

layer.setColorChecked(BOOL.TRUE);

// Add Layer to the particular page sheet

page.getPageSheet().getLayers().add(layer);

// get shape by ID

Shape shape = page.getShapes().getShape(3);

// assign shape to this new Layer

shape.getLayerMem().getLayerMember().setValue(Integer.toString(layer.getIX()));

// save diagram

diagram.save("c:\\temp\\AddLayer_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
### **Adds InheritFill Property in the Shape Class**
Developers may get or set the inherit fill property. We have added InheritFill property in the Shape class. Please check this code example:

**Java**

{{< highlight java >}}

 // call the diagram constructor to load a VSDX diagram

Diagram diagram = new Diagram("c:\\temp\\Drawing1.vsdx");

// get page by ID

Page page = diagram.getPages().getPage("Page-1");

// get shape by ID

Shape shape = page.getShapes().getShape(1);

// get the fill formatting values

System.out.println(shape.getInheritFill().getFillBkgnd().getValue());

System.out.println(shape.getInheritFill().getFillForegnd().getValue());

System.out.println(shape.getInheritFill().getFillPattern().getValue());

{{< /highlight >}}
