---
title: Öffentlich API Änderungen in Aspose.Diagram 17.01
type: docs
weight: 10
url: /de/net/public-api-changes-in-aspose-diagram-17-01/
---
{{% alert color="primary" %}} 

Dieses Dokument beschreibt Änderungen an Aspose.Diagram API von Version 16.12.0 zu 17.1.0, die für Modul-/Anwendungsentwickler von Interesse sein könnten. Es enthält nicht nur neue und aktualisierte öffentliche Methoden, sondern auch eine Beschreibung aller Änderungen im Verhalten hinter den Kulissen in Aspose.Diagram.

{{% /alert %}} 
## **Konvertieren Visio Zeichnen mit ausgewählten Formen**
Entwickler können bestimmte Formen auswählen, um die Zeichnung Visio in jedes andere unterstützte Format zu konvertieren. Wir haben hinzugefügt[Formen](http://www.aspose.com/api/net/diagram/aspose.diagram.saving/renderingsaveoptions/properties/shapes)Mitglied im[RenderingSaveOptions](http://www.aspose.com/api/net/diagram/aspose.diagram.saving/renderingsaveoptions)Klasse dazu. Jede Speicheroptionsklasse ist die erweiterte Form der RenderingSaveOptions-Klasse. Bitte überprüfen Sie das Codebeispiel:

**C#**

{{< highlight "csharp" >}}

 // the path to the documents directory.

string dataDir = RunExamples.GetDataDir_LoadSaveConvert();

// call the diagram constructor to load diagram from a VSD file

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// create an instance SVG save options class

SVGSaveOptions options = new SVGSaveOptions();

ShapeCollection shapes = options.Shapes;

// get shapes by page index and shape ID, and then add in the shape collection object

shapes.Add(diagram.Pages[0].Shapes.GetShape(1));

shapes.Add(diagram.Pages[0].Shapes.GetShape(2));

// save Visio drawing

diagram.Save(dataDir + "SelectiveShapes_out.svg", options);

{{< /highlight >}}
