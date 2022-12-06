---
title:  Konvertera Visio till bildformat
linktitle: Konvertera Visio till bilder
type: docs
weight: 20
url: /sv/java/convert-visio-to-image/
description: Det här ämnet visar hur du Aspose.Diagram tillåter att konvertera Visio till olika bildformat. Konvertera Visio,VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,0761 PNG, JPEG a, BMP-linjer med några få linjer med kod.
---
## **Exportera diagram till bildfilformat**
 Den här artikeln förklarar hur du exporterar en Microsoft Visio diagram till en bild med[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) API.

 Använd[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram)class' konstruktor för att läsa diagram-filerna och Spara-metoden för att exportera diagram till valfritt bildformat som stöds. Bilden nedan visar en VSD-fil som håller på att sparas i PNG-format. Du kan också använda andra diagram-format (VSS, VSSX, VSSM, VDX, VST, VSTX, VSTM, VDX, 0761101 eller 13371) också.
**Källfilen. Observera att pil- och triangeletiketterna är i fetstil.**

![todo:image_alt_text](http://i.imgur.com/WOV36ek.png)

Så här exporterar du ett diagram till en bild:

- Skapa en instans av klassen Diagram.
- Anropa Diagram-klassens Spara-metod och ställ in bildformatet du vill exportera till. Utdatafilen ser ut som originalfilen.

**Utdata-PNG-filen.**

![todo:image_alt_text](http://i.imgur.com/WOV36ek.png)
### **Exportera till bildfil Programmeringsexempel**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-ExportToImage-ExportToImage.java" >}}

Det är också möjligt att spara en viss sida till bild istället för hela dokumentet:

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-ExportPageToImage-ExportPageToImage.java" >}}