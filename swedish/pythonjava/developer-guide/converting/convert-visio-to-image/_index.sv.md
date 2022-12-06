---
title:  Konvertera Visio till bildformat
linktitle: Konvertera Visio till bilder
type: docs
weight: 20
url: /sv/python-java/convert-visio-to-image/
description: This topic show you how to convert Visio to various images formats using Aspose.Diagram for Python via Java. Convert Visio,VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM, VSSM to PNG, JPEG, BMP images with a några rader kod.
---
## **Exportera diagram till bildfilformat**
Den här artikeln förklarar hur du exporterar en Microsoft Visio diagram till en bild med Aspose.Diagram för Python via Java.

Använd Diagram-klassens konstruktor för att läsa diagram-filerna och Spara-metoden för att exportera diagram till valfritt bildformat som stöds. Bilden nedan visar en VSD-fil som håller på att sparas till PNG-format. Du kan använda andra diagram-format (VSS, VSSX, VSSM, VDX, VST, VSTX, VSTM, 0761113476, 0761130476, 0761130476, 0761130476, 0761130476, 376113416 och 376113476)

**[Exempelfilen VSD.](ExportToImage.vsd)**

Så här exporterar du ett diagram till en bild:

- Skapa en instans av klassen Diagram.
- Anropa Diagram-klassens Spara-metod och ställ in bildformatet du vill exportera till. Utdatafilen ser ut som originalfilen.

**Utdatafilen PNG.**

![todo:image_alt_text](ExportToImage.png)
### **Exportera till bildfil Programmeringsexempel**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-LoadSaveConvert-ExportToImage.py" >}}

Det är också möjligt att spara en viss sida till bild istället för hela dokumentet:

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-LoadSaveConvert-ExportPageToImage.py" >}}