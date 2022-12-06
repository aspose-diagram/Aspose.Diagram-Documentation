---
title: Aspose.Diagram for .NET 20.8 Release Notes
type: docs
weight: 14
url: /sv/net/aspose-diagram-for-net-20-8-release-notes/
---
{{% alert color="primary" %}}

Den här sidan innehåller information om release notes för Aspose.Diagram for .NET 20.8.

{{% /alert %}}
## **Förbättringar och förändringar**  ##

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|DIAGRAMNET-51886|Skapa möjlighet att infoga Ole-objekt som Words, Cells, Slides, etc. till Diagram i den enda formen med både objektdata och förhandsgranskningsbild inuti den.|Förbättring|
|DIAGRAMNET-51888|Visio till PDF - API tar lång tid att konvertera|Förbättring|
|DIAGRAMNET-51889|Spara till pdf som loopar mer än 20 minuter|Förbättring|
|DIAGRAMNET-51893|ViewBox-attribut saknas efter VSDX till SVG-konvertering|Förbättring|
|DIAGRAMNET-51851|VSDX till PDF - vissa ikoner saknas och andra inte renderade korrekt|Insekt|
|DIAGRAMNET-51873|VSDX till PDF - Innehåll finns till vänster i utdata-PDF|Insekt|
|DIAGRAMNET-51874|VSDX till PDF - innehåll och rader saknas i utdata|Insekt|
|DIAGRAMNET-51876|VSDX till PNG - vissa former är felaktiga i utdata|Insekt|
|DIAGRAMNET-51879|Visio till PDF - utdata är inte korrekt|Insekt|
|DIAGRAMNET-51894|System.NullReferenceException när diagram laddas|Insekt|
|DIAGRAMNET-51895|Det gick inte att hämta gruppegenskapsdata som SelectionModel, DisplayMode|Insekt|

## **Offentlig API och bakåtinkompatibla ändringar**  ##
Följande är en lista över alla ändringar som gjorts för allmänheten API, såsom tillagda, bytt namn, borttagna eller utfasade medlemmar samt alla icke-bakåtkompatibla ändringar som gjorts till Aspose.Diagram for .NET. Om du har frågor om någon ändring som anges, vänligen ta upp den på supportforumet Aspose.Diagram.

####  Tillagd metod AddShape i sida ####
```
Diagram diagram = new Diagram();

// Get page object by index
Aspose.Diagram.Page page0 = diagram.Pages[0];
// set pinX, pinY, width and height
double pinX = 2, pinY = 2, width = 4, hieght = 3;

// Import ole as Visio shape word
page0.AddShape(pinX, pinY, width, hieght, new FileStream( "imageword.emf", FileMode.OpenOrCreate), new FileStream( "wordsource.doc", FileMode.OpenOrCreate));
```
