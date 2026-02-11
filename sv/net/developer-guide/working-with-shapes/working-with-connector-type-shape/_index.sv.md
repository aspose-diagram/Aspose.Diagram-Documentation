---
title: Arbeta med Connector Type Shape
type: docs
weight: 70
url: /sv/net/working-with-connector-type-shape/
description: Det här avsnittet förklarar hur du ställer in Connector Appearance med Aspose.Diagram.
---
## **Ställ in utseendet på kontakttypsformen i Visio**
Det här ämnet utvecklar hur utvecklare kan ändra utseendet på formen av dynamisk kontakttyp med hjälp av Aspose.Diagram for .NET.
### **Ställ in kontaktens utseende**
 SetConnectorsType-metoden exponerad av[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) klass kan användas för att ställa in utseendet på kontakttypens form.

Koden nedan visar hur man:

1. Ladda ett prov diagram.
1. skaffa en viss sida.
1. få en speciell kontaktform.
1. ställ in formens utseende.
1. spara diagram
#### **Ställ in kontaktens utseende Programmeringsexempel**
Använd följande kod i din .NET-applikation för att ställa in utseendet på kontakttypens form med Aspose.Diagram for .NET.

```
{{< highlight "csharp" >}}
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
```
## **Välj Omdirigeringsalternativ för Connector Shape**
 ConFixedCode-egenskapen exponerad av[Layout](http://www.aspose.com/api/net/diagram/aspose.diagram/layout) klass kan användas för att välja omdirigeringsalternativ. Layout-egenskapen, exponerad av[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) klass, kommer att användas.

Koden nedan visar hur man:

1. Ladda en exempelfil.
1. skaffa en viss sida.
1. få en speciell kontaktform.
1. ställ in alternativ för omdirigering.
1. spara diagram.
### **Välj Programmeringsexempel för omdirigeringsalternativ**
Använd följande kod i din .NET-applikation för att välja omdirigeringsalternativet för kontaktformen med Aspose.Diagram for .NET.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-3");

// Get a particular connector shape
Shape shape = page.Shapes.GetShape(18);
// Set reroute option
shape.Layout.ConFixedCode.Value = ConFixedCodeValue.NeverReroute;

// Save Visio diagram
diagram.Save(dataDir + "RerouteConnectors_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
