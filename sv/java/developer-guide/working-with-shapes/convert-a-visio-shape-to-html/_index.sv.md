---
title: Konvertera en Visio Shape till HTML
type: docs
weight: 10
url: /sv/java/convert-a-visio-shape-to-html/
description: Det här avsnittet förklarar hur man konverterar en visio-form till html med Aspose.Diagram.
---
## ** Konvertera en visio-form till html**
 ToHTML-metoden som exponeras av[Form](http://www.aspose.com/api/java/diagram/com.aspose.diagram/shape) klass kan användas för att konvertera till html.

Koden nedan visar hur man:

1. Ladda ett prov diagram.
1. skaffa en viss sida.
1. få en speciell form.
1. konvertera form till html.
### **Forma till HTML**
Använd följande kod i din java-applikation för att konvertera en visio-form till html.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ShapeToHtml.class); 
// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "ShapeToHtml.vsdx");

// Get a particular page
Page page = diagram.getPages().get(0);

// Get a particular shape
Shape shape = page.getShapes().get(0);

// Shape to HTML
HTMLSaveOptions hs = new HTMLSaveOptions();
shape.toHTML("out.htm", hs);
{{< /highlight >}}



