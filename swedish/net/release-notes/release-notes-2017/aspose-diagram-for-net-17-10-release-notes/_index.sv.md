---
title: Aspose.Diagram for .NET 17.10 Release Notes
type: docs
weight: 30
url: /sv/net/aspose-diagram-for-net-17-10-release-notes/
---
{{% alert color="primary" %}} 

 Den här sidan innehåller release notes för[Aspose.Diagram for .NET 17.10](https://www.nuget.org/packages/Aspose.Diagram/17.10.0).

{{% /alert %}} 
## **Förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|DIAGRAMNET-51349|Lägg till stöd för att konvertera en ritning till bild samma område som en PDF|Förbättring|
|DIAGRAMNET-51352|Åtkomst till inbäddade filer|Förbättring|
|DIAGRAMNET-51085|Formlerna går förlorade under kontrollfliken i Shapesheet när du sparar i VSDX|Insekt|
|DIAGRAMNET-51094|Bevara standardinställningarna under kontrollfliken när du placerar en trapetsform|Insekt|
|DIAGRAMNET-51355|VSDX till PDF - textobjekten är felplacerade|Insekt|
|DIAGRAMNET-51356|VSDX till HTML - textobjekten är felplacerade|Insekt|
|DIAGRAMNET-51357|Öppna och spara rutin för VSDX - saknas datum och redigera datumattribut för anteckningar|Insekt|
|` `DIAGRAMNET-51358|Ett nollpekarfel inträffade när VSDX-ritningen laddades|Insekt|
|DIAGRAMNET-51359|Fel i listan med elementförfattare efter att ha laddat en VSDX|Insekt|
|DIAGRAMNET-51361|VSDX till VDX - det felaktiga textteckensnittet i formen|Insekt|
|DIAGRAMNET-51363|Öppna och spara rutin för VSDX - Tabs-sektionen förvandlas till en självstängd tagg|Insekt|
|DIAGRAMNET-51365|VSD till PNG - felaktig layout av formerna|Insekt|
|DIAGRAMNET-51367|VSD ritningsimport - ett fel i elementet Master|Insekt|
|DIAGRAMNET-51368|VSD till PNG - ett spillfel inträffade|Insekt|
|DIAGRAMNET-51369|VSD till PDF - felplacerade textobjekt längst ner|Insekt|
|DIAGRAMNET-51371|VSDX till VSDX - ytterligare textobjekt läggs till|Insekt|
|DIAGRAMNET-51373|Öppna och spara rutin för en VSDX-ritning saknar ett asiatiskt textteckensnitt|Insekt|
## **Offentlig API och bakåtinkompatibla ändringar**
Följande är en lista över eventuella ändringar som gjorts för allmänheten API, t.ex. tillagda, bytt namn, borttagna eller utfasade medlemmar samt alla icke-bakåtkompatibla ändringar som gjorts till Aspose.Diagram for .NET. Om du har frågor om någon ändring i listan, vänligen ta upp dem i de[Aspose.Diagram supportforum](https://forum.aspose.com/c/diagram/17).
### **Lägger till SameAsPdfConversionArea i ImageSaveOptions**
Den anger om området ska sparas på samma sätt som PDF.

{{< highlight "java" >}}

 string dataDir = @"C:\temp\";

// load a drawing

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// specify image save options

Aspose.Diagram.Saving.ImageSaveOptions opts = new Aspose.Diagram.Saving.ImageSaveOptions(SaveFileFormat.PNG);

opts.SameAsPdfConversionArea = true;

{{< /highlight >}}
