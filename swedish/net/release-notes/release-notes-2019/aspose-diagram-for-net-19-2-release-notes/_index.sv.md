---
title: Aspose.Diagram for .NET 19.2 Release Notes
type: docs
weight: 110
url: /sv/net/aspose-diagram-for-net-19-2-release-notes/
---
{{% alert color="primary" %}} 

Den här sidan innehåller release notes för[Aspose.Diagram for .NET 19.2](https://www.nuget.org/packages/Aspose.Diagram/19.2.0)

{{% /alert %}} 
## **Förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|DIAGRAMNET-50009|Hjärtformen är blandad när du exporterar VSD ritning i PDF filformat|Förbättring|
|DIAGRAMNET-50010|VSD till PDF exporterar flera sicksacklinjer med en samtidig punkt istället för en enda kurvlinje|Förbättring|
|DIAGRAMNET-51257|Lägg till stöd för NUBRS-linjen när du exporterar en ritning|Förbättring|
|DIAGRAMNET-51611|Det gick inte att få Prop.Prompt.Value korrekt|Förbättring|
|DIAGRAMNET-50355|Böjda linjer exporteras som raka linjer|Insekt|
|DIAGRAMNET-50702|VSDX till PDF export - de böjda kontakterna blir raka|Insekt|
|DIAGRAMNET-51348|VSDX till PDF - Felaktig återgivning av bokstäver|Insekt|
|DIAGRAMNET-51399|VSD till PNG - den krökta linjen omvandlas till rät linje|Insekt|
|DIAGRAMNET-51448|VSD till PNG - ellipsen saknas runt ordet nätverk|Insekt|
|DIAGRAMNET-51472|VSD till PDF - de böjda linjerna exporteras som raka linjer|Insekt|
|DIAGRAMNET-51507|VSDX till PNG - fyllda ovala former saknas i utgången|Insekt|
|DIAGRAMNET-51508|VSDX till SVG - fyllda ovala former saknas i utgången|Insekt|
|DIAGRAMNET-51537|VSDX till SVG - böjda kontakter blir raka kontakter när VSDX återges till PDF|Insekt|
|DIAGRAMNET-51540|Formkanterna ändrades till kvadratiska efter konvertering|Insekt|
|DIAGRAMNET-51577|VISIO till SVG - utgången är inte korrekt|Insekt|
|DIAGRAMNET-51592|Böjda linjer ändras till raka linjer under konvertering|Insekt|
|DIAGRAMNET-51600|Raka linjer blir spikar när du sparar ett diagram som ett annat format|Insekt|
|DIAGRAMNET-51604|VSDX till PDF konverteringsfel - svarta ellipser|Insekt|
|DIAGRAMNET-51605|Uppdatera API referenser och lägg till detaljer om metoden Shape.SetAngle().|Insekt|
|DIAGRAMNET-51610|VSDX till SVG - texten återges inte i rätt teckensnitt|Insekt|
## **Offentlig API och bakåtinkompatibla ändringar**
Följande är en lista över eventuella ändringar som gjorts för allmänheten API, t.ex. tillagda, bytt namn, borttagna eller utfasade medlemmar samt alla icke-bakåtkompatibla ändringar som gjorts till Aspose.Diagram for .NET. Om du har frågor om någon ändring i listan, vänligen ta upp dem i de[Aspose.Diagram supportforum](https://forum.aspose.com/c/diagram/17).
### **Lägg till InheritProps i Shape**
Innehåller rekvisita för formen som ärvs av masterformen.

{{< highlight "java" >}}

  foreach (Aspose.Diagram.Prop prop in shape.InheritProps)

{

    Console.WriteLine(prop.Name);

    Console.WriteLine(prop.Label.Value);

    Console.WriteLine(prop.Prompt.Value);

    Console.WriteLine(prop.Type.Value.ToString());

    Console.WriteLine(prop.Value.Val);

    Console.WriteLine(prop.Format.Value);

}

{{< /highlight >}}
