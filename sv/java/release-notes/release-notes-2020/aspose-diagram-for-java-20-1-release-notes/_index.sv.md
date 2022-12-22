---
title: Aspose.Diagram for Java 20.1 Release Notes
type: docs
weight: 70
url: /sv/java/aspose-diagram-for-java-20-1-release-notes/
---
{{% alert color="primary" %}} 

Den här sidan innehåller information om release notes för Aspose.Diagram for Java 20.1.

{{% /alert %}} 
## **Förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|DIAGRAMJAVA-50664|Gradientfyllning stöds inte vid export till SVG|Förbättring|
|DIAGRAMJAVA-50670|Tillåt att teckensnitt laddas från minnet|Förbättring|
|DIAGRAMJAVA-50681|API tar lång tid att ladda diagram fil med stor storlek|Förbättring|
|DIAGRAMJAVA-50381|Nätverksformerna bevaras inte vid konvertering av en VSDX till PDF|Insekt|
|DIAGRAMJAVA-50386|Bilderna vänds upp och ner med färgskillnad vid konvertering av en VSD till SVG|Insekt|
|DIAGRAMJAVA-50679|VSDX till PDF - Kontakter saknas i utgången|Insekt|
|DIAGRAMJAVA-50680|Visio till PNG - Utdatabilder har beskurits ut|Insekt|
## **Offentlig API och bakåtinkompatibla ändringar**
Följande är en lista över alla ändringar som gjorts för allmänheten API såsom tillagda, bytt namn, borttagna eller utfasade medlemmar samt alla icke-bakåtkompatibla ändringar som gjorts till Aspose.Diagram för JAVA. Om du har funderingar på någon av de listade ändringarna, vänligen ta upp det på Aspose.Diagram supportforum.

- Added getPages och setPages in Page - Anger indexet för de sidor som ska laddas.

{{< highlight "java" >}}

 LoadOptions options = new LoadOptions(LoadFileFormat.VSDX);

options.setPages(new ArrayList());

options.getPages().add(0);

{{< /highlight >}}

- Lägger till setFontSources i FontConfigs - Ställer in teckensnittskällorna.

{{< highlight "java" >}}

 byte[]b = new byte[]{ 0 };

com.aspose.diagram.MemoryFontSource sc1 = new com.aspose.diagram.MemoryFontSource(b);

com.aspose.diagram.MemoryFontSource sc2 = new com.aspose.diagram.MemoryFontSource(b);

com.aspose.diagram.MemoryFontSource[]sc = new com.aspose.diagram.MemoryFontSource[]{ sc1, sc2 };

com.aspose.diagram.FontConfigs.setFontSources(sc); 

{{< /highlight >}}


