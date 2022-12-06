---
title: Arbeta med text
type: docs
weight: 90
url: /sv/net/working-with-text/
description: Det här avsnittet förklarar hur du infogar en textform eller uppdaterar formens text med Aspose.Diagram.
---
## **Infoga en textform på sidan Visio**
 Aspose.Diagram API låter utvecklare infoga en textform var som helst på sidan Visio. För att uppnå detta, AddText-metoden för[Sida](http://www.aspose.com/api/net/diagram/aspose.diagram/page) klass tar PinX, PinY, bredd, höjd och textparametrar.
### **Infoga ett programmeringsexempel för textform**
Följande kodbit lägger till en textform i Visio diagram.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Text-InsertTextShape-InsertTextShape.cs" >}}
## **Uppdatering Visio Formtext**
 Såväl som[skapa diagram](/diagram/sv/net/load-or-create-a-visio-drawing/) , Aspose.Diagram for .NET låter dig arbeta med former på olika sätt. Den här artikeln tittar på hur du kommer åt och uppdaterar text i former. Text-egenskapen, exponerad av[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) klass, stöder objektet Aspose.Diagram.Text. Egenskapen kan användas för att hämta eller uppdatera en forms text. Processen för att uppdatera en forms text är enkel:

1. Ladda ett diagram.
1. Hitta en viss form.
1. Ställ in den nya texten.
1. Spara diagram.
### **Uppdatera formtextprogrammeringsexempel**
Följande kodbit uppdaterar en forms text. Former identifieras med deras ID. Kodsegmenten nedan letar efter en form som kallas process och med ID 1 och ändrar dess text.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Text-UpdateShapeText-UpdateShapeText.cs" >}}
## **Applicera inbyggd eller anpassad formatmall på en Visio-form**
Microsoft Visio stilmallar lagrar formateringsinformation som kan appliceras på former för ett konsekvent utseende och känsla. Aspose.Diagram for .NET låter dig tillämpa stilmallar inifrån en applikation.

 Egenskaperna TextStyle, FillStyle och LineStyle som exponeras av[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) klass stödja[Aspose.Diagram.StyleSheet](http://www.aspose.com/api/net/diagram/aspose.diagram/stylesheet) objekt. Egenskapen kan användas för att hämta stilinformation och tillämpa anpassade text-, linje- och fyllningsstilar på en diagram.
### **Anpassade stilar i Microsoft Visio**
Så här tillämpar du anpassade stilar på former i Microsoft Visio:

1. Öppna ett diagram i Microsoft Visio.
1.  Välj**Definiera stilar** från**Formatera** menyn (Visio 2007), eller högerklicka**Stilar** i**Rita Explorer** fönstret och välj**Definiera stilar** (Visio 2010).
1.  I den**Definiera stilar** skriv ett nytt namn för din anpassade stilmall. Till exempel CustomStyle1.
1.  Klicka på**Text**, **Linje** och**Fylla** knappar för att ställa in text-, linje- och fyllningsstilar.
1.  Klick**OK**.

Efter att ha definierat anpassade stilmallar i Microsoft Visio använder du följande kod i en .NET-applikation för att tillämpa anpassade stilar på dina former. Observera att kodexemplen nedan kallar den anpassade stilmall som definierats ovan: du måste känna till namnet och platsen för arket du använder. Så här tillämpar du anpassade stilar programmatiskt:

1. Ladda ett diagram.
1. Hitta formen du vill använda en stil på.
1. Ladda stilmallen.
1. Applicera stilar.
1. Spara diagram.
#### **Applicera anpassade stilar programmeringsexempel**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Text-ApplyCustomStyleSheets-ApplyCustomStyleSheets.cs" >}}
## **Tillämpa annan stil på varje textvärde i en form**
 Såväl som[skapa diagram](/diagram/sv/net/load-or-create-a-visio-drawing/), Aspose.Diagram for .NET låter dig arbeta med former på olika sätt. Den här artikeln hjälper dig att lägga till flera textvärden till en form och använda olika stilar på varje textvärde.

{{% alert color="primary" %}} 

Shape-elementet innehåller ett element som kallas Text, som innehåller tecknen i texten och specialelement (cp, pp, tp och fld) som markerar slutet på en körning och början på nästa. Char Element innehåller formateringsattribut för formens text, såsom teckensnitt, färg, textstil, skiftläge, position i förhållande till baslinjen och punktstorlek.

{{% /alert %}} 
### **Lägga till formtext och stilar**

|**Ingång diagram**|
|:- |
|![todo:image_alt_text](working-with-text_1.png)|


|**Diagram efter att ha lagt till olika textvärden till en form med olika stil på varje textvärde**|
|:- |
|![todo:image_alt_text](working-with-text_2.png)|
#### **Lägga till text och stilar Programmeringsexempel**
Följande kodbit lägger till en forms text och olika stilar.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Text-ApplyFontOnText-ApplyFontOnText.cs" >}}
## **Hitta och ersätt texten i en form**
 De[Text](http://www.aspose.com/api/net/diagram/aspose.diagram/txt) Klass låter dig redigera formens text. Ersätt-metoden, exponerad av[Text](http://www.aspose.com/api/net/diagram/aspose.diagram/txt) klass, stöd för att ändra texten i en form.
Kodexemplen i den här artikeln hittar och ersätter formens text på sidan.

|**Ingång diagram**|
|:- |
|![todo:image_alt_text](working-with-text_3.png)|


|**diagram efter formen har redigerats**|
|:- |
|![todo:image_alt_text](working-with-text_4.png)|
Processen för att ändra formens text:

1. Ladda ett diagram.
1. Hitta en viss text av en form.
1. Byt ut text i denna form
1. Spara diagram.
### **Hitta och ersätt textprogrammeringsexempel**
Kodavsnitten nedan visar hur du ändrar formens text. Koden itererar genom formerna på en sida.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Text-FindAndReplaceShapeText-FindAndReplaceShapeText.cs" >}}
## **Extrahera vanlig text från sidan Visio Diagram**
Aspose.Diagram API tillåter utvecklare att extrahera vanlig text från sidan Visio diagram. De kan också iterera genom sidorna Visio diagram för att täcka hela texten Visio diagram.

 Microsoft Office Visio lägger till texten i formerna. De[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) klass innehåller ett element som heter Text, som innehåller tecknen i texten och specialelement (cp, pp, tp och fld) som markerar slutet på en körning och början på nästa.
### **Extrahera programmeringsexempel för vanlig text**
Följande kodbit itererar genom formerna på sidan Visio och filtrerar vanlig text utan att formatera information.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Text-GetPlainTextOfVisio-GetPlainTextOfVisio.cs" >}}
