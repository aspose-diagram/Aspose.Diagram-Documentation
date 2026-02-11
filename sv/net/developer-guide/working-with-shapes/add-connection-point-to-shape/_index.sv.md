---
title: Lägg till anslutningspunkt till form
type: docs
weight: 70
url: /sv/net/add-connection-point-to-shape/
description: Det här avsnittet förklarar hur du lägger till anslutningspunkt till en visio-form med Aspose.Diagram.
---
## **Lägg till anslutningspunkt till en form i Visio**
Det här ämnet utvecklar hur utvecklare kan lägga till anslutningspunkt till en visio-form med hjälp av Aspose.Diagram for .NET.
### **Lägg till anslutningspunkt**
 De[Anslutningar](https://reference.aspose.com/diagram/net/aspose.diagram/shape/properties/connections) objekt representerar anslutningssamlingen i[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) klass.

Koden nedan visar hur man:

1. Ladda ett prov diagram.
1. skaffa en viss sida.
1. få en speciell form.
1. ny anslutning
1.  ställ in egenskapen för anslutning
1. lägga till anslutning till formen
1. spara diagram
#### **Lägg till anslutningspunkt till form Programmeringsexempel**
Använd följande kod i din .NET-applikation för att lägga till anslutning till en form med Aspose.Diagram for .NET.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSD diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsd");

// Get a particular page
Page page = diagram.Pages.GetPage("Page-3");
// Get a dynamic connector type shape by id
Shape shape = page.Shapes.GetShape(18);
// Set dynamic connector appearance
shape.SetConnectorsType(ConnectorsTypeValue.StraightLines);

// Saving Visio diagram
diagram.Save(dataDir + "SetConnectorAppearance_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

