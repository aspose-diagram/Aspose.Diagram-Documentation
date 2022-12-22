---
title: Offentlig API Ändringar i Aspose.Diagram 17.01
type: docs
weight: 10
url: /sv/java/public-api-changes-in-aspose-diagram-17-01/
---
{{% alert color="primary" %}} 

Det här dokumentet beskriver ändringar av Aspose.Diagram API från version 16.12.0 till 17.01, som kan vara av intresse för modul-/applikationsutvecklare. Den innehåller inte bara nya och uppdaterade offentliga metoder, utan också en beskrivning av eventuella förändringar i beteendet bakom kulisserna i Aspose.Diagram.

{{% /alert %}} 
### **Konvertera Visio Rita med selektiva former**
Utvecklare kan välja specifika former för att konvertera Visio-ritningen till något annat format som stöds. Vi har lagt till Shapes-medlem i klassen RenderingSaveOptions för detta ändamål. Varje sparalternativklass är den utökade formen av RenderingSaveOptions-klassen. Kontrollera kodexemplet:

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
