﻿---
title:  Konvertera Visio till HTML-format
linktitle: Konvertera Visio till HTML
type: docs
weight: 30
url: /sv/python-net/convert-visio-to-html/
description: Det här ämnet visar hur du Aspose.Diagram tillåter att konvertera Visio till HTML-format. Konvertera VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM till html med några rader kod.
---
## **Exportera Visio till HTML**
 Den här artikeln förklarar hur du exporterar en Microsoft Visio diagram till HTML med[Aspose.Diagram för Python via .NET](https://products.aspose.com/diagram/python-net/) API.

Använd klasskonstruktorn Diagram för att läsa diagram-filerna och metoden Spara för att exportera diagram till valfritt bildformat som stöds. Utvecklare kan spara resulterande HTML i den lokala lagringen eller direkt till en stream-instans.

1. [Spara resulterande HTML i den lokala lagringen](https://docs.aspose.com/diagram/net/convert-visio-to-html/#save-resultant-html-in-the-local-storage).
1. [Spara resulterande HTML i en stream-instans](https://docs.aspose.com/diagram/net/convert-visio-to-html/#save-resultant-html-in-a-stream-instance).

Bilden nedan visar en VSD-fil som ska sparas i PNG-format. Du kan använda andra diagram-format (VSDX, VSDM, VSTX, VSSX, VSS, VSSM, VDX, VST, VSTX, 7183481, 7183481, 7183481, 7183481, 7183481, 7183481, 7183481, 7183481, 81, 7183481 eller 81, 61, 4341, 61 eller 61, 61 eller 60, 61 eller 600

|**Ingång diagram.**|
|:- |
|![todo:image_alt_text](how-to-convert-a-visio-diagram_6.png)|
Utför följande steg för att exportera VSD diagram till HTML:

1. Skapa en instans av klassen Diagram.
1. Anropa Dagram-klassens spara-metod och ange HTML som utdataformat.
### **Spara resulterande HTML i den lokala lagringen**
Den resulterande filen kan sparas genom att skicka en komplett sökvägssträng, inklusive filnamn och filtillägg, t.ex. @"c:\temp\MyOutput.html".
#### **Spara resulterande HTML i lokalt lagringsprogrammeringsexempel**
{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-ExportToHTML.py" >}}
