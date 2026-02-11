---
title: Recuperare un controllo ActiveX da un oggetto Shape per modificare le proprietà
type: docs
weight: 20
url: /it/net/retrieve-an-activex-control-from-a-shape-object-to-modify-properties/
description: Modificare le proprietà di un controllo activeX con la libreria Aspose.Diagram.
---
{{% alert color="primary" %}} 

Utilizzando Aspose.Diagram API, gli sviluppatori possono recuperare un controllo ActiveX da un oggetto forma Visio per impostarne tutte le proprietà disponibili.

{{% /alert %}} 
## **Recupera un esempio di programmazione di controlli ActiveX**
[Forma](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class offre la proprietà ActiveXControl che consente agli sviluppatori di recuperare un controllo ActiveX da un oggetto shape Visio. Gli sviluppatori possono eseguire il cast di un controllo ActiveX nella classe di controllo ActiveX appropriata e quindi impostarne tutte le proprietà disponibili.

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
