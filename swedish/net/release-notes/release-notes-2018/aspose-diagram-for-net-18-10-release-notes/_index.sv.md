---
title: Aspose.Diagram for .NET 18.10 Release Notes
type: docs
weight: 30
url: /sv/net/aspose-diagram-for-net-18-10-release-notes/
---
{{% alert color="primary" %}} 

 Den här sidan innehåller release notes för[Aspose.Diagram for .NET 18.10](https://www.nuget.org/packages/Aspose.Diagram/18.10.0).

{{% /alert %}} 
## **Förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|DIAGRAMNET-51527|Bilder försvinner efter konvertering av VSDM till SVG|Förbättring|
|DIAGRAMNET-51532|VSD till PDF - Skuggan av bilden är inte korrekt|Förbättring|
|DIAGRAMNET-51536|Formens skugga togs bort efter VSDX till SVG-konvertering|Förbättring|
|DIAGRAMNET-51544|Understrykning tas bort från text efter konvertering av VSDM till SVG|Förbättring|
|DIAGRAMNET-51558|Implementera Getter för Shape.ConnectorsType|Förbättring|
|DIAGRAMNET-51520|VDX till HTML - Extra rader visas i utdata|Insekt|
|DIAGRAMNET-51521|Teckensnitt i diagram får ändringar efter att ha sparat VSD som VSDX|Insekt|
|DIAGRAMNET-51523|VSDX till SVG - Pilhuvuden saknas|Insekt|
|DIAGRAMNET-51524|VSDM till SVG - Blå kors dök upp i utdatafil|Insekt|
|DIAGRAMNET-51525|Formen på beslutet ändras från diamant till kvadrat medan VSDM till SVG-konvertering|Insekt|
|DIAGRAMNET-51528|Formen på beslutet ändras från diamant till kvadrat medan VSDM till SVG-konvertering|Insekt|
|DIAGRAMNET-51529|VSDM till SVG - Prickade linjer omvandlas till fyllda linjer|Insekt|
|DIAGRAMNET-51531|Former flyttas till höger efter konvertering av VSDX till SVG|Insekt|
|DIAGRAMNET-51533|Röda kors dök upp efter VISIO till SVG-konvertering|Insekt|
|DIAGRAMNET-51534|Röd prick dök upp i det nedre vänstra hörnet av formen|Insekt|
|DIAGRAMNET-51538|Bilder försvinner efter konvertering av VSDX till PDF|Insekt|
|DIAGRAMNET-51541|Text är osynlig efter konvertering av VSDX till SVG|Insekt|
|DIAGRAMNET-51542|Text raderades efter VSDX till SVG-konvertering|Insekt|
|DIAGRAMNET-51543|Tid- och datumformat ändras efter VSDM TILL SVG|Insekt|
|DIAGRAMNET-51545|VSDX till SVG - Texten är inslagen i utdata|Insekt|
|DIAGRAMNET-51546|VSDX till SVG - Texten är inslagen i utdata|Insekt|
|DIAGRAMNET-51547|VSDX till SVG - Texten är inslagen i utdata|Insekt|
|DIAGRAMNET-51548|VSDX till SVG - Texten är inslagen i utdata|Insekt|
|DIAGRAMNET-51551|Det gick inte att få rätt temafärg på former|Insekt|
|DIAGRAMNET-51552|Omvända pilspetsar som visas i SVG-konvertering|Insekt|
|DIAGRAMNET-51559|Textändringsproblem vid konvertering av VSDM till SVG|Insekt|
|DIAGRAMNET-51560|Anslutningslinjerna blir tunna efter konvertering till SVG|Insekt|
## **Offentlig API och bakåtinkompatibla ändringar**
Följande är en lista över eventuella ändringar som gjorts för allmänheten API, t.ex. tillagda, bytt namn, borttagna eller utfasade medlemmar samt alla icke-bakåtkompatibla ändringar som gjorts till Aspose.Diagram for .NET. Om du har frågor om någon ändring i listan, vänligen ta upp dem i de[Aspose.Diagram supportforum](https://forum.aspose.com/c/diagram/17).
#### **Lade till InheritLine i Shape**
Innehåller linjeformateringsvärdena för formen som ärvs av den överordnade stilen och huvudformen.

{{< highlight "java" >}}

 		Line line = shape.InheritLine;

{{< /highlight >}}


#### **Lade till GetConnectorsType i Shape**
Hämta Connectors typ

{{< highlight "java" >}}

 Shapes.GetShape(1).GetConnectorsType()

{{< /highlight >}}

