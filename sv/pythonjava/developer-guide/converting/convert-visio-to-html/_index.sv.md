﻿---
title:  Konvertera Visio till HTML format
linktitle: Konvertera Visio till HTML
type: docs
weight: 30
url: /sv/python-java/convert-visio-to-html/
description: This topic show you how to convert Visio to html formats using Aspose.Diagram for Python via Java. Convert VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM, VSSM to html with a few lines of code.
---
## **Exportera Visio till HTML** ##
 Den här artikeln förklarar hur du exporterar en Microsoft Visio diagram till HTML med[Aspose.Diagram för Python via Java](https://products.aspose.com/diagram/python-java/) API.

Använd klasskonstruktorn Diagram för att läsa diagram-filerna och metoden Spara för att exportera diagram till valfritt bildformat som stöds. Utvecklare kan spara resulterande HTML i den lokala lagringen eller direkt till en stream-instans.

 Bilden nedan visar en[VSD fil](ExportToHTML.vsd) på väg att sparas i formatet PNG. Du kan använda andra diagram-format (VSDX, VSTM, VSTM, VSSX, VSS, VSSM, VDX, 0761837619, 1761837619, 161837619, 161837619, 174 och 161837619, 161837619, 180 och 140, 161, 140 och 1400, 140, 100 eller 100

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
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-LoadSaveConvert-ExportToHTML.py" >}}



### **Spara resulterande HTML i en stream-instans**
Det är för användning att spara den resulterande HTML i en databas eller arkiv utan att lagra den i den lokala lagringen. Denna funktion bäddar även in andra resulterande resurser från HTML, t.ex. typsnitt, CSS (som innehåller stilinformationen) och bilder. Eftersom det sparar en enda HTML-fil i stream-instansen.
#### **Spara resultatet HTML i ett strömprogrammeringsexempel**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-LoadSaveConvert-ExportHTMLinStream.py" >}}
