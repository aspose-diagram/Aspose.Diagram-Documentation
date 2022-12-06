---
title: Aspose.Diagram for Java 17.12 Release Notes
type: docs
weight: 10
url: /sv/java/aspose-diagram-for-java-17-12-release-notes/
---
{{% alert color="primary" %}} 

 Den här sidan innehåller release notes för[Aspose.Diagram for Java 17.12](https://docs.aspose.com/diagram/java/aspose-diagram-for-java-17-12-release-notes/).

{{% /alert %}} 
## **Förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|DIAGRAMJAVA-50290|Ange den enda API för att konvertera en Visio-form till PDF|Förbättring|
|DIAGRAMJAVA-50291|Ange singeln API för att konvertera en Visio-form till HTML|Förbättring|
|DIAGRAMJAVA-50572|Metoden Shape.connectedShapes hämtar inte utgående noder|Förbättring|
|DIAGRAMJAVA-50391|De vända bilderna och pilarna genereras vid konvertering av en VSD till SVG|Insekt|
|DIAGRAMJAVA-50570|VSD till PDF - de ytterligare textobjekten läggs till|Insekt|
|DIAGRAMJAVA-50571|Importera VSDX - ett fel uppstod i formelementet|Insekt|
|DIAGRAMJAVA-50573|VSD till SVG - linjerna i en gruppform saknas|Insekt|
|DIAGRAMJAVA-50575|VSD till SVG - textposterna saknas|Insekt|
|DIAGRAMJAVA-50576|Import VDX-proceduren ger ett sidelementfel|Insekt|
### **Lägger till Copy-medlem i Shape-klassen**
Kopieringsmedlemmen tar en målforminstans som en parameter för att klona denna form.

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

Shape newShape = new Shape();

// copy diagram

newShape.copy(diagram.getPages().get(0).getShapes().get(0));

newShape.setID(3);

newShape.getXForm().getPinX().setValue(1);

newShape.getXForm().getPinY().setValue(1);

{{< /highlight >}}
### **Lägger till pdf-medlem i Shape-klassen**
toPdf-medlemmen konverterar en form till PDF-format.

{{< highlight "java" >}}

 String dataDir = "C:\\temp\\";

// import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// save a shape in the PDF format

diagram.getPages().get(0).getShapes().getShape(59).toPdf(dataDir + "out.pdf");

{{< /highlight >}}
### **Lägger till HTML-medlem i Shape-klassen**
toHTML-medlemmen konverterar en form till PDF-format.

{{< highlight "java" >}}

 String dataDir = "C:\\temp\\";

// import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

HTMLSaveOptions hs = new HTMLSaveOptions();

// save a shape in the PDF format

diagram.getPages().get(0).getShapes().getShape(59).toHTML(dataDir + "out.pdf", hs);

{{< /highlight >}}
### **Användningsexempel**
Kontrollera listan med hjälpämnen som lagts till i Aspose.Diagram Wiki-dokument:

1. [Kopiera en Visio Shape till en annan Shape-instans](https://docs.aspose.com/diagram/java/working-with-visio-shape-data/#use-connection-indexes-to-connect-shapes-programming-sample)
1. [Konvertera Visio Shape till PDF](https://docs.aspose.com/diagram/java/convert-a-visio-shape-to-pdf/)
1. [Konvertera Visio Shape till HTML](https://docs.aspose.com/diagram/java/convert-a-visio-shape-to-html/)


