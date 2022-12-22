---
title: Spaziatura automatica una raccolta di forme nella pagina Visio
type: docs
weight: 30
url: /it/java/auto-space-a-collection-of-shapes-in-the-visio-page/
---
## **Spaziatura automatica una raccolta di forme nella pagina Visio**
Con Aspose.Diagram for Java API, gli sviluppatori possono spaziare automaticamente una raccolta di forme nel disegno Visio. Per ottenere ciò, la classe Page offre un membro autoSpaceShapes che accetta i parametri ShapeCollection e AutoSpaceOptions. La classe AutoSpaceOptions permette di impostare distanze orizzontali e verticali.
### **Spaziatura automatica forme nella pagina**
Utilizzare il codice seguente nell'applicazione Java per eseguire la spaziatura automatica di una raccolta di forme in qualsiasi pagina del disegno Visio.

**Java**

{{< highlight "java" >}}

 // load a Visio drawing

Diagram diagram = new Diagram("c:\\temp\\Drawing1.vsdx");

// get page of the Visio drawing

Page page = diagram.getPages().getPage("Page-1");

// initialize auto space options

AutoSpaceOptions options = new AutoSpaceOptions();

// set horizontal and vertical distances

options.setDistanceInHorizontal(2);

options.setDistanceInVertical(2);

// set auto space 

page.autoSpaceShapes(page.getShapes(), options);

// save Visio drawing

diagram.save("c:\\temp\\AutoSpaceShapes_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
