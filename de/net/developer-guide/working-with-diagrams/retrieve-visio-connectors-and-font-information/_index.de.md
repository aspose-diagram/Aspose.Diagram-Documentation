---
title: Rufen Sie Visio-Konnektoren und Schriftartinformationen ab
type: docs
weight: 20
url: /de/net/retrieve-visio-connectors-and-font-information/
description: In diesem Abschnitt wird erläutert, wie Sie visio-Konnektoren und Schriftartinformationen erhalten.
---
## **Abrufen von Connector-Informationen**
 Aspose.Diagram for .NET bietet Mechanismen zum Abrufen von Informationen – ID und Name – über[Seiten](/diagram/de/net/retrieve-2c-get-2c-copy-and-insert-a-page/) und[Meister](https://docs.aspose.com/diagram/net/working-with-masters/). Außerdem erhalten Sie Informationen zu Verbindungselementen, den Elementen, die Formen verbinden.

 Das[Verbinden](http://www.aspose.com/api/net/diagram/aspose.diagram/connect) -Objekt stellt einen Verbinder dar, der zwei Shapes auf einem Zeichenblatt Visio verbindet. Die Connects-Eigenschaft, verfügbar gemacht durch die[Buchseite](http://www.aspose.com/api/net/diagram/aspose.diagram/page) -Klasse unterstützt eine Sammlung von Aspose.Diagram.Connect-Objekten. Diese Eigenschaft kann verwendet werden, um ID- und Namensinformationen zu einem Connector abzurufen.
### **Programmierbeispiel**
Der folgende Codeabschnitt ruft die Informationen für die Connectors in einem diagram ab.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Diagrams();

// Call the diagram constructor to load diagram from a VSD file
Diagram vdxDiagram = new Diagram(dataDir + "RetrieveConnectorInfo.vsd");

foreach (Aspose.Diagram.Connect connector in vdxDiagram.Pages[0].Connects)
{
    // Display information about the Connectors
    Console.WriteLine("\nFrom Shape ID : " + connector.FromSheet);
    Console.WriteLine("To Shape ID : " + connector.ToSheet);
}

{{< /highlight >}}
```
## **Abrufen von Schriftinformationen**
 Aspose.Diagram verfügt über Mechanismen zum Abrufen von Informationen über die Elemente, aus denen diagram besteht[Seiten](/diagram/de/net/retrieve-2c-get-2c-copy-and-insert-a-page/), [Schablonen](https://docs.aspose.com/diagram/net/working-with-masters/), [Anschlüsse](/diagram/de/net/retrieving-connector-information/)und auch Schriftarten. Dieser Artikel zeigt, wie Sie herausfinden, welche Schriftarten in einer diagram verwendet werden.

 Das[Schriftart](http://www.aspose.com/api/net/diagram/aspose.diagram/font) Objekt stellt eine Schriftart dar, die entweder auf Text in einem Dokument angewendet wird oder zur Verwendung auf dem System verfügbar ist. Ein Font-Objekt ordnet einen Namen (z. B. „Arial“) der Schriftart-ID (z. B. 3) zu, die Microsoft Visio in einer Font-Zelle in einem Zeichenabschnitt einer Form speichert, die mit dieser Schriftart formatierten Text enthält. Schriftart-IDs können sich ändern, wenn ein Dokument auf verschiedenen Systemen geöffnet wird oder wenn Schriftarten installiert oder entfernt werden.
### **Abrufen des Font-Programmierbeispiels**
Der folgende Codeabschnitt ruft Schriftartinformationen von Visio diagram ab.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Diagrams();

// Call the diagram constructor to load diagram from a VSD file
Diagram vdxDiagram = new Diagram(dataDir + "RetrieveFontInfo.vsd");

foreach (Aspose.Diagram.Font font in vdxDiagram.Fonts)
{
    // Display information about the fonts
    Console.WriteLine(font.Name);
}

{{< /highlight >}}
```
### **Abrufen des Standardschriftverzeichnisses**
Aspose.Diagram for .NET API ermöglicht auch das Abrufen des Standardverzeichnispfads für Schriftarten mithilfe der Methode GetDefaultFontDir() der Klasse Diagram. Der folgende Codeabschnitt ruft das Standardverzeichnis für Schriftarten aus dem Verzeichnis Visio diagram ab.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Diagrams();

// Call the diagram constructor to load diagram from a VSD file
Diagram vdxDiagram = new Diagram(dataDir + "RetrieveFontInfo.vsd");
           
// Display font default directory
Console.WriteLine(vdxDiagram.GetDefaultFontDir());

{{< /highlight >}}
```
### **Unbenutzte Schriftarten erhalten**
{{% alert color="primary" %}}

Diese Methode wird von Version 19.6 oder höher unterstützt.

{{% /alert %}}

Aspose.Diagram for .NET API ermöglicht auch das Abrufen nicht verwendeter Schriftarten mithilfe der Methode GetUnusedStyles() der Klasse Diagram. Der folgende Codeabschnitt ruft nicht verwendete Schriftarten aus Visio diagram ab.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Diagrams();

// Call the diagram constructor to load diagram from a VSD file
Diagram vdxDiagram = new Diagram(dataDir + "Sample_UnusedFonts.vsdx");

// Get Unused Fonts 
StyleSheetCollection unused = vdxDiagram.GetUnusedStyles();

// Display unused fonts count 
Console.WriteLine(unused.Count);

{{< /highlight >}}
```
