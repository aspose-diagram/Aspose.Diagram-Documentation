---
title: Öffentlich API Änderungen in Aspose.Diagram 6.0.0
type: docs
weight: 40
url: /de/net/public-api-changes-in-aspose-diagram-6-0-0/
---
{{% alert color="primary" %}} 

Dieses Dokument beschreibt Änderungen an Aspose.Diagram API von Version 5.9.0 zu 6.0.0, die für Modul-/Anwendungsentwickler von Interesse sein könnten. Es enthält nicht nur neue und aktualisierte öffentliche Methoden, sondern auch eine Beschreibung aller Änderungen im Verhalten hinter den Kulissen in Aspose.Diagram.

{{% /alert %}} 
## **IsGlued-Methode wird in der Shape-Klasse hinzugefügt**
Die IsGlued-Methode verwendet ein Shape-Objekt als Parameter, um zu bestimmen, ob die beiden Shapes geklebt sind oder nicht.
Beispielcode:

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
## **IsConnected-Methode wird in der Shape-Klasse hinzugefügt**
Die IsConnected-Methode verwendet ein Shape-Objekt als Parameter, um zu bestimmen, ob die beiden Shapes verbunden sind oder nicht.
Beispielcode:

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
