---
title: Aspose.Diagram for .NET 19.11 Release Notes
type: docs
weight: 20
url: /sv/net/aspose-diagram-for-net-19-11-release-notes/
---
{{% alert color="primary" %}} 

Den här sidan innehåller information om release notes för Aspose.Diagram for .NET 19.11.

{{% /alert %}} 
## **Förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|DIAGRAMNET-50004| Lägg till stöd till[tillämpa stilmall](/diagram/sv/net/format-visio-pages/) för helsida|Förbättring|
|DIAGRAMNET-50576|Lägg till stöd för att kassera ett Diagram klassobjekt|Förbättring|
|DIAGRAMNET-50098|Ställ in sidans bakgrundsfärg|Insekt|
|DIAGRAMNET-51722|Diagram till SVG - utdatabilden har fel|Insekt|
|DIAGRAMNET-51724|Fel i Chrome-konsolen vid visning av utdata SVG|Insekt|
|DIAGRAMNET-51725|Hämta z-index av former i Diagram|Insekt|
|DIAGRAMNET-51726|Bakgrundsbild saknas (PowerPoint läggs till i VISIO) samtidigt som oanvända masterformer och stilar tas bort|Insekt|
|DIAGRAMNET-51727|CheckBox (CheckBox Control) Saknas när oanvända masterformer och stilar tas bort|Insekt|
|DIAGRAMNET-51728|Linje saknas när oanvända masterformer och stilar tas bort|Insekt|

## **Offentlig API och bakåtinkompatibla ändringar**
Följande är en lista över alla ändringar som gjorts för allmänheten API, såsom tillagda, bytt namn, borttagna eller utfasade medlemmar samt alla icke-bakåtkompatibla ändringar som gjorts till Aspose.Diagram for .NET. Om du har frågor om någon ändring som anges, vänligen ta upp den på supportforumet Aspose.Diagram.
### **Lade till ApplyStyle på sidan**
Tillämpar stil på helsidan.

{{< highlight "java" >}}

StyleSheet st = new StyleSheet();

st.ID = dia.StyleSheets.Count + 1;

Aspose.Diagram.Char ch = new Aspose.Diagram.Char();

ch.Color.Value = "#00ff00";

ch.IX = 0;

st.Chars.Add(ch);

st.Line.LineColor.Value = "#ff0000";

st.Line.LinePattern.Value = 1;

st.Line.LineWeight.Value = 0.01;

st.Fill.FillForegnd.Value = "#0000ff";

st.Fill.FillPattern.Value = 1;

st.Fill.ShdwPattern.Value = 0;

dia.StyleSheets.Add(st);

foreach (Shape shape in dia.Pages[0].Shapes)

{

     shape.Line.LinePattern.Value = 1;
    
     shape.Fill.FillPattern.Value = 1;

}

dia.Pages[0].ApplyStyle(st.ID, st.ID, st.ID);

{{< /highlight >}}
### **Tillagd Kassera på Diagram**
Utför programdefinierade uppgifter associerade med att frigöra, släppa eller återställa ohanterade resurser.

{{< highlight "java" >}}

 diagram.Dispose();

{{< /highlight >}}
