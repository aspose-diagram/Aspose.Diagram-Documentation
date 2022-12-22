---
title: Pubblico API Modifiche Aspose.Diagram 17.01
type: docs
weight: 10
url: /it/java/public-api-changes-in-aspose-diagram-17-01/
---
{{% alert color="primary" %}} 

Questo documento descrive le modifiche allo Aspose.Diagram API dalla versione 16.12.0 alla 17.01, che potrebbero interessare gli sviluppatori di moduli/applicazioni. Include non solo metodi pubblici nuovi e aggiornati, ma anche una descrizione di eventuali cambiamenti nel comportamento dietro le quinte in Aspose.Diagram.

{{% /alert %}} 
### **Converti Visio Disegno con forme selettive**
Gli sviluppatori possono selezionare forme specifiche per convertire il disegno Visio in qualsiasi altro formato supportato. Abbiamo aggiunto il membro Shapes nella classe RenderingSaveOptions per questo scopo. Ogni classe di opzione di salvataggio è la forma estesa della classe RenderingSaveOptions. Si prega di controllare l'esempio di codice:

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
