---
title:  Konvertera Visio till HTML format
linktitle: Konvertera Visio till HTML
type: docs
weight: 30
url: /sv/java/convert-visio-to-html/
description: Det här ämnet visar hur du Aspose.Diagram tillåter att konvertera Visio till HTML-format. Konvertera VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM till html-kod.
---
## **Exportera Visio till HTML** **Exportera Visio till HTML**
 Den här artikeln förklarar hur du exporterar en Microsoft Visio diagram till HTML med[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) API.

 Använd[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/Diagram) klasskonstruktorn för att läsa diagram-filerna och metoden Spara för att exportera diagram till valfritt bildformat som stöds. Utvecklare kan spara resulterande HTML i den lokala lagringen eller direkt till en stream-instans.

1. [Spara resulterande HTML i den lokala lagringen](/diagram/sv/java/how-to-convert-a-visio-diagram/).
1. [Spara resulterande HTML i en stream-instans](/diagram/sv/java/how-to-convert-a-visio-diagram/).

Bilden nedan visar en VSD-fil som ska sparas till PNG-format. Du kan använda andra diagram-format (VSDX, VSTM, VSTM, VSSX, VSS, VSSM, VDX, 0761937611, 381937611, 381937611, 381937611, 381937611, 381937611, 381937611, 381937611, 381937611, 381937611, 3819 och 140

**Ingång diagram.**

![todo:image_alt_text](http://i.imgur.com/YX4BNNq.png)

Utför följande steg för att exportera VSD diagram till HTML:

1. Skapa en instans av klassen Diagram.
1. Anropa Dagram-klassens spara-metod och ställ in HTML som utdataformat.

Bilden nedan visar utdatafilen HTML.

**Utgång HTML diagram.**

![todo:image_alt_text](http://i.imgur.com/syavUqI.png)
### **Spara resulterande HTML i den lokala lagringen**
Den resulterande filen kan sparas genom att skicka en komplett sökvägssträng, inklusive filnamn och filtillägg, t.ex. @"c:\temp\MyOutput.html".
#### **Spara resultatet HTML i lokalt lagringsprogrammeringsexempel**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ExportToHTML.class);

// call the diagram constructor to load diagram from a VSD file
Diagram diagram = new Diagram(dataDir + "ExportToHTML.vsd");

// Save as HTML
diagram.save(dataDir + "ExportToHTML_Out.html", SaveFileFormat.HTML);

{{< /highlight >}}
```



### **Spara resulterande HTML i en stream-instans**
Det är för användning att spara den resulterande HTML i en databas eller arkiv utan att lagra den i den lokala lagringen. Denna funktion bäddar även in andra resulterande resurser från HTML, t.ex. typsnitt, CSS (som innehåller stilinformationen) och bilder. Eftersom det sparar en enda HTML-fil i stream-instansen.
#### **Spara resultatet HTML i ett strömprogrammeringsexempel**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ExportHTMLinStream.class);
// load diagram
Diagram diagram = new Diagram(dataDir + "ExportToHTML.vsd");
// save resultant HTML directly to a stream
ByteArrayOutputStream dstStream = new ByteArrayOutputStream();
diagram.save(dstStream, SaveFileFormat.HTML);
// In you want to read the result into a Diagram object again, in Java you need to get the
// data bytes and wrap into an input stream.
ByteArrayInputStream srcStream = new ByteArrayInputStream(dstStream.toByteArray());

{{< /highlight >}}
```
