---
title: Arbeiten mit Konnektortyp-Shape
type: docs
weight: 70
url: /de/net/working-with-connector-type-shape/
description: In diesem Abschnitt wird erläutert, wie Sie die Steckerdarstellung mit Aspose.Diagram festlegen.
---
## **Legen Sie das Erscheinungsbild der Verbindertypform in Visio fest**
In diesem Thema wird erläutert, wie Entwickler das Erscheinungsbild der Form des dynamischen Verbindungstyps mithilfe von Aspose.Diagram for .NET ändern können.
### **Legen Sie das Erscheinungsbild des Verbinders fest**
 Die SetConnectorsType-Methode, die von der bereitgestellt wird[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) -Klasse kann verwendet werden, um das Erscheinungsbild der Verbindertypform festzulegen.

Der folgende Code zeigt, wie man:

1. Laden Sie eine Probe diagram.
1. eine bestimmte Seite bekommen.
1. erhalten Sie eine bestimmte Steckerform.
1. Erscheinungsbild der Form festlegen.
1. außer diagram
#### **Programmierbeispiel für das Aussehen des Konnektors festlegen**
Verwenden Sie den folgenden Code in Ihrer .NET-Anwendung, um das Aussehen der Verbindertypform mithilfe von Aspose.Diagram for .NET festzulegen.


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

## **Wählen Sie die Umleitungsoption der Verbindungsform aus**
 Die ConFixedCode-Eigenschaft, die von der bereitgestellt wird[Layout](http://www.aspose.com/api/net/diagram/aspose.diagram/layout) Klasse kann verwendet werden, um die Umleitungsoption auszuwählen. Die Layout-Eigenschaft, verfügbar gemacht durch die[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) Klasse, verwendet werden.

Der folgende Code zeigt, wie man:

1. Laden Sie eine Beispieldatei.
1. eine bestimmte Seite bekommen.
1. erhalten Sie eine bestimmte Steckerform.
1. Umleitungsoptionen festlegen.
1. außer diagram.
### **Wählen Sie Programmierbeispiel für Umleitungsoption**
Verwenden Sie den folgenden Code in Ihrer .NET-Anwendung, um die Umleitungsoption der Verbinderform mit Aspose.Diagram for .NET auszuwählen.


{{< highlight csharp >}}
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

