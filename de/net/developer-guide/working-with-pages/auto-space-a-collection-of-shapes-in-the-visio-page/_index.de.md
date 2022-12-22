---
title: Platzieren Sie automatisch eine Sammlung von Formen auf der Seite Visio
type: docs
weight: 30
url: /de/net/auto-space-a-collection-of-shapes-in-the-visio-page/
description: In diesem Abschnitt wird erläutert, wie Sie eine Sammlung von Formen auf einer visio-Seite mit Aspose.Diagram automatisch füllen.
---
## **Platzieren Sie automatisch eine Sammlung von Formen auf der Seite Visio**
Mit Aspose.Diagram for .NET API können Entwickler eine Sammlung von Formen in der Zeichnung Visio automatisch platzieren. Um dies zu erreichen, bietet die Page-Klasse ein AutoSpaceShapes-Member, das ShapeCollection- und AutoSpaceOptions-Parameter übernimmt. Die AutoSpaceOptions-Klasse ermöglicht das Festlegen horizontaler und vertikaler Abstände.
### **Formen mit automatischem Abstand auf der Seite**
Verwenden Sie den folgenden Code in Ihrer .NET-Anwendung, um eine Sammlung von Formen auf einer beliebigen Seite der Visio-Zeichnung automatisch zu platzieren.

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
