---
title: Rufen Sie ein ActiveX-Steuerelement von einem Shape-Objekt ab, um Eigenschaften zu ändern
type: docs
weight: 20
url: /de/net/retrieve-an-activex-control-from-a-shape-object-to-modify-properties/
description: Ändern Sie die Eigenschaften eines ActiveX-Steuerelements mit der Bibliothek Aspose.Diagram.
---
{{% alert color="primary" %}} 

Mit Aspose.Diagram API können Entwickler ein ActiveX-Steuerelement aus einem Visio-Shape-Objekt abrufen, um alle verfügbaren Eigenschaften festzulegen.

{{% /alert %}} 
## **Rufen Sie ein Programmierbeispiel für ActiveX-Steuerelemente ab**
[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) -Klasse bietet die ActiveXControl-Eigenschaft, mit der Entwickler ein ActiveX-Steuerelement aus einem Visio-Shape-Objekt abrufen können. Entwickler können ein ActiveX-Steuerelement in die entsprechende ActiveX-Steuerelementklasse umwandeln und dann alle verfügbaren Eigenschaften festlegen.

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
