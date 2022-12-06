---
title: Offentlig API Ändringar i Aspose.Diagram 6.0.0
type: docs
weight: 40
url: /sv/net/public-api-changes-in-aspose-diagram-6-0-0/
---
{{% alert color="primary" %}} 

Det här dokumentet beskriver ändringar av Aspose.Diagram API från version 5.9.0 till 6.0.0, som kan vara av intresse för modul-/applikationsutvecklare. Den innehåller inte bara nya och uppdaterade offentliga metoder, utan också en beskrivning av eventuella förändringar i beteendet bakom kulisserna i Aspose.Diagram.

{{% /alert %}} 
## **IsGlued Method läggs till i Shape-klassen**
IsGlued-metoden tar ett formobjekt som en parameter för att avgöra om de två formerna är limmade eller inte.
Exempelkod:

**C#**

{{< highlight "java" >}}

 // Call the diagram constructor to load diagram

Diagram diagram = new Diagram("C:/temp/Drawing1.vsdx");

// get Visio page by name

Page page = diagram.Pages.GetPage("Page-1");

// get Visio shapes by ids

Shape ShapedOne = page.Shapes.GetShape(1);

Shape ShapedTwo = page.Shapes.GetShape(2);

// determine whether shapes are glued

bool glued = ShapedOne.IsGlued(ShapedTwo);

{{< /highlight >}}

**VB**

{{< highlight "java" >}}

 ' Call the diagram constructor to load diagram

Dim diagram As New Diagram("C:/temp/Drawing1.vsdx")

' get Visio page by name

Dim page As Page = diagram.Pages.GetPage("Page-1")

' get Visio shapes by ids

Dim ShapedOne As Shape = page.Shapes.GetShape(1)

Dim ShapedTwo As Shape = page.Shapes.GetShape(2)

' determine whether shapes are glued

Dim glued As Boolean = ShapedOne.IsGlued(ShapedTwo)

{{< /highlight >}}
## **IsConnected Method läggs till i Shape-klassen**
IsConnected-metoden tar ett formobjekt som en parameter för att avgöra om de två formerna är kopplade eller inte.
Exempelkod:

**C#**

{{< highlight "java" >}}

 // Call the diagram constructor to load diagram

Diagram diagram = new Diagram("C:/temp/Drawing1.vsdx");

// get Visio page by name

Page page = diagram.Pages.GetPage("Page-1");

// get Visio shapes by ids

Shape ShapedOne = page.Shapes.GetShape(1);

Shape ShapedTwo = page.Shapes.GetShape(2);

// determine whether shapes are glued

bool glued = ShapedOne.IsConnected(ShapedTwo);

{{< /highlight >}}

**VB**

{{< highlight "java" >}}

 ' Call the diagram constructor to load diagram

Dim diagram As New Diagram("C:/temp/Drawing1.vsdx")

' get Visio page by name

Dim page As Page = diagram.Pages.GetPage("Page-1")

' get Visio shapes by ids

Dim ShapedOne As Shape = page.Shapes.GetShape(1)

Dim ShapedTwo As Shape = page.Shapes.GetShape(2)

' determine whether shapes are glued

Dim glued As Boolean = ShapedOne.IsConnected(ShapedTwo)

{{< /highlight >}}
