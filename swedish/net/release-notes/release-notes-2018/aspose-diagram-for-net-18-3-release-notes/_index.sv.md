---
title: Aspose.Diagram for .NET 18.3 Release Notes
type: docs
weight: 100
url: /sv/net/aspose-diagram-for-net-18-3-release-notes/
---
{{% alert color="primary" %}} 

 Den här sidan innehåller release notes för[Aspose.Diagram for .NET 18.3](https://www.nuget.org/packages/Aspose.Diagram/18.3.0).

{{% /alert %}} 
## **Förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|DIAGRAMNET-50147|VSD till XPS konvertering, de tomma sidorna skapas med röda korsbilder|Förbättring|
|DIAGRAMNET-51431|Lägg till MoveTo-metoden för insamling av sidor|Förbättring|
|DIAGRAMNET-50424  |VSDX till PDF konvertering, ikonen ligger över texten|Insekt|
|DIAGRAMNET-50459|VSDX till PDF konvertering, formikonen är felplacerad från sin ursprungliga position|Insekt|
|DIAGRAMNET-50460|VSDX till PDF konvertering, formikonen är felplacerad från sin ursprungliga position|Insekt|
|DIAGRAMNET-50674|Alla HTML-resurser sparas inte på den anpassade sökvägen|Insekt|
|DIAGRAMNET-51403|VSD till bild - pilhuvudena är felplacerade|Insekt|
|DIAGRAMNET-51427|Utdata VSDX - kontrollerna i Shapes fungerar inte|Insekt|
|DIAGRAMNET-51429|Fixa produktsidans URL över NuGet Galleri|Insekt|
|DIAGRAMNET-51432|Öppna och spara rutin för VSDX bevarar inte teckensnittscell|Insekt|
|DIAGRAMNET-51433|Det går inte att hämta alla formnamn från en VSDX-ritning|Insekt|
## **Offentlig API och bakåtinkompatibla ändringar**
Följande är en lista över eventuella ändringar som gjorts för allmänheten API, t.ex. tillagda, bytt namn, borttagna eller utfasade medlemmar samt alla icke-bakåtkompatibla ändringar som gjorts till Aspose.Diagram for .NET. Om du har frågor om någon ändring i listan, vänligen ta upp dem i de[Aspose.Diagram supportforum](https://forum.aspose.com/c/diagram/17).
### **Lägger till MoveTo-medlem i sidklassen**
MoveTo-medlemmen tar målsidans index som en parameter för att flytta sidans position i Visio-ritningen.

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

Page newPage = new Page(1);

// move page in the diagram

newPage.MoveTo(2);

{{< /highlight >}}
### **Användningsexempel**
Kontrollera listan med hjälpämnen som lagts till i Aspose.Diagram Wiki-dokument:

1. [Flytta sidposition i Visio-ritningen](https://docs.aspose.com/diagram/net/retrieve-get-copy-and-insert-a-page/#move-page-position-in-the-visio-drawing)
