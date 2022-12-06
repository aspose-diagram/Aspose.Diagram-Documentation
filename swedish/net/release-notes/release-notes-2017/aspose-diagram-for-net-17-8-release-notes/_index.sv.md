---
title: Aspose.Diagram for .NET 17.8 Release Notes
type: docs
weight: 50
url: /sv/net/aspose-diagram-for-net-17-8-release-notes/
---
{{% alert color="primary" %}} 

 Den här sidan innehåller release notes för[Aspose.Diagram for .NET 17.8](https://www.nuget.org/packages/Aspose.Diagram/17.8.0).

{{% /alert %}} 
## **Förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|DIAGRAMNET-51295|VSDX till SVG - den låga kvaliteten på SVG-utdata.|Förbättring|
|DIAGRAMNET-51298|SVGSaveOptions - lägg till stöd för att kontrollera nivån på bitmappskomprimering.|Förbättring|
|DIAGRAMNET-51300|Lägg till stöd för anslutande former med anslutningsindex.|Förbättring|
|DIAGRAMNET-50577|VSDX till PDF-konvertering, den cirkulära formens text är felplacerad - I.|Insekt|
|DIAGRAMNET-50582|VSDX till HTML-konvertering, den cirkulära formens text är felplacerad - I.|Insekt|
|DIAGRAMNET-50601|VSDX till PDF-konvertering, den cirkulära formens text är felplacerad - II.|Insekt|
|DIAGRAMNET-50606|VSDX till HTML-konvertering, den cirkulära formens text är felplacerad - II.|Insekt|
|DIAGRAMNET-51197|Varningstriangelformer renderas inte korrekt när VSDM sparas till SVG.|Insekt|
|DIAGRAMNET-51245|Förskjutna textobjekt vid konvertering av en VSD till PDF.|Insekt|
|DIAGRAMNET-51246|Felaktiga teckensnitt tillämpas på text vid konvertering av en VSD till PDF.|Insekt|
|DIAGRAMNET-51296|VSDM till SVG - bilden är trunkerad.|Insekt|
|DIAGRAMNET-51301|VSDX till PDF - färgen på text på anslutande linjer ändras.|Insekt|
|DIAGRAMNET-51302|VSDX till PDF - grafiska element saknas.|Insekt|
|DIAGRAMNET-51304|VSDX till PDF - ofullständig återgivning av flödesschemat.|Insekt|
|DIAGRAMNET-51305|VSDX till PDF - grafiska element saknas.|Insekt|
|DIAGRAMNET-51306|VSDX till PDF - färgen på text på anslutande linjer ändras.|Insekt|
|DIAGRAMNET-51307|VSDX till PDF - grafiska element saknas.|Insekt|
|DIAGRAMNET-51313|Öppna och spara rutin av en VSDX-ritning genererar en korrupt utdatafil.|Insekt|
|DIAGRAMNET-51314|VSDX till SVG - felaktig placering av texten.|Insekt|
|DIAGRAMNET-51317|VSDX till PDF - texten på anslutande rader saknas.|Insekt|
|DIAGRAMNET-51318|VSDX till PDF - den fetstilade texten i rektangelformer saknas.|Insekt|
|DIAGRAMNET-51319|VSDM till SVG - den aritmetiska operationen resulterade i ett spillfel.|Insekt|
|DIAGRAMNET-51320|Fel i formelementet när en VSDM laddades.|Insekt|
|DIAGRAMNET-51323|VSDM till SVG - alla anslutningslinjer saknas.|Insekt|
|DIAGRAMNET-51324|VSDM till SVG - felaktig kantstil och kantfärg av olika former.|Insekt|
|DIAGRAMNET-51326|Problem efter att ha lagt till två kommentarer till formen.|Insekt|
|DIAGRAMNET-51327|Problem efter att ha använt "AddComment"-metoden när du lägger till kommentarer till olika former.|Insekt|
|DIAGRAMNET-51328|Aspose Diagram importerar felaktigt form till dokument.|Insekt|
|DIAGRAMNET-51330|VSDM till SVG - ytterligare en vattenstämpeltext läggs till.|Insekt|
|DIAGRAMNET-51332|VSDM till SVG - felaktig återgivning av en ikon.|Insekt|
|DIAGRAMNET-51334|VSDM till SVG - förskjuten text i övre högra hörnet.|Insekt|
|DIAGRAMNET-51335|VSDM till SVG - felaktig återgivning av bakgrundsbilden.|Insekt|
|DIAGRAMNET-51337|VSD till HTML - ogiltigt format för inmatningssträngsfelet.|Insekt|
## **Offentlig API och bakåtinkompatibla ändringar**
Följande är en lista över eventuella ändringar som gjorts för allmänheten API, t.ex. tillagda, bytt namn, borttagna eller utfasade medlemmar samt alla icke-bakåtkompatibla ändringar som gjorts till Aspose.Diagram for .NET. Om du har frågor om någon ändring i listan, vänligen ta upp dem i de[Aspose.Diagram supportforum](https://forum.aspose.com/c/diagram/17).
### **Lägger till Quality-medlem i SVGSaveOptions-klassen**
Den får eller ställer in ett värde som bestämmer kvaliteten på de genererade bilderna.

{{< highlight "java" >}}

 string dataDir = @"c:\temp\";

// Load an existing drawing

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// specify SVG export settings

SVGSaveOptions options = new SVGSaveOptions();

// set image quality

options.Quality = 100;

// save drawing in the SVG format

diagram.Save(dataDir + "UseSVGSaveOptions_out.svg", options);

{{< /highlight >}}
### **Lägger till ConnectShapesViaConnectorIndex-metoden i klassen Page**
Det gör det möjligt att ansluta former med hjälp av anslutningsindex.

{{< highlight "java" >}}

 string dataDir = @"c:\temp\";

// Load an existing drawing

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// get shapes by ID

Aspose.Diagram.Shape shape1 = diagram.Pages[0].Shapes.GetShape(1);

Aspose.Diagram.Shape shape2 = diagram.Pages[0].Shapes.GetShape(2);

// add connector shapes

Aspose.Diagram.Shape connector1 = new Aspose.Diagram.Shape();

long connecter1Id = diagram.AddShape(connector1, "Dynamic connector", 0);

// connect shapes by index of conneecting points

diagram.Pages[0].ConnectShapesViaConnectorIndex(shape1.ID, 6, shape2.ID, 3, connecter1Id);

// save drawing

diagram.Save(dataDir + "UseSVGSaveOptions_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
### **Användningsexempel**
Kontrollera listan med hjälpämnen som lagts till i Aspose.Diagram Wiki-dokument:

1. [Använd anslutningsindex för att koppla samman former](https://docs.aspose.com/diagram/net/add-retrieve-copy-and-read-visio-shape-data/#use-connection-indexes-to-connect-shapes)
1. [Användning av SVG Spara alternativ](https://docs.aspose.com/diagram/net/save-visio-document/)
