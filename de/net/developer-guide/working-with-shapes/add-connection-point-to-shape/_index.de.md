---
title: Verbindungspunkt zu Form hinzufügen
type: docs
weight: 70
url: /de/net/add-connection-point-to-shape/
description: In diesem Abschnitt wird erläutert, wie Sie einem visio-Shape einen Verbindungspunkt mit Aspose.Diagram hinzufügen.
---
## **Verbindungspunkt zu einer Form hinzufügen in Visio**
In diesem Thema wird erläutert, wie Entwickler einem visio-Shape mithilfe von Aspose.Diagram for .NET einen Verbindungspunkt hinzufügen können.
### **Verbindungspunkt hinzufügen**
 Das[Verbindungen](https://reference.aspose.com/diagram/net/aspose.diagram/shape/properties/connections) -Objekt stellt die Verbindungssammlung in der dar[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) Klasse.

Der folgende Code zeigt, wie man:

1. Laden Sie eine Probe diagram.
1. eine bestimmte Seite bekommen.
1. eine bestimmte Form bekommen.
1. neue Verbindung
1.  Legen Sie die Verbindungseigenschaft fest
1. Verbindung zur Form hinzufügen
1. außer diagram
#### **Fügen Sie einen Verbindungspunkt hinzu, um das Programmierbeispiel zu formen**
Verwenden Sie den folgenden Code in Ihrer .NET-Anwendung, um einer Form mithilfe von Aspose.Diagram for .NET eine Verbindung hinzuzufügen.


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

