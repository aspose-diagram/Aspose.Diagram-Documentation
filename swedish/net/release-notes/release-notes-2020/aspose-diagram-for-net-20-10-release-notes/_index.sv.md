---
title: Aspose.Diagram for .NET 20.10 Release Notes
type: docs
weight: 10
url: /sv/net/aspose-diagram-for-net-20-10-release-notes/
---
{{% alert color="primary" %}}

Den här sidan innehåller information om release notes för Aspose.Diagram for .NET 20.10.

{{% /alert %}}
## **Förbättringar och förändringar**  ##

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|DIAGRAMNET-51891|Visio till JPG - API tar lång tid att konvertera|Förbättring|
|DIAGRAMNET-51902|Visio-filer med versioner under 11 stöds inte undantag när VSS öppnas|Förbättring|
|DIAGRAMNET-51906|Exportera VSDX till PDF: problem med linjebredd, bild och dimensionering|Förbättring|
|DIAGRAMNET-51929|VSD till SVG-konvertering: Matristransformationer i SVG-utgångsfilen|Förbättring|
|DIAGRAMNET-51931|Visio till PDF - API förbrukar stor mängd minne och tar lång tid|Förbättring|
|DIAGRAMNET-51936|[Forts.]Visio till PDF - API förbrukar stora mängder minne och tar lång tid|Förbättring|
|DIAGRAMNET-51881|2 etiketternas placering är inte korrekt|Insekt|
|DIAGRAMNET-51907|Ett allmänt fel inträffade i GDI+-undantaget inträffar vid rendering av VSDX-fil|Insekt|
|DIAGRAMNET-51926-|Aspose.Diagram 20.9: NullReferenceException vid konvertering av VDX till PNG|Insekt|
|DIAGRAMNET-51928|VSD till SVG-konvertering: Viss text och pilar i slutet av raderna saknas|Insekt|
|DIAGRAMNET-51932|Formstilar förlorade efter vsd –> vsdx konvertering|Insekt|
|DIAGRAMNET-51933|Gradient stoppar format som inte överensstämmer med svg-standarden|Insekt|
|DIAGRAMNET-51934|Objektreferens är inte inställd på en instans av ett objekt.' när du sparar VSS-former för specifik fil|Insekt|
|DIAGRAMNET-51940|2 etiketternas placering är inte korrekt|Insekt|

## **Offentlig API och bakåtinkompatibla ändringar**  ##
Följande är en lista över alla ändringar som gjorts för allmänheten API, såsom tillagda, bytt namn, borttagna eller utfasade medlemmar samt alla icke-bakåtkompatibla ändringar som gjorts till Aspose.Diagram for .NET. Om du har frågor om någon ändring som anges, vänligen ta upp den på supportforumet Aspose.Diagram.

 * Lade till IsExportScaleInMatrix i SVGSaveOptions - Definierar om det behövs exportskala i matris eller inte.
```
Aspose.Diagram.Saving.SVGSaveOptions o = new Aspose.Diagram.Saving.SVGSaveOptions();
o.IsExportScaleInMatrix = false;
```
