---
title: Lägg till vattenstämpel till Visio
type: docs
weight: 10
url: /sv/java/add-watermark-to-visio/
keywords: watermark, visi
description: Hur man lägger till vattenstämpel till visio med Java Diagram API.
---
## **Skapar ett Diagram**
 Aspose.Diagram for Java låter dig läsa och skapa Microsoft Visio diagram från dina egna applikationer, utan Microsoft Office Automation. Det första steget när du skapar nya dokument är att skapa en diagram. Sedan[lägg till former och kontakter](https://docs.aspose.com/diagram/java/add-retrieve-copy-and-read-visio-shape-data/)för att bygga upp diagram. Använd standardkonstruktorn för[Diagram](http://www.aspose.com/api/java/diagram/com.aspose.diagram/diagram) klass för att skapa en ny diagram.
### **Programmeringsexempel**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(CreateDiagram.class);
// Create directory if it is not already present.
File file = new File(dataDir);
if (!file.exists())
	file.mkdir();
// initialize a new Diagram
Diagram diagram = new Diagram();
// save in the VSDX format
diagram.save(dataDir + "CreateDiagram_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```

Detta exempel fungerar enligt följande:

1. Skapa ett objekt av klassen Diagram.
1. Lägg till vattenstämpel till visio på sidan
1. Anropa Save-metoden för klassobjektet Diagram och skicka även hela filsökvägen och DiagramSaveOptions-objektet.
### **Lägg till vattenstämpel Programmeringsexempel**
Följande exempelkod visar hur man lägger till vattenstämpel i Visio diagram.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(AddWatermarkToVisio.class);   
        
// load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get page by name
Page page = diagram.getPages().getPage("Page-1");

double pinx = page.getPageSheet().getPageProps().getPageWidth().getValue() / 2;
double piny = page.getPageSheet().getPageProps().getPageHeight().getValue() / 2;
double width = page.getPageSheet().getPageProps().getPageWidth().getValue();
double height =page.getPageSheet().getPageProps().getPageHeight().getValue();
    
//Add watermark
Shape shape = page.addText(pinx, piny, width, height, "Test text","Calibri","#a5a5a5",0.25);

// save diagram
diagram.save(dataDir + "ApplyFontOnText_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
