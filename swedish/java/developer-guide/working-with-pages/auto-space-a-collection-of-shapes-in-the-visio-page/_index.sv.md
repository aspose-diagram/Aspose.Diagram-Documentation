---
title: Placera automatiskt en samling former på sidan Visio
type: docs
weight: 30
url: /sv/java/auto-space-a-collection-of-shapes-in-the-visio-page/
---
## **Placera automatiskt en samling former på sidan Visio**
Med Aspose.Diagram for Java API kan utvecklare automatiskt placera en samling former i Visio-ritningen. För att uppnå detta erbjuder Page-klassen autoSpaceShapes-medlem som tar parametrarna ShapeCollection och AutoSpaceOptions. Klassen AutoSpaceOptions tillåter att ställa in horisontella och vertikala avstånd.
### **Auto-space former på sidan**
Använd följande kod i din Java-applikation för att automatiskt fördela en samling former på valfri sida i Visio-ritningen.

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
