---
title: Aspose.Diagram for Java 19.3 Release Notes
type: docs
weight: 100
url: /sv/java/aspose-diagram-for-java-19-3-release-notes/
---
{{% alert color="primary" %}} 

Den här sidan innehåller utgåvor för Aspose.Diagram for Java 19.3

{{% /alert %}} 
## **Förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|DIAGRAMJAVA-50339|Lägg till stöd för att hämta vanliga teckensnittskataloger på operativsystem|Förbättring|
|DIAGRAMJAVA-50097|VSD till PDF konvertering - Böjda linjer blir en rak linje|Insekt|
|DIAGRAMJAVA-50161|VTX till HTML konvertering - Bakgrundsbild av hela diagram saknas|Insekt|
|DIAGRAMJAVA-50301|VSD till PDF export - Metatyper förvandlas till röriga symboler|Insekt|
|DIAGRAMJAVA-50464|Formen återgavs felaktigt vid konvertering av VSDX till PNG|Insekt|
|DIAGRAMJAVA-50652|VISIO till PDF - Utdata PDF visar fel i Adobe Reader|Insekt|
## **Offentlig API och bakåtinkompatibla ändringar**
Följande är en lista över eventuella ändringar som gjorts för allmänheten API, t.ex. tillagda, bytt namn, borttagna eller utfasade medlemmar samt alla icke-bakåtkompatibla ändringar som gjorts till Aspose.Diagram for Java. Om du har frågor om någon ändring i listan, vänligen ta upp dem i de[Aspose.Diagram supportforum](https://forum.aspose.com/c/diagram/17).
### **Lägger till GetDefaultFontDir i Diagram**
Hämta sökvägen till mappen för standardteckensnitt

{{< highlight "java" >}}

  string str =  diagram.getDefaultFontDir();

{{< /highlight >}}
