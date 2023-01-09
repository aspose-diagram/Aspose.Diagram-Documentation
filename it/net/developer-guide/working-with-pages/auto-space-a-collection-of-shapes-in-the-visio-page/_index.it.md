---
title: Spaziatura automatica una raccolta di forme nella pagina Visio
type: docs
weight: 30
url: /it/net/auto-space-a-collection-of-shapes-in-the-visio-page/
description: Questa sezione spiega come eseguire la spaziatura automatica di una raccolta di forme in una pagina visio con Aspose.Diagram.
---
## **Spaziatura automatica una raccolta di forme nella pagina Visio**
Con Aspose.Diagram for .NET API, gli sviluppatori possono spaziare automaticamente una raccolta di forme nel disegno Visio. Per ottenere ciò, la classe Page offre un membro AutoSpaceShapes che accetta i parametri ShapeCollection e AutoSpaceOptions. La classe AutoSpaceOptions permette di impostare distanze orizzontali e verticali.
### **Spaziatura automatica forme nella pagina**
Utilizzare il codice seguente nell'applicazione .NET per eseguire la spaziatura automatica di una raccolta di forme in qualsiasi pagina del disegno Visio.

**C#**

{{< highlight "java" >}}

 // load a Visio drawing

Diagram diagram = new Diagram(@"c:\temp\Drawing1.vsdx");

// get page of the Visio drawing

Aspose.Diagram.Page page = diagram.Pages.GetPage("Page-1");

// initialize auto space options

AutoSpaceOptions options = new AutoSpaceOptions();

// set horizontal and vertical distances

options.DistanceInHorizontal = 2;

options.DistanceInVertical = 2;

// set auto space 

page.AutoSpaceShapes(page.Shapes, options);

// save Visio drawing

diagram.Save(@"c:\temp\AutoSpaceShapes_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
