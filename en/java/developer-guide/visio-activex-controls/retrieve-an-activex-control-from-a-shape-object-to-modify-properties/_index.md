---
title: Retrieve an ActiveX Control from a Shape Object to Modify Properties
type: docs
weight: 20
url: /java/retrieve-an-activex-control-from-a-shape-object-to-modify-properties/
---

{{% alert color="primary" %}} 

Using Aspose.Diagram API, developers can retrieve an ActiveX control from a Visio shape object to set its all available properties.

{{% /alert %}} 
## **Retrieve an ActiveX Control Programming Sample**
[Shape](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) class offers getActiveXControl method which allows developers to retrieve an ActiveX control from a Visio shape object. Developers can cast an ActiveX control in the appropriate ActiveX control class, and then set its all available properties.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getSharedDataDir(RetrieveActiveXControl.class) + "VisioActiveXControls/";
// load a Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsd");
// get a Visio page by name
Page page = diagram.getPages().getPage("Page-1");
// get a shape by ID
Shape shape = page.getShapes().getShape(1);
// get an ActiveX control
CommandButtonActiveXControl cbac = (CommandButtonActiveXControl)shape.getActiveXControl();
// set width of the command button control
cbac.setWidth(4);
// set height of the command button control
cbac.setHeight(4);
// set caption of the command button control
cbac.setCaption("Test Button");
// save diagram
diagram.save(dataDir + "RetrieveActiveXControl_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

