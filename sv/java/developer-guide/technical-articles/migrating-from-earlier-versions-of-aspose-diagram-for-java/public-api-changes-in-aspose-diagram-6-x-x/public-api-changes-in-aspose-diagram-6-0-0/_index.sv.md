---
title: Offentlig API Ändringar i Aspose.Diagram 6.0.0
type: docs
weight: 50
url: /sv/java/public-api-changes-in-aspose-diagram-6-0-0/
---
{{% alert color="primary" %}} 

Det här dokumentet beskriver ändringar av Aspose.Diagram API från version 5.9.0 till 6.0.0, som kan vara av intresse för modul-/applikationsutvecklare. Den innehåller inte bara nya och uppdaterade offentliga metoder, utan också en beskrivning av eventuella förändringar i beteendet bakom kulisserna i Aspose.Diagram.

{{% /alert %}} 
### **isGlued Method läggs till i Shape-klassen**
Metoden isGlued tar ett formobjekt som en parameter för att avgöra om de två formerna är limmade eller inte.
Exempelkod:

**Java**

{{< highlight "java" >}}

 // Call the diagram constructor to load diagram

Diagram diagram = new Diagram("C:/temp/Drawing1.vsdx");

// get Visio page by name

Page page = diagram.getPages().getPage("Page-1");

// get Visio shapes by ids

Shape ShapedOne = page.getShapes().getShape(1);

Shape ShapedTwo = page.getShapes().getShape(2);

// determine whether shapes are glued

boolean glued = ShapedOne.isGlued(ShapedTwo);

{{< /highlight >}}
### **isConnected Method läggs till i Shape-klassen**
Metoden isConnected tar ett formobjekt som en parameter för att avgöra om de två formerna är kopplade eller inte.
Exempelkod:

**Java**

{{< highlight "java" >}}

 // Call the diagram constructor to load diagram

Diagram diagram = new Diagram("C:/temp/Drawing1.vsdx");

// get Visio page by name

Page page = diagram.getPages().getPage("Page-1");

// get Visio shapes by ids

Shape ShapedOne = page.getShapes().getShape(1);

Shape ShapedTwo = page.getShapes().getShape(2);

// determine whether shapes are connected

boolean connected = ShapedOne.isConnected(ShapedTwo);

{{< /highlight >}}
