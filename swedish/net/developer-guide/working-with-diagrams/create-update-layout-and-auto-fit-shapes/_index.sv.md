---
title: Skapa, uppdatera, layout och autopassa former
type: docs
weight: 10
url: /sv/net/create-update-layout-and-auto-fit-shapes/
description: Använd C# Diagram API för att skapa, uppdatera och automatiskt layoutformer i Visio-filer med C# i dina applikationer. Komplett guide med C# kodexempel.
---
## **Skapar ett Diagram**
 Aspose.Diagram for .NET låter dig läsa och skapa Microsoft Visio diagram från dina egna applikationer, utan Microsoft Office Automation. Det första steget när du skapar nya dokument är att skapa en diagram. Sedan[lägg till former och kontakter](https://docs.aspose.com/diagram/net/add-retrieve-copy-and-read-visio-shape-data/)för att bygga upp diagram. Använd standardkonstruktorn för[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) klass för att skapa en ny diagram.
### **Programmeringsexempel**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Diagrams-CreateDiagram-CreateDiagram.cs" >}}
## **Layoutformer i flödesschemastil**
 Med vissa typer av anslutna ritningar, såsom flödesscheman och nätverksdiagram, kan du använda**Layoutformer** funktion för att automatiskt placera former. Automatisk positionering är snabbare än att manuellt dra varje form till en ny plats.

Om du till exempel uppdaterar ett stort flödesschema för att inkludera en ny process, kan du lägga till och koppla samman de former som utgör processen och sedan använda layoutfunktionen för att automatiskt layouta den uppdaterade ritningen.

 Layoutmetoden, exponerad av[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) klass layoutar formerna och/eller dirigerar om kopplingarna på alla diagram:s sidor. Denna metod accepterar en[Layoutalternativ](https://reference.aspose.com/diagram/net/aspose.diagram.autolayout/layoutoptions)objekt som argument. Använd de olika egenskaperna som exponeras av klassen LayoutOptions för att automatiskt layouta former.

Bilden nedan visar diagram som laddas av kodavsnitten i den här artikeln, innan automatisk layout tillämpas. Kodavsnitten visar hur du ansöker[flödesschema layouter](https://docs.aspose.com/diagram/net/create-update-layout-and-auto-fit-shapes/) och[kompakta trädlayouter](https://docs.aspose.com/diagram/net/create-update-layout-and-auto-fit-shapes/).

**Källan diagram.**

![todo:image_alt_text](create-update-layout-and-auto-fit-shapes_1.png)

Kodavsnitten i den här artikeln tar källan diagram och tillämpar flera typer av automatisk layout på den och sparar var och en i en separat fil.

|<p>**Layout former botten till toppen** </p><p>![todo:image_alt_text](create-update-layout-and-auto-fit-shapes_2.png)</p>|<p>**Layoutformer uppifrån och ned** </p><p>![todo:image_alt_text](create-update-layout-and-auto-fit-shapes_3.png)</p>|
|:- |:- |
|<p>**Layoutformer från vänster till höger** </p><p>![todo:image_alt_text](create-update-layout-and-auto-fit-shapes_4.png)</p>|<p>**Layoutformer från höger till vänster** </p><p>![todo:image_alt_text](create-update-layout-and-auto-fit-shapes_5.png)</p>|
Så här layoutar du former i flödesdiagramstil:

1. Skapa en instans av klassen Diagram.
1. Skapa en instans av klassen LayoutOptions och ställ in flödesschema-stilrelaterade egenskaper.
1. Anropa klassens layoutmetod Diagram genom att skicka LayoutOptions.
1. Ring Diagram-klassens Spara-metod för att skriva Visio-ritningen.
### **Exempel på programmering av flödesschema**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Diagrams-LayOutShapesInFlowchartStyle-LayOutShapesInFlowchartStyle.cs" >}}
### **Lägga ut former i kompakt trädstil**
 Den kompakta trädlayoutstilen försöker bygga en trädstruktur. Den använder samma indatafil som[exemplet ovan](https://docs.aspose.com/diagram/net/create-update-layout-and-auto-fit-shapes/)och sparar ut till flera olika kompakta trädstilar.

|<p>**Kompakt trädlayout - ner och höger** </p><p>![todo:image_alt_text](create-update-layout-and-auto-fit-shapes_6.png)</p>|
|:- |
|<p>**Kompakt trädlayout - ner och vänster** </p><p>![todo:image_alt_text](create-update-layout-and-auto-fit-shapes_7.png)</p>|


|<p>**Kompakt trädlayout - höger och ner** </p><p>![todo:image_alt_text](create-update-layout-and-auto-fit-shapes_8.png)</p>|<p>**Kompakt trädlayout - vänster och ner** </p><p>![todo:image_alt_text](create-update-layout-and-auto-fit-shapes_9.png)</p>|
|:- |:- |
Så här layoutar du former i kompakt trädstil:

1.  Skapa en instans av[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) klass.
1. Skapa en instans av klassen LayoutOptions och ange egenskaper för kompakt trädstil.
1. Anropa klassens layoutmetod Diagram genom att skicka LayoutOptions.
1. Anropa Diagram-klassens Spara-metod för att skriva Visio-filen.
#### **Kompakt trädstilsprogrammeringsexempel**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Diagrams-LayOutShapesInCompactTreeStyle-LayOutShapesInCompactTreeStyle.cs" >}}
## **Autopassa Visio Diagram**
 Aspose.Diagram API stöder automatisk anpassning av Visio-ritningen. Denna funktionsoperation hjälper till att föra yttre former innanför sidgränsen Visio. Aspose.Diagram for .NET API har[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) klass som representerar en Visio-ritning. De[DiagramSaveOptions](https://reference.aspose.com/diagram/net/aspose.diagram.saving/diagramsaveoptions) klass exponerar AutoFitPageToDrawingContent-egenskapen för att automatiskt anpassa Visio-ritningen.

Detta exempel fungerar enligt följande:

1. Skapa ett objekt av klassen Diagram.
1. Skapa ett objekt av klassen DiagramSaveOptions och skicka det resulterande filformatet.
1. Ställ in AutoFitPageToDrawingContent-egenskapen för DiagramSaveOptions-objektet.
1. Anropa Save-metoden för klassobjektet Diagram och skicka även hela filsökvägen och DiagramSaveOptions-objektet.
### **Auto-fit programmeringsexempel**
Följande exempelkod visar hur du automatiskt anpassar former i Visio diagram.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Diagrams-AutoFitShapesInVisio-AutoFitShapesInVisio.cs" >}}
## **Arbetar med VBA Project**
### **Ändra VBA-modulkod i Visio Diagram**
 Den här artikeln visar hur man ändrar en VBA-modulkod automatiskt med Aspose.Diagram for .NET. Vi har lagt till[VbaModule](http://www.aspose.com/api/net/diagram/aspose.diagram.vba/VbaModule), [VbaModuleCollection](http://www.aspose.com/api/net/diagram/aspose.diagram.vba/VbaModuleCollection), [VbaProject](http://www.aspose.com/api/net/diagram/aspose.diagram.vba/VbaProject), [VbaProjectReference](http://www.aspose.com/api/net/diagram/aspose.diagram.vba/VbaProjectReference) och[VbaProjectReferenceCollection](http://www.aspose.com/api/net/diagram/aspose.diagram.vba/VbaProjectReferenceCollection) klasser. Dessa klasser hjälper till att få kontroll över VBA-projekt. Utvecklare kan extrahera och ändra VBA-modulkod.
### **Modifiera VBA-modulkodprogrammeringsexempel**
Kontrollera detta kodexempel:

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Diagrams-ModifyVBAModule-ModifyVBAModule.cs" >}}
### **Ta bort alla makron från Visio Diagram**
 Aspose.Diagram for .NET tillåter utvecklare att ta bort alla makron från Visio diagram. VbProjectData-egenskapen, exponerad av[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) klass, låter dig ta bort alla makron från Visio-ritningen.
### **Ta bort alla makron programmeringsexempel**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Diagrams-RemoveMacrosFromVisio-RemoveMacrosFromVisio.cs" >}}
## **Skapa en ny Diagram med VSTO**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/)låter utvecklare skapa och arbeta med Microsoft Office Visio diagram och införliva funktioner i sina program. Det finns andra sätt att arbeta med Visio-filer, oftast Microsoft Automation. Tyvärr har det vissa begränsningar. Aspose.Diagram är kraftfull och snabb och fungerar självständigt utan Microsoft Office installation.

 Den här migreringsartikeln visar hur du använder först[VSTO](https://docs.aspose.com/diagram/net/create-update-layout-and-auto-fit-shapes/) och då[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) för att skapa en ny diagram och lägga till några former till den. Du kommer att märka att Aspose.Diagram-koden är kortare än VSTO-koden. Använd gärna koden som bas för din egen utveckling och förbättra den för att möta dina behov. VSTO låter dig programmera med Microsoft Visio filer. Så här skapar du ett nytt diagram:

1. Skapa ett Visio applikationsobjekt.
1. Gör applikationsobjektet osynligt.
1. Skapa ett tomt diagram.
1. Lägg till former från Visio mästare (stenciler).
1. Spara filen som VDX.
### **Skapa nytt Diagram med VSTO-programmeringsexempel**
{{% alert color="primary" %}}

använder Visio = Microsoft.Office.Interop.Visio;
Importer Visio = Microsoft.Office.Interop.Visio

{{% /alert %}}


**Exempel:**

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Knowledge-Base-CreatingDiagramWithVSTO-CreatingDiagramWithVSTO.cs" >}}
## **Skapa ett nytt Diagram med Aspose.Diagram for .NET**
Genom att använda Aspose.Diagram API behöver utvecklarna inte Microsoft Office Visio installation på maskinen, och de kan arbeta oberoende av Microsoft Office Automation.

Så här skapar du ett nytt diagram:

1. Skapa ett tomt diagram.
1. Lägg till former från Visio mästare (stenciler).
1. Spara filen som VDX.
### **Ny Diagram med Aspose.Diagram for .NET Programmeringsexempel**
{{% alert color="primary" %}}

använder Aspose.Diagram;
Importer Aspose.Diagram

{{% /alert %}}

Exempel:

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Knowledge-Base-CreatingDiagramWithAspose-CreatingDiagramWithAspose.cs" >}}
## **Uppdatera formegenskaper**
 När du arbetar med Microsoft Visio diagram kan användare uppdatera formattribut inklusive text, stil, position, höjd och bredd. Som mjukvaruutvecklare som arbetar med Visio-filer kommer du att bli ombedd att göra detta programmatiskt. Den goda nyheten är att det är möjligt, antingen genom att använda mekanismerna för programmering med Visio-filer som Microsoft tillhandahåller, VSTO, eller att använda[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/).

 Ämnet nedan visar hur man använder[VSTO](https://products.aspose.com/diagram/net/) och[Aspose.Diagram](https://products.aspose.com/diagram/net/) för att uppdatera formegenskaper. Kodavsnitten nedan visar hur du uppdaterar formegenskaper för VSTO och Aspose.Diagram for .NET. Använd gärna koden och tillämpa den på just din situation.
### **Uppdatering av formegenskaper med VSTO**
VSTO låter dig programmera med Microsoft Visio filer. Så här uppdaterar du formegenskaper:

1. Skapa ett Visio applikationsobjekt.
1. Gör applikationsobjektet osynligt.
1. Öppna en befintlig Visio VSD fil.
1. Hitta den önskade formen.
1. Uppdatera formegenskaperna (text, textstil, position och storlek).
1. Spara filen som VDX.
#### **Uppdatering av formegenskaper med VSTO-programmeringsexempel**
{{% alert color="primary" %}}

använder Visio = Microsoft.Office.Interop.Visio;
Importer Visio = Microsoft.Office.Interop.Visio

{{% /alert %}}

**Exempel:**

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Knowledge-Base-UpdateShapePropsWithVSTO-UpdateShapePropsWithVSTO.cs" >}}
### **Uppdatera formegenskaper med Aspose.Diagram for .NET**
Med Aspose.Diagram API behöver utvecklare inte Microsoft Office Visio på maskinen, och de kan arbeta oberoende av Microsoft Office Automation.

Så här uppdaterar du formegenskaper med Aspose.Diagram for .NET:

1. Öppna en befintlig Visio VSD fil.
1. Hitta den önskade formen.
1. Uppdatera formegenskaperna (text, textstil, position och storlek).
1. Spara filen som VDX.
#### **Uppdatering av formegenskaper med Aspose.Diagram for .NET Programmeringsexempel**
{{% alert color="primary" %}}

använder Aspose.Diagram;
Importer Aspose.Diagram

{{% /alert %}}

**Exempel:**

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Knowledge-Base-UpdateShapePropsWithAspose-UpdateShapePropsWithAspose.cs" >}}
