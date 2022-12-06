---
title: Aspose.Diagram for .NET 17.5 Release Notes
type: docs
weight: 80
url: /sv/net/aspose-diagram-for-net-17-5-release-notes/
---
{{% alert color="primary" %}} 

 Den här sidan innehåller release notes för[Aspose.Diagram for .NET 17.5](https://www.nuget.org/packages/Aspose.Diagram/17.5.0).

{{% /alert %}} 
## **Förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|DIAGRAMNET-51104|Lägg till stöd för formens 3D-rotationsegenskaper|Ny funktion|
|DIAGRAMNET-51229|Öppna och spara processen för VSDM tar bort SolutionXMLs|Förbättring|
|DIAGRAMNET-50283|VTX till HTML-konvertering, dubbelradseffekt på formtextobjekt|Insekt|
|DIAGRAMNET-51195|Felaktig återgivning av en kuvertikon när du sparar ett VDX till SVG|Insekt|
|DIAGRAMNET-51196|Felaktig textjustering när du sparar en VDX till SVG|Insekt|
|DIAGRAMNET-51225|Hämtar ett felaktigt kalendervärde för Shape-data för VSDM|Insekt|
|DIAGRAMNET-51226|Att spara till HTML-ström bäddar inte in externa resurser|Insekt|
|DIAGRAMNET-51227|Det går inte att ställa in TimeSave-värdet för en VSDM|Insekt|
|DIAGRAMNET-51228|Textobjekten förskjuts vid inställning av formdata i VSDM|Insekt|
|DIAGRAMNET-51234|Det går inte att ta bort och lägga till samma namngivna master i VSDM|Insekt|
|DIAGRAMNET-51235|Öppna och spara processen för VSDM tar bort filen vbaProjectSignature.bin|Insekt|
|DIAGRAMNET-51236|Öppna och spara processen för VSDM ändringar Lösning XML-fil|Insekt|
|DIAGRAMNET-51237|Det går inte att spara Del- och NoQuickDrag-värden för Geoms i en VSDM|Insekt|
|DIAGRAMNET-51238|Ställ in TimeSave-värdet när du sparar en Visio-ritning|Insekt|
|DIAGRAMNET-51239|Öppna och spara processen för VSDM tar bort relationsdelen av Solution XML|Insekt|
|DIAGRAMNET-51240|Förskjuten text vid konvertering av en VSD till PDF|Insekt|
|DIAGRAMNET-51242|Det går inte att lägga till formdata till olika former i VSDM|Insekt|
|DIAGRAMNET-51243|Användarcellens UFEV-värde har inte sparats korrekt i VSDM|Insekt|
|DIAGRAMNET-51244|Duplicate page xml-fel vid kopiering av sidor från två VSDM-ritningar|Insekt|
|DIAGRAMNET-51247|Område som inte är tryckt ingår också vid konvertering av en VSD till PDF|Insekt|
## **Offentlig API och bakåtinkompatibla ändringar**
Följande är en lista över eventuella ändringar som gjorts för allmänheten API, t.ex. tillagda, bytt namn, borttagna eller utfasade medlemmar samt alla icke-bakåtkompatibla ändringar som gjorts till Aspose.Diagram for .NET. Om du har frågor om någon ändring i listan, vänligen ta upp dem i de[Aspose.Diagram supportforum](https://forum.aspose.com/c/diagram/17).
### **Lägger till ThreeDFormat-medlem i Shape Class**
ThreeDFormat-klassen tillåter utvecklare att hämta eller ställa in 3D-rotationsegenskaper för en form.

{{< highlight "java" >}}

 // Load diagram

Diagram diagram = new Diagram(@"c:\temp\3DShape_Rotation.vsdx");

// get page by name

Aspose.Diagram.Page page = diagram.Pages.GetPage("Page-1");

// get shape by ID

Aspose.Diagram.Shape shape = page.Shapes.GetShape(1);

// set RotationXAngle property, 

// all other properties are added in ThreeDFormat class

shape.ThreeDFormat.RotationXAngle.Value = 2.61;

// save diagram to VSDX format

diagram.Save(@"c:\temp\3DShape_Rotation_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
### **Användningsexempel**
Kontrollera listan med hjälpämnen som lagts till i Aspose.Diagram Wiki-dokument:

1. [Ändra 3D-rotationsegenskaper i Shapesheet](/diagram/sv/net/3d-rotation-effects-in-a-visio-drawing/#id-3drotationeffectsinavisiodrawing-set3drotationpropertiesinshapesheet)
