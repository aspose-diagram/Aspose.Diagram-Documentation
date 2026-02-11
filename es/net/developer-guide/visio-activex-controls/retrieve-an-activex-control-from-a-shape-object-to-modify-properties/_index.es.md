---
title: Recuperar un control ActiveX de un objeto de forma para modificar propiedades
type: docs
weight: 20
url: /es/net/retrieve-an-activex-control-from-a-shape-object-to-modify-properties/
description: Modifique las propiedades de un control ActiveX con la biblioteca Aspose.Diagram.
---
{{% alert color="primary" %}} 

Con Aspose.Diagram API, los desarrolladores pueden recuperar un control ActiveX de un objeto de forma Visio para configurar todas sus propiedades disponibles.

{{% /alert %}} 
## **Recuperar una muestra de programación de control ActiveX**
[Forma](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class ofrece la propiedad ActiveXControl que permite a los desarrolladores recuperar un control ActiveX de un objeto de forma Visio. Los desarrolladores pueden convertir un control ActiveX en la clase de control ActiveX adecuada y luego establecer todas sus propiedades disponibles.

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
