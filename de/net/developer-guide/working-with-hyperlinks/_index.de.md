---
title: Arbeiten mit Hyperlinks
type: docs
weight: 160
url: /de/net/working-with-hyperlinks/
description: In diesem Abschnitt wird erläutert, wie Sie einen Hyperlink in einem Visio-Shape mit Aspose.Diagram hinzufügen oder abrufen.
---
## **Hyperlink zu einer Visio-Form hinzufügen**
Microsoft Office Visio unterstützt das Hinzufügen der Hyperlinks zu jeder Form. Die Hyperlinks können auf eine andere Seite oder Form in der aktuellen Zeichnung, eine Seite oder Form in einer anderen Zeichnung, ein anderes Dokument als eine Visio-Zeichnung, eine Website, eine FTP-Site oder eine E-Mail-Adresse verweisen. Entwickler können Aspose.Diagram API verwenden, um ganz einfach Hyperlinks zu einer Visio-Form hinzuzufügen.

 In der mehrseitigen Visio-Zeichnung können Hyperlinks Sie von einer Form zu vielen anderen Arten von Links navigieren.[HyperlinkCollection](http://www.aspose.com/api/net/diagram/aspose.diagram/hyperlinkcollection) ausgesetzt durch die[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) Die Klasse bietet die Add-Methode, mit der der Hyperlink einer Form hinzugefügt werden kann.

Um Eigenschaften in Microsoft Office Visio zu identifizieren:

1. Klicken Sie in einem Visio diagram mit der rechten Maustaste auf eine Form.
1.  Auswählen**Hyperlinks.**
1. Legen Sie vorhandene Eigenschaften fest
1.  Drücken Sie**OK** Taste

**Die Hyperlinkdaten einer Form, wie in Microsoft Visio zu sehen**

![todo: Bild_alt_Text](working-with-hyperlinks_1.png)
### **Hyperlink-Programmierbeispiel hinzufügen**
Das folgende Code-Snippet fügt die Hyperlink-Daten der Form hinzu.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Hyperlinks();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-1");
// Get shape by ID
Shape shape = page.Shapes.GetShape(2);

// Initialize Hyperlink object
Hyperlink hyperlink = new Hyperlink();
// Set address value
hyperlink.Address.Value = "http:// Www.google.com/";
// Set sub address value
hyperlink.SubAddress.Value = "Sub address here";
// Set description value
hyperlink.Description.Value = "Description here";
// Set name
hyperlink.Name = "MyHyperLink";

// Add hyperlink to the shape
shape.Hyperlinks.Add(hyperlink);            
// Save diagram to local space
diagram.Save(dataDir + "AddHyperlinkToShape_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Holen Sie sich Hyperlink-Daten der Visio-Shapes**
Entwickler können alle Hyperlinks aus einem Visio-Shape auf die gleiche Weise abrufen wie sie[Visio Formdaten lesen](https://docs.aspose.com/diagram/net/load-or-create-a-visio-drawing/) verwenden[Aspose.Diagram for .NET API](https://products.aspose.com/diagram/net/).

In der mehrseitigen Visio-Zeichnung können Hyperlinks Sie von einer Form zu vielen anderen Arten von Links navigieren.[HyperlinkCollection](http://www.aspose.com/api/net/diagram/aspose.diagram/hyperlinkcollection) ausgesetzt durch die[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) -Klasse ermöglicht es Entwicklern, Hyperlinks abzurufen.

Um Eigenschaften in Microsoft Office Visio zu identifizieren:

1. Klicken Sie in einem diagram mit der rechten Maustaste auf eine Form.
1.  Auswählen**Hyperlinks.**

Alle vorhandenen Eigenschaften werden im Dialogfeld aufgelistet.
**Die Hyperlinkdaten einer Form, wie in Microsoft Visio zu sehen**

![todo: Bild_alt_Text](working-with-hyperlinks_1.png)

**Ein Konsolenfenster, das die Shape-Datenausgabe anzeigt**

![todo: Bild_alt_Text](working-with-hyperlinks_3.png)
### **Holen Sie sich das Hyperlinks-Programmierbeispiel**
Das folgende Code-Snippet liest die Hyperlink-Daten der Form.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Hyperlinks();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-1");
// Get shape by ID
Shape shape = page.Shapes.GetShape(1);
// Iterate through the hyperlinks
foreach (Aspose.Diagram.Hyperlink hyperlink in shape.Hyperlinks)
{
    Console.WriteLine("Address: " + hyperlink.Address.Value);
    Console.WriteLine("Sub Address: " + hyperlink.SubAddress.Value);
    Console.WriteLine("Description: " + hyperlink.Description.Value);
}       

{{< /highlight >}}
```
