---
title: Offentlig API Ändringar i Aspose.Diagram 6.3.0
type: docs
weight: 40
url: /sv/java/public-api-changes-in-aspose-diagram-6-3-0/
---
{{% alert color="primary" %}} 

Det här dokumentet beskriver ändringar av Aspose.Diagram API från version 6.0.0 till 6.3.0, som kan vara av intresse för modul-/applikationsutvecklare. Den innehåller inte bara nya och uppdaterade offentliga metoder, utan också en beskrivning av eventuella förändringar i beteendet bakom kulisserna i Aspose.Diagram.

{{% /alert %}} 
## **Upptäck formatet för en Visio-fil**
### **Olika klasser, metoder och egenskaper läggs till för att upptäcka formatet**
- **Lägg till klasserna FileFormatUtil och FileFormatInfo** 
 - Dessa klasser ger programmatisk åtkomst för att upptäcka filtypen Visio.
- **Lägger till detectFileFormat-metoden i FileFormatUtil Class** 
 - Den upptäcker och returnerar information om formatet för en lagrad Visio diagram i en fil.
- **Lägger till FileFormatType Property i FileFormatInfo Class** 
 - Den får det upptäckta filformatet.
- **Lägger till LoadFormat-egenskap i FileFormatInfo** 
 - Den får det upptäckta laddningsformatet.

 Utvecklare kan enkelt upptäcka formatet på vilken Visio-fil som helst. Det här hjälpämnet illustrerar hur du upptäcker filformatet Visio (med en sökväg eller ström) och kontrollerar dess tillägg:[Upptäck filformatet Visio](/diagram/sv/java/introduction/#Introduction-DetecttheFormatofVisioFile)
## **Kontrollera exporten av dolda Visio-sidor när du sparar**
### **Lägger till setExportHiddenPage i klasserna SVGSaveOptions, XPSSaveOptions, ImageSaveOptions, HTMLSaveOptions och PdfSaveOptions**
- Den definierar om du behöver exportera de dolda Visio-sidorna eller inte.

 Utvecklare kan inkludera eller utesluta dolda Visio-sidor när de sparar en Visio diagram till PDF-, HTML-, bild- (PNG, JPEG, GIF), SVG- och XPS-filer. Det här hjälpämnet illustrerar hur du gör det:[Kontrollera exporten av dolda Visio-sidor när du sparar](/diagram/sv/java/set-orientation-and-control-the-export-of-hidden-visio-pages-on-saving/#control-the-export-of-hidden-visio-pages-on-saving)
