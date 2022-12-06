---
title: Aspose.Diagram for Java 17.02.0 Release Notes
type: docs
weight: 110
url: /sv/java/aspose-diagram-for-java-17-02-0-release-notes/
---
{{% alert color="primary" %}} 

Den här sidan innehåller release notes för[Aspose.Diagram for Java 17.02.0](https://docs.aspose.com/diagram/java/aspose-diagram-for-java-17-02-release-notes/).

{{% /alert %}} 
## **Förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|DIAGRAMJAVA-50037|VSD till PDF-konvertering ändras bakgrundsfärgen för en gruppform.|Insekt|
|DIAGRAMJAVA-50365|En tom sida genereras när en Visio sida med ekvationer konverteras till PNG.|Insekt|
|DIAGRAMJAVA-50461|Kanter saknas vid konvertering av VSDX till PNG.|Insekt|
|DIAGRAMJAVA-50462|Symbolen försvinner när VSDX konverteras till PNG.|Insekt|
|DIAGRAMJAVA-50463|Symbolen försvinner när VSDX konverteras till SVG.|Insekt|
|DIAGRAMJAVA-50465|Färgen på texten är annorlunda vid konvertering av VSDX till PNG.|Insekt|
|DIAGRAMJAVA-50466|Textpositionen är felaktig när VSD konverteras till SVG-format.|Insekt|
|DIAGRAMJAVA-50237|` `[VSDX till PDF]- Felmeddelande uppstod när teckensnittet LeagueGothic Regular användes.|Undantag|
## **Offentlig API och bakåtinkompatibla ändringar**
Se listan för eventuella ändringar som gjorts för allmänheten API såsom tillagda, omdöpta, borttagna eller utfasade medlemmar samt alla icke-bakåtkompatibla ändringar som gjorts till Aspose.Diagram for Java. Om du har frågor om någon ändring i listan, vänligen ta upp det på[Aspose.Diagram supportforum](https://forum.aspose.com/c/diagram/17).
### **Lägger till metoden Shape.getParentShape**
Metoden Shape.getParentShape gör det möjligt att få den överordnade formen för en nyligen utförd form.

{{< highlight "java" >}}

 // Call a Diagram class constructor to load the Visio drawing

Diagram diagram = new Diagram("Drawing1.vsdx");

// get a sub-shape by page name, group shape ID, and then sub-shape ID

Shape shape = diagram.getPages().getPage("Page-3").getShapes().getShape(13).getShapes().getShape(2);

Shape parentShape = shape.getParentShape();

System.out.println("Parent Shape's Properties:");

System.out.println("Shape ID: " + parentShape.getID());

System.out.println("Shape Name: " + parentShape.getName());

System.out.println("Shape Type: " + parentShape.getType());

{{< /highlight >}}
### **Lägger till metoden Shape.isInGroup**
Metoden Shape.isInGroup gör det möjligt att upptäcka om den senaste formen är en del av en gruppform.

{{< highlight "java" >}}

 // Call a Diagram class constructor to load the Visio drawing

Diagram diagram = new Diagram("Drawing1.vsdx");

// get a sub-shape by page name, group shape ID, and then sub-shape ID

Shape shape = diagram.getPages().getPage("Page-3").getShapes().getShape(13).getShapes().getShape(2);

System.out.println("Is it in a Group: " + shape.isInGroup());

{{< /highlight >}}
### **Lägger till Metered Class**
Klassen Metered läggs till. Det tillåter utvecklare att låsa upp utvärderingsbegränsningarna för Aspose.Diagram API samt spåra och underhålla API licenser. Den övervakar också den regelbundna användningen av Aspose.Diagram API.

{{< highlight "java" >}}

 // Initialize a Metered license class object

Metered metered = new Metered();

// apply public and private keys

metered.setMeteredKey("your-public-key", "your-private-key");

{{< /highlight >}}
### **Användningsexempel**
Kontrollera listan med hjälpämnen som lagts till i Aspose.Diagram Wiki-dokument:

1. [Ställ in offentliga och privata nycklar för att tillämpa mätlicens](/diagram/sv/java/licensing/#licensing-setpublicandprivatekeystoapplymeteredlicense)
1. [Hämta den överordnade formen för en underform](/diagram/sv/java/add-retrieve-copy-and-read-visio-shape-data/#add-retrieve-copyandreadvisioshapedata-retrievetheparentshapeofasub-shape)
1. [Verifiera om Visio-formen är i en grupp av former](https://docs.aspose.com/diagram/java/group-convert-and-verify-shapes/)


