---
title: Aspose.Diagram for .NET 19.4 Release Notes
type: docs
weight: 90
url: /sv/net/aspose-diagram-for-net-19-4-release-notes/
---
{{% alert color="primary" %}} 

Den här sidan innehåller release notes för[Aspose.Diagram for .NET 19.4](https://www.nuget.org/packages/Aspose.Diagram/19.4.0)

{{% /alert %}} 
## **Förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|DIAGRAMNET-51602|Det inbäddade XSLX-objektet skadas efter manipulering|Förbättring|
|DIAGRAMNET-51625|Extern excel-data i .vsdx-filer tas bort när Diagram sparas på nytt|Förbättring|
|DIAGRAMNET-51626|API behandlar inte Excel-data|Förbättring|
|DIAGRAMNET-51627|Extrahera formdata på basis av Dependsons formel|Förbättring|
|DIAGRAMNET-51629|Att förstora en sida för att passa en ritning verkar inte fungera|Förbättring|
|DIAGRAMNET-51176|Gradientens titelfält ändras vid konvertering av en VSDM till SVG|Insekt|
|DIAGRAMNET-51404|VSD till bild - Formfärgen är mörk|Insekt|
|DIAGRAMNET-51473|VDX till PDF - Fel bakgrundsfärg|Insekt|
|DIAGRAMNET-51475|VSDX till PDF - Gradienterna renderas omvänt|Insekt|
|DIAGRAMNET-51616|Visio till PDF - Gradient återges upp och ned i utdata PDF|Insekt|
|DIAGRAMNET-51630|VSDX till HTML - Bakgrundsfärg på former finns inte i utdata|Insekt|
|DIAGRAMNET-51631|VSDX till PDF - Bakgrundsfärg på former finns inte i utdata|Insekt|
|DIAGRAMNET-51632|VSD till SVG - Det går inte att casta objekt av typen ' ' till typen ' ' Undantag inträffade|Insekt|

## **Offentlig API och bakåtinkompatibla ändringar**
Följande är en lista över eventuella ändringar som gjorts för allmänheten API, t.ex. tillagda, bytt namn, borttagna eller utfasade medlemmar samt alla icke-bakåtkompatibla ändringar som gjorts till Aspose.Diagram for .NET. Om du har frågor om någon ändring i listan, vänligen ta upp dem i de[Aspose.Diagram supportforum](https://forum.aspose.com/c/diagram/17).
### **Lägger till enum RemoveHiddenInfoItem**
Anger borttagning av dold information för diagram.
### **Lägger till RemoveHiddenInfoItem i Diagram**
Ta bort oanvänd information.

{{< highlight "java" >}}

diagram.RemoveHiddenInformation((int)(RemoveHiddenInfoItem.Shapes | RemoveHiddenInfoItem.Masters));

{{< /highlight >}}
