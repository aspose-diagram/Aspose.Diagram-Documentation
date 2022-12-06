---
title: Platzieren Sie automatisch eine Sammlung von Formen auf der Seite Visio
type: docs
weight: 30
url: /de/java/auto-space-a-collection-of-shapes-in-the-visio-page/
---
## **Platzieren Sie automatisch eine Sammlung von Formen auf der Seite Visio**
Mit Aspose.Diagram for Java API können Entwickler eine Sammlung von Formen in der Zeichnung Visio automatisch platzieren. Um dies zu erreichen, bietet die Page-Klasse ein autoSpaceShapes-Member, das ShapeCollection- und AutoSpaceOptions-Parameter verwendet. Die AutoSpaceOptions-Klasse ermöglicht das Festlegen horizontaler und vertikaler Abstände.
### **Formen mit automatischem Abstand auf der Seite**
Verwenden Sie den folgenden Code in Ihrer Java-Anwendung, um eine Sammlung von Formen auf einer beliebigen Seite der Visio-Zeichnung automatisch zu platzieren.

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
