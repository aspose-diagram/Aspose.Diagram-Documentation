---
title: Öffentlich API Änderungen in Aspose.Diagram 5.8.0
type: docs
weight: 20
url: /de/java/public-api-changes-in-aspose-diagram-5-8-0/
---
{{% alert color="primary" %}} 

Dieses Dokument beschreibt Änderungen an Aspose.Diagram API von Version 5.7.0 auf 5.8.0, die für Modul-/Anwendungsentwickler von Interesse sein könnten. Es enthält nicht nur neue und aktualisierte öffentliche Methoden, sondern auch eine Beschreibung aller Änderungen im Verhalten hinter den Kulissen in Aspose.Diagram.

{{% /alert %}} 
### **SaveToolBar Option wird in HTMLSaveOptions hinzugefügt**
Die neue SaveToolBar-Option wurde der HTMLSaveOptions-Klasse hinzugefügt. Es gibt an, ob die Symbolleiste gespeichert werden soll oder nicht. Der Standardwert ist wahr. Beispielcodes:

**Java**

{{< highlight "java" >}}

 // initialize HTMLSaveOptions class object

HTMLSaveOptions opts = new HTMLSaveOptions();

// set save toolbar option

opts.setSaveToolBar(false);

{{< /highlight >}}
### **VSDX Speicheroption wurde im SaveFileFormat hinzugefügt**
Zuvor unterstützte Aspose.Diagram API das Lesen des Formats VSDX, aber jetzt haben wir Unterstützung für das Schreiben von Diagrammen im Format VSDX hinzugefügt. Beispielcodes:

**Java**

{{< highlight "java" >}}

 // save diagram in the VSDX format

diagram.save("C:\\temp\\Output.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
### **Group-Methode wurde in der ShapeCollection-Klasse hinzugefügt**
Entwickler können jetzt mehrere Formen in Visio diagram mit Aspose.Diagram API gruppieren. Beispielcodes:

**Java**

{{< highlight "java" >}}

 // load a Visio diagram

Diagram diagram = new Diagram("c:\\temp\\test.vsd");

// Initialize an array of shapes

Shape[]shapes = new Shape[2];

// extract and assign shapes to the array

shapes[0]= diagram.getPages().get(0).getShapes().getShape(1);

shapes[1]= diagram.getPages().get(0).getShapes().getShape(2);

// mark array shapes as group

diagram.getPages().get(0).getShapes().group(shapes);

// save visio diagram

diagram.save("c:\\temp\\out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
