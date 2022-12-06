---
title: Offentlig API Ändringar i Aspose.Diagram 17.01
type: docs
weight: 10
url: /sv/net/public-api-changes-in-aspose-diagram-17-01/
---
{{% alert color="primary" %}} 

Det här dokumentet beskriver ändringar av Aspose.Diagram API från version 16.12.0 till 17.1.0, som kan vara av intresse för modul-/applikationsutvecklare. Den innehåller inte bara nya och uppdaterade offentliga metoder, utan också en beskrivning av eventuella förändringar i beteendet bakom kulisserna i Aspose.Diagram.

{{% /alert %}} 
## **Konvertera Visio Rita med selektiva former**
Utvecklare kan välja specifika former för att konvertera Visio-ritningen till något annat format som stöds. Vi har lagt till[Former](http://www.aspose.com/api/net/diagram/aspose.diagram.saving/renderingsaveoptions/properties/shapes)medlem i[RenderingSaveOptions](http://www.aspose.com/api/net/diagram/aspose.diagram.saving/renderingsaveoptions)klass för detta ändamål. Varje sparalternativklass är den utökade formen av RenderingSaveOptions-klassen. Kontrollera kodexemplet:

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
