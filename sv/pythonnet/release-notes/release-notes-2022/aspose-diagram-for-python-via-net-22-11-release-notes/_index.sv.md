---
title: Aspose.Diagram för Python via .NET 22.11 Release Notes
type: docs
weight: 16
url: /sv/python-net/aspose-diagram-for-python-via-net-22-11-release-notes/
---
{{% alert color="primary" %}} 

Den här sidan innehåller releasenotes för Aspose.Diagram för Python via .NET 22.11.

{{% /alert %}} 

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|DIAGRAMNET-53011|Lägg till stöd för att spara xaml som ström|Förbättring|
|DIAGRAMNET-53012|Formel inte uppfriskande fält|Förbättring|
|DIAGRAMNET-53024|Formel inte uppfriskande fält|Förbättring|
|DIAGRAMNET-53009|Konversation från vsdx till svg förlorad bild|Förbättring|
|DIAGRAMNET-53010|App: Sparar vsdx till Pdf-förlorade former|Insekt|
|DIAGRAMNET-53013|Visio till SVG - Anpassade linjemönster|Insekt|
|DIAGRAMNET-53017|Länkat område i HTML av VSD har ändrats till version 22.10.0.0|Insekt|
|DIAGRAMNET-53018|Bugg med Paras.SpLine|Insekt|
|DIAGRAMNET-53019|extra linje dras längst ner till vänster|Insekt|
|DIAGRAMNET-53033|Värden på celler har inte beräknats korrekt|Insekt|
|DIAGRAMNET-53034|Ändring i form PinX gör att höjden ändras|Insekt|

## **Offentlig API och bakåtinkompatibla ändringar**
Följande är en lista över alla ändringar som gjorts för allmänheten API, såsom tillagda, bytt namn, borttagna eller utfasade medlemmar samt alla icke-bakåtkompatibla ändringar som gjorts till Aspose.Diagram for .NET. Om du har frågor om någon ändring som anges, vänligen ta upp den på supportforumet Aspose.Diagram.

### **Lägger till GetConnectorRule i Shape**
- Returnerar en connectorRule som innehåller form-id och connecton som är anslutna till formen

{{< highlight "java" >}}
ConnectorRule rule= shape.GetConnectorRule();
{{< /highlight >}}

### **Lägger till IsSavingCustomLinePattern i SVGSaveOptions**
- Definierar om Sparar anpassat linjemönster.

{{< highlight "java" >}}
var opt = new SVGSaveOptions()
{
     IsSavingCustomLinePattern = false
};
{{< /highlight >}}

### **Lägger till StreamProvider i XAMLSaveOptions**
- Hämtar eller ställer in IStreamProvider för export av objekt

{{< highlight "java" >}}
MemoryStream stream = new MemoryStream();
var saveOptions = new XAMLSaveOptions();
var streamProvider = new XamlExportStreamProvider(".vsdx");
saveOptions.StreamProvider = streamProvider;
diagram.Save(stream, saveOptions);
{{< /highlight >}}