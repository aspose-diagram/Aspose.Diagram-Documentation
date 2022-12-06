---
title: Aspose.Diagram for Java 6.3.0 Release Notes
type: docs
weight: 90
url: /sv/java/aspose-diagram-for-java-6-3-0-release-notes/
---
## **Andra förbättringar och förändringar**

|**Nyckel** |**Sammanfattning** |**Kategori** |
|:- |:- |:- |
| DIAGRAMJava-50306| Lägg till stöd för att detektera typen Visio diagram.| Ny funktion|
| DIAGRAMJava-50311| Förhindra export av de dolda Visio-sidorna i PDF-filen.| Ny funktion|
| DIAGRAMJava-50312| Förhindra export av de dolda Visio-sidorna i HTML.| Ny funktion|
| DIAGRAM Java-50313| Förhindra export av de dolda Visio-sidorna i PNG.| Ny funktion|
| DIAGRAMJava-50314| Förhindra export av de dolda Visio-sidorna i JPEG.| Ny funktion|
|DIAGRAMJava-50315| Förhindra export av de dolda Visio-sidorna i SVG.| Ny funktion|
| DIAGRAMJava-50316| Förhindra export av de dolda Visio-sidorna i GIF.| Ny funktion|
| DIAGRAMJava-50317| Förhindra export av de dolda Visio-sidorna i XPS.| Ny funktion|
| DIAGRAMJava-50307| VDX till VSDX export markerar alternativet för sidans rutnät som markerat.| Insekt|
| DIAGRAMJava-50308| Öppna och spara rutin för VSDX ändrar text till dummy-tecken.| Insekt|
| DIAGRAMJava-50309| Öppna och spara rutinen för VSDX har ändrat den prickade linjens form.| Insekt|
| DIAGRAMJava-50310| Öppna och spara rutin VSDX ändrar texttypsnitt och fetstil.| Insekt|
| DIAGRAMJava-50318| VSD till VDX exporten ger huvudelementfelet.| Insekt|
### **Offentlig API och bakåtinkompatibla ändringar**
Se listan för eventuella ändringar som gjorts för allmänheten API såsom tillagda, omdöpta, borttagna eller utfasade medlemmar samt alla icke-bakåtkompatibla ändringar som gjorts till Aspose.Diagram for Java. Om du har frågor om någon ändring i listan, vänligen ta upp det på[Aspose.Diagram supportforum](https://forum.aspose.com/c/diagram/17).
#### **Lägg till klasserna FileFormatUtil och FileFormatInfo.**
Dessa klasser ger programmatisk åtkomst för att upptäcka filtypen Visio.
#### **Lägger till detectFileFormat-metoden i FileFormatUtil Class.**
Den upptäcker och returnerar information om formatet för en lagrad Visio diagram i en fil.
#### **Lägger till FileFormatType Property i FileFormatInfo Class**
Den får det upptäckta filformatet.
#### **Lägger till LoadFormat-egenskap i FileFormatInfo**
Den får det upptäckta laddningsformatet.
#### **Lägger till setExportHiddenPage i SVGSaveOptions, XPSSaveOptions,ImageSaveOptions,HTMLSaveOptions,PdfSaveOptions**
Den definierar om du behöver exportera de dolda Visio-sidorna eller inte.
### **Användningsexempel**
Kontrollera listan med hjälpämnen som lagts till i Aspose.Diagram Wiki-dokument:

- [Kontrollera exporten av dolda Visio-sidor när du sparar]()
- [Upptäck filformatet Visio]()
