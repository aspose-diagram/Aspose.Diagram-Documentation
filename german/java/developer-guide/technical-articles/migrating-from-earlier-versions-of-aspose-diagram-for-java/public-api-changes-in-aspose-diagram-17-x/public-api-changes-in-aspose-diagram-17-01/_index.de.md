---
title: Öffentlich API Änderungen in Aspose.Diagram 17.01
type: docs
weight: 10
url: /de/java/public-api-changes-in-aspose-diagram-17-01/
---
{{% alert color="primary" %}} 

Dieses Dokument beschreibt Änderungen an Aspose.Diagram API von Version 16.12.0 bis 17.01, die für Modul-/Anwendungsentwickler von Interesse sein könnten. Es enthält nicht nur neue und aktualisierte öffentliche Methoden, sondern auch eine Beschreibung aller Änderungen im Verhalten hinter den Kulissen in Aspose.Diagram.

{{% /alert %}} 
### **Konvertieren Visio Zeichnen mit ausgewählten Formen**
Entwickler können bestimmte Formen auswählen, um die Zeichnung Visio in jedes andere unterstützte Format zu konvertieren. Zu diesem Zweck haben wir das Shapes-Member in der RenderingSaveOptions-Klasse hinzugefügt. Jede Speicheroptionsklasse ist die erweiterte Form der RenderingSaveOptions-Klasse. Bitte überprüfen Sie das Codebeispiel:

**Java**

{{< highlight "csharp" >}}

 // The path to the documents directory.

String dataDir = Utils.getSharedDataDir(ConvertVisioWithSelectiveShapes.class) + "LoadSaveConvert\\";

// call the diagram constructor to load diagram from a VSD file

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// create an instance SVG save options class

SVGSaveOptions options = new SVGSaveOptions();

ShapeCollection shapes = options.getShapes();

// get shapes by page index and shape ID, and then add in the shape collection object

shapes.add(diagram.getPages().get(0).getShapes().getShape(1));

shapes.add(diagram.getPages().get(0).getShapes().getShape(2));

// save Visio drawing

diagram.save(dataDir + "SelectiveShapes_out.svg", options);

{{< /highlight >}}
