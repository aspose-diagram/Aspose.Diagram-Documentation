---
title: Aspose.Diagram for Java 17.6 Release Notes
type: docs
weight: 70
url: /sv/java/aspose-diagram-for-java-17-6-release-notes/
---
{{% alert color="primary" %}} 

 Den här sidan innehåller release notes för[Aspose.Diagram for Java 17.6](https://docs.aspose.com/diagram/java/aspose-diagram-for-java-17-6-release-notes/).

{{% /alert %}} 
## **Förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|DIAGRAMJAVA-50500|Utdata VSDX - den manuellt tillagda formstorleken ändras inte|Förbättring|
|DIAGRAMJAVA-50503|Utdata VSDX - texten flödar över när du lägger till flerradstext|Förbättring|
|DIAGRAMJAVA-50505|Ett nollpekarfel inträffade vid konvertering av ritsidan till bild|Insekt|
|DIAGRAMJAVA-50484|Vertikal textvisning av beslutsrutans form när du sparar en ritning i formatet VSDX|Insekt|
|DIAGRAMJAVA-50486|Vertikal textvisning av fördefinierad processform när du sparar en ritning i formatet VSDX|Insekt|
|DIAGRAMJAVA-50492|Formlerna i bredd- och höjdcellerna bevaras inte|Insekt|
|DIAGRAMJAVA-50493|Saknade tecken vid konvertering av en VSD till SVG|Insekt|
|DIAGRAMJAVA-50494|Utgång VSDX - anslutningslinjerna ansluter inte mitt i processformer|Insekt|
|DIAGRAMJAVA-50499|VSDX till PNG - en vit horisontell linje visas längst ner i formen|Insekt|
## **Offentlig API och bakåtinkompatibla ändringar**
Se listan för eventuella ändringar som gjorts för allmänheten API såsom tillagda, omdöpta, borttagna eller utfasade medlemmar samt alla icke-bakåtkompatibla ändringar som gjorts till Aspose.Diagram for Java. Om du har frågor om någon ändring i listan, vänligen ta upp det på[Aspose.Diagram supportforum](https://forum.aspose.com/c/diagram/17).
### **Lägger till refreshData Method i Shape-klassen**
Metoden Shape.refreshData tillåter utvecklare att uppdatera data efter att ha ändrat formens position, formens text, geomer och anslutningar.

{{< highlight "java" >}}

 // Call a Diagram class constructor to load the Visio drawing

Diagram diagram = new Diagram(@"c:\temp\Drawing1.vsdx");

//Find a particular shape and update its XForm

for(Shape shape :(Iterable<Shape>) diagram.getPages().get(0).getShapes())

{

    if (shape.getNameU().toLowerCase() == "process" && shape.getID() == 1)

    {

        shape.getXForm().getPinX().setValue(5);

        shape.getXForm().getPinY().setValue(5);

        shape.refreshData();

    }

}

{{< /highlight >}}
