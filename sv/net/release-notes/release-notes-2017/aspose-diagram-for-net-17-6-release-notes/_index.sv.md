---
title: Aspose.Diagram for .NET 17.6 Release Notes
type: docs
weight: 70
url: /sv/net/aspose-diagram-for-net-17-6-release-notes/
---
{{% alert color="primary" %}} 

 Den här sidan innehåller release notes för[Aspose.Diagram for .NET 17.6](https://www.nuget.org/packages/Aspose.Diagram/17.6.0).

{{% /alert %}} 
## **Förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|DIAGRAMNET-51264|Skuggan av former är svart vid konvertering av en VSDM till SVG|Förbättring|
|DIAGRAMNET-51270|Kan inte se en form av VSDX i Visio Viewer|Förbättring|
|DIAGRAMNET-51273|Felaktig visning av form i Visio Viewer 2013|Förbättring|
|DIAGRAMNET-51249|Det felaktiga utseendet på den böjda linjen som ansluter till VSDM|Insekt|
|DIAGRAMNET-51250|Ytterligare en vänstra parentes läggs till i texten när du konverterar en VSD till PDF|Insekt|
|DIAGRAMNET-51251|Storleken på ikonen nedgraderas vid konvertering av en VSDM till SVG|Insekt|
|DIAGRAMNET-51253|Felaktig färg på text och ramar i former vid konvertering av en VSDM till SVG|Insekt|
|DIAGRAMNET-51255|En bild längst ner har krossats vid konvertering av en VSDM till SVG|Insekt|
|DIAGRAMNET-51258|Öppna och spara rutin för VSDM - längden på väggarna ändras|Insekt|
|DIAGRAMNET-51259|Öppna och spara rutin för VSDM - längden på väggarna ändras|Insekt|
|DIAGRAMNET-51260|Ett fel på indexeringsintervallet inträffade vid anrop av layoutmetoden för klassen Diagram|Insekt|
|DIAGRAMNET-51263|En extra röd färgetikett visas vid konvertering av en VSDM till SVG|Insekt|
|DIAGRAMNET-51265|Teckensnittet för titeltexten ändras vid konvertering av en VSDM till SVG|Insekt|
|DIAGRAMNET-51266|Storleken på bakgrundsbilden reduceras till att konvertera en VSDM till SVG|Insekt|
|DIAGRAMNET-51267|En ikonstorlek nedgraderas vid konvertering av en VSDM till SVG|Insekt|
|DIAGRAMNET-51268|Hämtar felaktigt transparensvärde för en bild från VSDM-ritning|Insekt|
|DIAGRAMNET-51269|Lägg till virtualiseringsskydd|Insekt|
## **Offentlig API och bakåtinkompatibla ändringar**
Följande är en lista över eventuella ändringar som gjorts för allmänheten API, t.ex. tillagda, bytt namn, borttagna eller utfasade medlemmar samt alla icke-bakåtkompatibla ändringar som gjorts till Aspose.Diagram for .NET. Om du har frågor om någon ändring i listan, vänligen ta upp dem i de[Aspose.Diagram supportforum](https://forum.aspose.com/c/diagram/17).
### **Lägger till RefreshData-medlem i Shape-klassen**
Metoden RefreshData för Shape-klassens instans uppdaterar formens data, inklusive XForm, TextXForm, Connection och Geom, efter att ha ändrat formens text eller andra.

{{< highlight "java" >}}

 // Load diagram

Diagram diagram = new Diagram(@"c:\temp\3DShape_Rotation.vsdx");

// get page by name

Aspose.Diagram.Page page = diagram.Pages.GetPage("Page-1");

// get shape by ID

Aspose.Diagram.Shape shape = page.Shapes.GetShape(1);

// set PinX and PinY values

shape.XForm.PinX.Value = 5;

shape.XForm.PinY.Value = 5;

// save diagram to VSDX format

diagram.Save(@"c:\temp\3DShape_Rotation_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
