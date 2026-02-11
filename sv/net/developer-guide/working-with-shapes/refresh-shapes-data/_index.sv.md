---
title: Uppdatera formdata
type: docs
weight: 40
url: /sv/net/refresh-shapes-data/
description: Det här avsnittet förklarar hur du uppdaterar formens data för en visio-form med Aspose.Diagram.
---
## **Uppdaterar formens position inklusive xform, anslutning och geom när du byter forms text eller annans**
 Metoden RefreshData exponerad av[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) klass kan användas för att uppdatera formens data

Koden nedan visar hur man:

1. Ladda en exempelfil.
1. Få tillgång till en viss form.
1. Uppdatera formens data.
### **Uppdatera Shapes data**
Använd följande kod i din .NET-applikation för att uppdatera en form med Aspose.Diagram for .NET.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load a Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-3");

// Get Shape
Shape shape = page.Shapes.GetShape(15);

// Refresh data
shape.RefreshData();

// Save visio diagram
diagram.Save(dataDir + "RefreshData_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}


