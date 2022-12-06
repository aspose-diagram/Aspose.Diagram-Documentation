---
title:  Konvertera Visio till HTML-format
linktitle: Konvertera Visio till HTML
type: docs
weight: 30
url: /sv/java/convert-visio-to-html/
description: Det här ämnet visar hur du Aspose.Diagram tillåter att konvertera Visio till HTML-format. Konvertera VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM till html med några rader kod.
---
## **Exportera Visio till HTML** **Exportera Visio till HTML**
 Den här artikeln förklarar hur du exporterar en Microsoft Visio diagram till HTML med[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) API.

 Använd[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/Diagram) klasskonstruktorn för att läsa diagram-filerna och metoden Spara för att exportera diagram till valfritt bildformat som stöds. Utvecklare kan spara resulterande HTML i den lokala lagringen eller direkt till en stream-instans.

1. [Spara resulterande HTML i den lokala lagringen](/diagram/sv/java/how-to-convert-a-visio-diagram/).
1. [Spara resulterande HTML i en stream-instans](/diagram/sv/java/how-to-convert-a-visio-diagram/).

Bilden nedan visar en VSD-fil som ska sparas i PNG-format. Du kan använda andra diagram-format (VSDX, VSTM, VSTM, VSSX, VSS, VSSM, VDX, VST, VSTX, 7183481, 7183481, 7183481, 7183481, 7183481, 7183481, 7183481, 7183481, 81, 7183481 eller 81, 61, 4341, 61 eller 61, 61 eller 60, 61 eller 600

**Ingång diagram.**

![todo:image_alt_text](http://i.imgur.com/YX4BNNq.png)

Utför följande steg för att exportera VSD diagram till HTML:

1. Skapa en instans av klassen Diagram.
1. Anropa Dagram-klassens spara-metod och ange HTML som utdataformat.

Bilden nedan visar utdata-HTML-filen.

**Utdata HTML diagram.**

![todo:image_alt_text](http://i.imgur.com/syavUqI.png)
### **Spara resulterande HTML i den lokala lagringen**
Den resulterande filen kan sparas genom att skicka en komplett sökvägssträng, inklusive filnamn och filtillägg, t.ex. @"c:\temp\MyOutput.html".
#### **Spara resulterande HTML i lokalt lagringsprogrammeringsexempel**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-ExportToHTML-ExportToHTML.java" >}}



### **Spara resulterande HTML i en stream-instans**
Det är avsett att spara den resulterande HTML-koden i en databas eller arkiv utan att lagra den i den lokala lagringen. Denna funktion bäddar också in andra resulterande resurser i HTML, t.ex. typsnitt, CSS (som innehåller stilinformationen) och bilder. Eftersom det sparar en enda HTML-fil i stream-instansen.
#### **Spara resulterande HTML i ett strömprogrammeringsexempel**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-ExportHTMLinStream-ExportHTMLinStream.java" >}}
