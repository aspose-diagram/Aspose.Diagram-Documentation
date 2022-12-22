---
title: Placera automatiskt en samling former på sidan Visio
type: docs
weight: 30
url: /sv/net/auto-space-a-collection-of-shapes-in-the-visio-page/
description: Det här avsnittet förklarar hur man autospacer en samling former på en visio-sida med Aspose.Diagram.
---
## **Placera automatiskt en samling former på sidan Visio**
Med Aspose.Diagram for .NET API kan utvecklare automatiskt placera en samling former i Visio-ritningen. För att uppnå detta erbjuder Page-klassen AutoSpaceShapes-medlem som tar parametrarna ShapeCollection och AutoSpaceOptions. Klassen AutoSpaceOptions tillåter att ställa in horisontella och vertikala avstånd.
### **Auto-space former på sidan**
Använd följande kod i din .NET-applikation för att automatiskt fördela en samling former på valfri sida i Visio-ritningen.

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
