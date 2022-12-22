---
title: Aspose.Diagram for Java 18.8 Release Notes
type: docs
weight: 50
url: /sv/java/aspose-diagram-for-java-18-8-release-notes/
---
{{% alert color="primary" %}} 

 Den här sidan innehåller release notes för[Aspose.Diagram for Java 18.8](https://docs.aspose.com/diagram/java/aspose-diagram-for-java-18-8-release-notes/).

{{% /alert %}} 
## **Förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|DIAGRAMJAVA-50611|Stöd för inställning av språk med API|Förbättring|
|DIAGRAMJAVA-50606|VSDX till SVG - felaktig återgivning av pilarna|Insekt|
|DIAGRAMJAVA-50610|Platsen för text på anslutningar är fel i utdatafilen VSDX|Insekt|
|DIAGRAMJAVA-50612|Det går inte att öppna utdatafilen VDX med Visio Viewer 2010 Professional|Insekt|
## **Offentlig API och bakåtinkompatibla ändringar**
Följande är en lista över eventuella ändringar som gjorts för allmänheten API, t.ex. tillagda, bytt namn, borttagna eller utfasade medlemmar samt alla icke-bakåtkompatibla ändringar som gjorts till Aspose.Diagram for Java. Om du har frågor om någon ändring i listan, vänligen ta upp dem i de[Aspose.Diagram supportforum](https://forum.aspose.com/c/diagram/17).
#### **Lade till setLocale i LoadOption**
{{< highlight "java" >}}

         LoadOptions loadOptions = new LoadOptions( LoadFileFormat.VDX ); 

        loadOptions.setLocale(Locale.US);

        Diagram diagram = new Diagram("test.vdx", loadOptions); 

{{< /highlight >}}

ställer in det språk som användes för diagram när filen laddades.
