---
title: Aspose.Diagram for Java 17.9 Release Notes
type: docs
weight: 40
url: /sv/java/aspose-diagram-for-java-17-9-release-notes/
---
{{% alert color="primary" %}} 

 Den här sidan innehåller release notes för[Aspose.Diagram for Java 17.9](https://docs.aspose.com/diagram/java/aspose-diagram-for-java-17-9-release-notes/).

{{% /alert %}} 
## **Förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|DIAGRAMJAVA-50485|Lägg till stöd för automatiska avståndsformer i Visio|Förbättring|
|DIAGRAMJAVA-50521|Utgång VSDX - felaktig layout av anslutningsledningen|Insekt|
|DIAGRAMJAVA-50522|Utdata PNG - formtexten går utanför gränsen|Insekt|
|DIAGRAMJAVA-50527|Utgång VSDX - anslutningslinjen vidrör formgränsen|Insekt|
|DIAGRAMJAVA-50540|Utgång VSDX - felaktig layout av anslutningsledningarna|Insekt|
|DIAGRAMJAVA-50543|Utdata VSDX - felaktig layout och felplacerad text på anslutningslinjerna|Insekt|
|DIAGRAMJAVA-50545|Utdata VSDX - Kan inte formulera textens position i form|Insekt|
|DIAGRAMJAVA-50547|Utdata VSDX - kan inte ställa in egenskapsvärdet som sträng|Insekt|
## **Offentlig API och bakåtinkompatibla ändringar**
Se listan för eventuella ändringar som gjorts för allmänheten API såsom tillagda, omdöpta, borttagna eller utfasade medlemmar samt alla icke-bakåtkompatibla ändringar som gjorts till Aspose.Diagram for Java. Om du har frågor om någon ändring i listan, vänligen ta upp det på[Aspose.Diagram supportforum](https://forum.aspose.com/c/diagram/17).
### **Lägger till autoSpaceShapes-medlem i sidan**
Det gör det möjligt att lägga till automatiskt utrymme bland samlingen av former.

{{< highlight "java" >}}

 AutoSpaceOptions options = new AutoSpaceOptions();

diagram.getPages().getPage(0).autoSpaceShapes(diagram.getPages().getPage(0).getShapes(), options);

{{< /highlight >}}
### **Användningsexempel**
Kontrollera listan med hjälpämnen som lagts till i Aspose.Diagram Wiki-dokument:

1. [Placera automatiskt en samling former på sidan Visio](/diagram/sv/java/auto-space-a-collection-of-shapes-in-the-visio-page/)
