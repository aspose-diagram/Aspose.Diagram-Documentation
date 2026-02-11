---
title: Hämta en ActiveX-kontroll från ett Shape-objekt för att ändra egenskaper
type: docs
weight: 20
url: /sv/net/retrieve-an-activex-control-from-a-shape-object-to-modify-properties/
description: Ändra egenskaperna för en ActiveX-kontroll med Aspose.Diagram-biblioteket.
---
{{% alert color="primary" %}} 

Med hjälp av Aspose.Diagram API kan utvecklare hämta en ActiveX-kontroll från ett Visio-formobjekt för att ställa in alla tillgängliga egenskaper.

{{% /alert %}} 
## **Hämta ett ActiveX-kontrollprogrammeringsexempel**
[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class erbjuder ActiveXControl-egenskap som tillåter utvecklare att hämta en ActiveX-kontroll från ett Visio-formobjekt. Utvecklare kan casta en ActiveX-kontroll i lämplig ActiveX-kontrollklass och sedan ställa in dess alla tillgängliga egenskaper.


{{< highlight csharp >}}
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

