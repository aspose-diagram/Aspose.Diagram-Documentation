---
title: Aspose.Diagram for Java 17.7 Release Notes
type: docs
weight: 60
url: /sv/java/aspose-diagram-for-java-17-7-release-notes/
---
{{% alert color="primary" %}} 

 Den här sidan innehåller release notes för[Aspose.Diagram for Java 17.7](https://docs.aspose.com/diagram/java/aspose-diagram-for-java-17-7-release-notes/).

{{% /alert %}} 
## **Förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|DIAGRAMJAVA-50491|Det går inte att hämta den nya formulerade formhöjden.|Förbättring|
|DIAGRAMJAVA-50510|VSD till SVG - felaktigt fyllnadsfärgmönster i formerna.|Förbättring|
|DIAGRAMJAVA-50483|Ofullständig anslutning av former vid lagring av en ritning i VSDX-format.|Insekt|
|DIAGRAMJAVA-50488|Ytterligare textobjekt läggs till när en VSD konverteras till SVG.|Insekt|
|DIAGRAMJAVA-50490|Vertikala kantlinjer för fördefinierad processbox är tjocka när en VSDX-ritning genereras.|Insekt|
|DIAGRAMJAVA-50495|Utdata VSDX - felaktig layout på kopplingslinjen vid tillägg av text till former.|Insekt|
|DIAGRAMJAVA-50496|Utgång VSDX - alla kontakter drivs uppåt.|Insekt|
|DIAGRAMJAVA-50498|Utdata VSDX - den vertikala textvisningen av former istället för den horisontella.|Insekt|
|DIAGRAMJAVA-50506|Ett fel uppstod när en VDX-ritning laddades.|Insekt|
|DIAGRAMJAVA-50508|Utdata VSDX - texten flödar över när du lägger till flerradstext.|Insekt|
|DIAGRAMJAVA-50511|Utgång VSDX - felplacerad text för den dynamiska kontakten.|Insekt|
|DIAGRAMJAVA-50512|Utgång VSDX - förbindelselinjen som går genom en annan form|Insekt|
|DIAGRAMJAVA-50513|Utgång VSDX - en extra linje av anslutning inuti beslutsformen|Insekt|
|DIAGRAMJAVA-50515|Utdata VSDX - hela texten i formen är utanför gränsen|Insekt|
### **addComment Method läggs till i klassen Page**
En överbelastad addComment-metod, som exponeras av klassen Page, tar en Shape-klassinstans och textsträng av kommentaren.

{{< highlight "java" >}}

 // load diagram

Diagram diagram = new Diagram("c:\\temp\\Drawing1.vsdx");

// retrieve page by name

Page page = diagram.getPages().getPage("Page-1");

// retrieve shape by ID

Shape shape = page.getShapes().getShape(12);

page.addComment(shape, "Hello");

// save diagram

diagram.save("c:\\temp\\Drawing1.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
### **Användningsexempel**
Kontrollera listan med hjälpämnen som lagts till i Aspose.Diagram Wiki-dokument:

1. [Lägg till en kommentar på formnivå i Visio Ritning](/diagram/sv/java/working-with-comments/#workingwithcomments-addashape-levelcommentinvisiodrawing)
