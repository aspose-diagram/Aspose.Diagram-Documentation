---
title: Arbeiten mit Kopf- und Fußzeilen
type: docs
weight: 140
url: /de/net/working-with-headers-and-footers/
description: In diesem Abschnitt wird erläutert, wie Sie Kopf- und Fußzeilen von Microsoft Office Visio mit Aspose.Diagram festlegen.
---
## **Kopf- und Fußzeilen der Visio-Diagramme verwalten**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) bietet einen Mechanismus zum Festlegen von Kopf- und Fußzeilen der Microsoft Office Visio Diagramme. Entwickler können die Textzeichenfolge abrufen oder festlegen, die auf der linken, mittleren und rechten Seite einer Kopf-/Fußzeile eines Dokuments angezeigt wird. Sie können auch den Kopf- und Fußzeilenrand zusammen mit den Schriftarteigenschaften des Textes festlegen.
### **Festlegen der Eigenschaften von Kopf- und Fußzeilen**
 Das[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram)Das Klassenobjekt bietet die HeaderFooter-Eigenschaft, mit der Kopf- und Fußzeilentext, Schriftart und Randwerte abgerufen und festgelegt werden können. Während der Druckvorschau der Zeichnung Visio können Benutzer in Microsoft Visio 2013 auf die Linkschaltfläche "Kopf- und Fußzeile bearbeiten" klicken (in Microsoft Visio 2010 >> Schaltfläche "Kopf- und Fußzeile"). Es gibt einige Optionen zum Hinzufügen von Text, wie im folgenden Screenshot gezeigt. Benutzer können diese Eigenschaften programmgesteuert mit Aspose.Diagram API wie folgt verwalten:
#### **Programmierbeispiel**
Der folgende Codeabschnitt hilft bei der Verwaltung der Eigenschaften von Kopf- und Fußzeilen.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_HeadersAndFooters();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Add page number at the right corner of header
diagram.HeaderFooter.HeaderRight = "&p";

// Set text at the center
diagram.HeaderFooter.HeaderCenter = "Center of the header";

// Set text at the left side
diagram.HeaderFooter.HeaderLeft = "Left of the header";

// Add text at the right corner of footer
diagram.HeaderFooter.FooterRight = "Right of the footer";

// Set text at the center
diagram.HeaderFooter.FooterCenter = "Center of the footer";

// Set text at the left side
diagram.HeaderFooter.FooterLeft = "Left of the footer";

// Set header & footer color
diagram.HeaderFooter.HeaderFooterColor = Color.AliceBlue;

// Set text font properties
diagram.HeaderFooter.HeaderFooterFont.Italic = BOOL.True;
diagram.HeaderFooter.HeaderFooterFont.Underline = BOOL.False;

// Save Visio diagram
diagram.Save(dataDir + "ManageHeadersandFooters_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

