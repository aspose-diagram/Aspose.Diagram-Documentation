---
title: Arbeiten mit Kopf- und Fußzeilen
type: docs
weight: 150
url: /de/java/working-with-headers-and-footers/
---
{{% alert color="primary" %}} 

Aspose.Diagram for Java bietet einen Mechanismus zum Setzen von Kopf- und Fußzeilen der Microsoft Office Visio Diagramme. Entwickler können die Textzeichenfolge abrufen oder festlegen, die auf der linken, mittleren und rechten Seite einer Kopf-/Fußzeile eines Dokuments angezeigt wird. Sie können auch den Kopf- und Fußzeilenrand zusammen mit den Schriftarteigenschaften des Textes festlegen.

{{% /alert %}} 
### **Festlegen der Eigenschaften von Kopf- und Fußzeilen**
 Das[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram)Das Klassenobjekt bietet die HeaderFooter-Eigenschaft, mit der Kopf- und Fußzeilentext, Schriftart und Randwerte abgerufen und festgelegt werden können. Während der Druckvorschau der Zeichnung Visio können Benutzer in Microsoft Visio 2013 auf die Linkschaltfläche "Kopf- und Fußzeile bearbeiten" klicken (in Microsoft Visio 2010 >> Schaltfläche "Kopf- und Fußzeile"). Es gibt einige Optionen zum Hinzufügen von Text, wie im folgenden Screenshot gezeigt. Benutzer können diese Eigenschaften programmgesteuert mit Aspose.Diagram API wie folgt verwalten:

**Verwalten Sie Kopf- und Fußzeilentext, Ränder und Schriftarteigenschaften.** 

![todo: Bild_alt_Text](working-with-headers-and-footers_1.png)

Der folgende Codeabschnitt hilft bei der Verwaltung der Eigenschaften von Kopf- und Fußzeilen.
#### **Programmierbeispiele**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ManageHeadersandFooters.class);
// call the diagram constructor to a load Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// add page number at the right corner of header
diagram.getHeaderFooter().setHeaderRight("&p");

// set text at the center
diagram.getHeaderFooter().setHeaderCenter("Center of the header");

// set text at the left side
diagram.getHeaderFooter().setHeaderLeft("Left of the header");

// add text at the right corner of footer
diagram.getHeaderFooter().setFooterRight("Right of the footer");

// set text at the center
diagram.getHeaderFooter().setFooterCenter("Center of the footer");

// set text at the left side
diagram.getHeaderFooter().setFooterLeft("Left of the footer");

// set header & footer color
diagram.getHeaderFooter().setHeaderFooterColor(Color.getRed());

// set text font properties
diagram.getHeaderFooter().getHeaderFooterFont().setItalic(BOOL.TRUE);
diagram.getHeaderFooter().getHeaderFooterFont().setUnderline(BOOL.FALSE);

// save Visio diagram
diagram.save(dataDir + "EditConnectorGeometry_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

