+++
title = "Public API Changes in Aspose.Diagram 6.8.0" 
description = "" 
weight = 20073 
+++

Aspose.Diagram for .NET : Public API Changes in Aspose.Diagram 6.8.0  

# Aspose.Diagram for .NET : Public API Changes in Aspose.Diagram 6.8.0


This document describes changes to the Aspose.Diagram API from version 6.6.0 to 6.8.0, that may be of interest to module/application developers. It includes not only new and updated public methods, but also a description of any changes in the behavior behind the scenes in Aspose.Diagram.

### Insert an ActiveX Control

Developers may insert an ActiveX control in the Visio diagram. We have added `AddActiveXControl` method in the [Page](http://www.aspose.com/api/net/diagram/aspose.diagram/page) class. Please check this code example:

**C#**

{{< code lang="c#" >}}
// load an existing Visio diagram
Diagram diagram = new Diagram();
// insert an ActiveX control
diagram.Pages[0].AddActiveXControl(ControlType.Image, 1, 1, 1, 1);
// save diagram
diagram.Save(@"C:\temp\MyOutput.vsdx", SaveFileFormat.VSDX);
{{< /code >}}

Error rendering macro 'code' : Invalid value specified for parameter lang

### Set the Color CheckBox of Layer

Developers can set or get the Color CheckBox of Layer using Aspose.Diagram API. Please check this code example:

**C#**

{{< code lang="c#" >}}
// Load source Visio diagram
Diagram diagram = new Diagram(@"c:\temp\Drawing1.vsdx");
// Get Visio page
Aspose.Diagram.Page page = diagram.Pages.GetPage("Page-1");

// Initialize a new Layer class object
Layer layer = new Layer();
// Set Layer name
layer.Name.Value = "Layer1";
// Set Layer Visibility
layer.Visible.Value = BOOL.True;
// set the color checkbox of Layer
layer.IsColorChecked = BOOL.True;

// Add Layer to the particular page sheet
page.PageSheet.Layers.Add(layer);

// Get shape by ID
Shape shape = page.Shapes.GetShape(3);
// Assign shape to this new Layer
shape.LayerMem.LayerMember.Value = layer.IX.ToString();
// Save diagram
diagram.Save(@"c:\temp\AddLayer_Out.vsdx", SaveFileFormat.VSDX);
{{< /code >}}

Error rendering macro 'code' : Invalid value specified for parameter lang

### Adds InheritFill Property in the Shape Class

Developers may get or set the inherit fill property. We have added `InheritFill` property in the `Shape` class. Please check this code example:

**C#**

{{< code lang="c#" >}}
// call the diagram constructor to load a VSDX diagram
Diagram diagram = new Diagram(@"c:\temp\Drawing1.vsdx");

// get page by ID
Page page = diagram.Pages.GetPage("Page-1");
// get shape by ID
Shape shape = page.Shapes.GetShape(1);
// get the fill formatting values
Console.WriteLine(shape.InheritFill.FillBkgnd.Value);
Console.WriteLine(shape.InheritFill.FillForegnd.Value);
Console.WriteLine(shape.InheritFill.FillPattern.Value);
{{< /code >}}

Error rendering macro 'code' : Invalid value specified for parameter lang

