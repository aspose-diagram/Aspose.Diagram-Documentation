---
title: Aspose.Diagram for Java 17.12 Versionshinweise
type: docs
weight: 10
url: /de/java/aspose-diagram-for-java-17-12-release-notes/
---
{{% alert color="primary" %}} 

 Diese Seite enthält Versionshinweise für[Aspose.Diagram for Java 17.12](https://docs.aspose.com/diagram/java/aspose-diagram-for-java-17-12-release-notes/).

{{% /alert %}} 
## **Verbesserungen und Änderungen**

|**Taste**|**Zusammenfassung**|**Kategorie**|
|:- |:- |:- |
|DIAGRAMJAVA-50290|Geben Sie die einzelne API an, um eine Visio-Form in PDF zu konvertieren|Erweiterung|
|DIAGRAMJAVA-50291|Geben Sie die einzelne API an, um eine Visio-Form in HTML zu konvertieren|Erweiterung|
|DIAGRAMJAVA-50572|Die Shape.connectedShapes-Methode ruft keine ausgehenden Knoten ab|Erweiterung|
|DIAGRAMJAVA-50391|Die gespiegelten Bilder und Pfeile werden beim Konvertieren eines VSD in SVG generiert|Insekt|
|DIAGRAMJAVA-50570|VSD nach PDF - die zusätzlichen Textpositionen werden hinzugefügt|Insekt|
|DIAGRAMJAVA-50571|Import VSDX - Im Shape-Element ist ein Fehler aufgetreten|Insekt|
|DIAGRAMJAVA-50573|VSD zu SVG - die Linien einer Gruppenform fehlen|Insekt|
|DIAGRAMJAVA-50575|VSD zu SVG - die Textelemente fehlen|Insekt|
|DIAGRAMJAVA-50576|Die Prozedur „VDX importieren“ löst einen Seitenelementfehler aus|Insekt|
### **Fügt ein Copy-Mitglied in der Shape-Klasse hinzu**
Das Kopierelement verwendet eine Zielforminstanz als Parameter zum Klonen dieser Form.

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

Shape newShape = new Shape();

// copy diagram

newShape.copy(diagram.getPages().get(0).getShapes().get(0));

newShape.setID(3);

newShape.getXForm().getPinX().setValue(1);

newShape.getXForm().getPinY().setValue(1);

{{< /highlight >}}
### **Fügt ein toPdf-Member in der Shape-Klasse hinzu**
Das Mitglied toPdf konvertiert eine Form in das PDF-Format.

{{< highlight "java" >}}

 String dataDir = "C:\\temp\\";

// import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// save a shape in the PDF format

diagram.getPages().get(0).getShapes().getShape(59).toPdf(dataDir + "out.pdf");

{{< /highlight >}}
### **Fügt ein HTML-Member in der Shape-Klasse hinzu**
Das toHTML-Member wandelt eine Form in das PDF-Format um.

{{< highlight "java" >}}

 String dataDir = "C:\\temp\\";

// import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

HTMLSaveOptions hs = new HTMLSaveOptions();

// save a shape in the PDF format

diagram.getPages().get(0).getShapes().getShape(59).toHTML(dataDir + "out.pdf", hs);

{{< /highlight >}}
### **Anwendungsbeispiele**
Bitte überprüfen Sie die Liste der Hilfethemen, die in den Aspose.Diagram-Wiki-Dokumenten hinzugefügt wurden:

1. [Kopieren Sie eine Visio-Form in eine andere Forminstanz](https://docs.aspose.com/diagram/java/working-with-visio-shape-data/#use-connection-indexes-to-connect-shapes-programming-sample)
1. [Konvertieren Sie Visio Form in PDF](https://docs.aspose.com/diagram/java/convert-a-visio-shape-to-pdf/)
1. [Konvertieren Sie Visio Shape in HTML](https://docs.aspose.com/diagram/java/convert-a-visio-shape-to-html/)


