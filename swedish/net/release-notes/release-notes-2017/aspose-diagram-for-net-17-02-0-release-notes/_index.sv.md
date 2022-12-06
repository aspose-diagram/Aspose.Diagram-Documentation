---
title: Aspose.Diagram for .NET 17.02.0 Release Notes
type: docs
weight: 110
url: /sv/net/aspose-diagram-for-net-17-02-0-release-notes/
---
{{% alert color="primary" %}} 

Den här sidan innehåller release notes för[Aspose.Diagram for .NET 17.02.0](https://www.nuget.org/packages/Aspose.Diagram/17.2.0).

{{% /alert %}} 
## **Förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|DIAGRAMNET-50018|Tillagt stöd för CLS-kompatibelt.|Ny funktion|
|DIAGRAMNET-51110|Integrerad med mätare.|Ny funktion|
|DIAGRAMNET-51143|Förmåga att få gruppen av en given form.|Ny funktion|
|DIAGRAMNET-51144|Förmåga att få föräldern till en given form.|Ny funktion|
|DIAGRAMNET-50149|VSD till PDF konvertering ändras bakgrundsfärgen för en gruppform.|Insekt|
|DIAGRAMNET-50579|VSDX till PDF konvertering, felaktig bakgrundsfärg på formen.|Insekt|
|DIAGRAMNET-50984|Bordslinjerna i tabellen saknas vid konvertering av en VSDX till PNG.|Insekt|
|DIAGRAMNET-50985|Textobjekten är inte korrekt justerade vid konvertering av en VSDX till PNG.|Insekt|
|DIAGRAMNET-50999|Återger felaktig färg på former vid konvertering av en VSD till PNG.|Insekt|
|DIAGRAMNET-51002|HTMLSaveOptions.DefaultFont-egenskapen fungerar inte som förväntat.|Insekt|
|DIAGRAMNET-51049|Formernas färg återges inte korrekt vid konvertering av en VSD till HTML.|Insekt|
|DIAGRAMNET-51080|Fel textjustering av former vid lagring i EMF.|Insekt|
|DIAGRAMNET-51132|De rundade hörnen ändras vid konvertering av en VSD till PDF.|Insekt|
|DIAGRAMNET-51133|Layouten för den dynamiska pilanslutningen ändras vid konvertering av en VSD till PDF.|Insekt|
|DIAGRAMNET-51135|Visio-formerna förskjuts vid konvertering av en VSDX till PDF.|Insekt|
|DIAGRAMNET-51136|Den vertikala texten visas som horisontell text vid konvertering av en VSDX till PDF.|Insekt|
|DIAGRAMNET-51140|Vertikal textruta hänger över kanten på noden när VSDX konverteras till PDF.|Insekt|
|DIAGRAMNET-51138|Ett fel uppstod vid inläsning av en VSDX diagram.|Undantag|
|DIAGRAMNET-51139|Kan inte komma åt filen fel uppstod vid konvertering av en VSDX till HTML.|Undantag|
|DIAGRAMNET-51148|NullReferenceException på Diagram.Spara medan VSD konverteras till HTML.|Undantag|
|DIAGRAMNET-51149|NullReferenceException vid Diagram.Spara när egenskapen CustomProp.Name inte är inställd|Undantag|
## **Offentlig API och bakåtinkompatibla ändringar**
 Följande är en lista över eventuella ändringar som gjorts för allmänheten API, t.ex. tillagda, bytt namn, borttagna eller utfasade medlemmar samt alla icke-bakåtkompatibla ändringar som gjorts till Aspose.Diagram for .NET. Om du har frågor om någon ändring i listan, vänligen ta upp dem i de[Aspose.Diagram supportforum](https://forum.aspose.com/c/diagram/17).
### **Lägger till Shape.ParentShape-egenskap**
Egenskapen Shape.ParentShape gör det möjligt att få den överordnade formen för en nyligen utförd form.

{{< highlight "java" >}}

 // Call a Diagram class constructor to load the VSD diagram

Diagram diagram = new Diagram("Drawing1.vsdx");

// get a sub-shape by page name, group shape ID, and then sub-shape ID

Shape shape = diagram.Pages.GetPage("Page-3").Shapes.GetShape(13).Shapes.GetShape(2);

Shape parentShape = shape.ParentShape;

Console.WriteLine("Parent Shape's Properties:");

Console.WriteLine("Shape ID: " + parentShape.ID);

Console.WriteLine("Shape Name: " + parentShape.Name);

Console.WriteLine("Shape Type: " + parentShape.Type);

{{< /highlight >}}
### **Lägger till metoden Shape.IsInGroup**
Metoden Shape.IsInGroup gör det möjligt att upptäcka om den senaste formen är en del av en gruppform.

{{< highlight "java" >}}

 // Call a Diagram class constructor to load the VSD diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// get a sub-shape by page name, group shape ID, and then sub-shape ID

Shape shape = diagram.Pages.GetPage("Page-3").Shapes.GetShape(13).Shapes.GetShape(2);

Console.WriteLine("Is it in a Group: " + shape.IsInGroup());

{{< /highlight >}}
### **Lägger till Metered Class**
Klassen Metered läggs till. Det tillåter utvecklare att låsa upp utvärderingsbegränsningarna för Aspose.Diagram API samt spåra och underhålla API licenser. Den övervakar också den regelbundna användningen av Aspose.Diagram API.

{{< highlight "java" >}}

 // Initialize a Metered license class object

Aspose.Diagram.Metered metered = new Aspose.Diagram.Metered();

// apply public and private keys

metered.SetMeteredKey("your-public-key", "your-private-key");

{{< /highlight >}}
### **Användningsexempel**
Kontrollera listan med hjälpämnen som lagts till i Aspose.Diagram Wiki-dokument:

1. [Ställ in offentliga och privata nycklar för att tillämpa mätlicens](/diagram/sv/net/licensing/#licensing-setpublicandprivatekeystoapplymeteredlicense)
1. [Hämta den överordnade formen för en underform](/diagram/sv/net/add-retrieve-copy-and-read-visio-shape-data/#add-retrieve-copyandreadvisioshapedata-retrievetheparentshapeofasub-shape)
1. [Verifiera om Visio-formen är i en grupp av former](https://docs.aspose.com/diagram/net/group-convert-and-verify-shapes/)
