---
title: Retrieve an ActiveX Control from a Shape Object to Modify Properties
type: docs
weight: 20
url: /net/retrieve-an-activex-control-from-a-shape-object-to-modify-properties/
description: Modify properties of an activeX Control with Aspose.Diagram library.
---

{{% alert color="primary" %}} 

Using Aspose.Diagram API, developers can retrieve an ActiveX control from a Visio shape object to set its all available properties.

{{% /alert %}} 
## **Retrieve an ActiveX Control Programming Sample**
[Shape](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class offers ActiveXControl property which allows developers to retrieve an ActiveX control from a Visio shape object. Developers can cast an ActiveX control in the appropriate ActiveX control class, and then set its all available properties.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioActiveXControls();
// Load and get a Visio page by name
Diagram diagram = new Diagram(dataDir + "Drawing1.vsd");            
Page page = diagram.Pages.GetPage("Page-1");
// Get a shape by ID
Shape shape = page.Shapes.GetShape(1);
// Get an ActiveX control
CommandButtonActiveXControl cbac = (CommandButtonActiveXControl)shape.ActiveXControl;
// Set width, height and caption of the command button control
cbac.Width = 4;           
cbac.Height = 4;           
cbac.Caption = "Test Button";
// Save diagram
diagram.Save(dataDir + "RetrieveActiveXControl_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
