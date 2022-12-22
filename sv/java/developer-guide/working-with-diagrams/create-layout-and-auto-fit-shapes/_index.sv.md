---
title: Skapa, layouta och automatiskt anpassa former
type: docs
weight: 10
url: /sv/java/create-layout-and-auto-fit-shapes/
---
## **Skapar ett Diagram**
 Aspose.Diagram for Java låter dig läsa och skapa Microsoft Visio diagram från dina egna applikationer, utan Microsoft Office Automation. Det första steget när du skapar nya dokument är att skapa en diagram. Sedan[lägg till former och kontakter](/diagram/sv/java/add-and-connect-visio-shapes/)för att bygga upp diagram. Använd standardkonstruktorn för[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) klass för att skapa en ny diagram.
### **Programmeringsexempel**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Diagrams-CreateDiagram-CreateDiagram.java" >}}
## **Layoutformer i flödesschemastil**
 Med vissa typer av anslutna ritningar, såsom flödesscheman och nätverksdiagram, kan du använda**Layoutformer** funktion för att automatiskt placera former. Automatisk positionering är snabbare än att manuellt dra varje form till en ny plats.

Om du till exempel uppdaterar ett stort flödesschema för att inkludera en ny process, kan du lägga till och koppla samman de former som utgör processen och sedan använda layoutfunktionen för att automatiskt layouta den uppdaterade ritningen.

 Layoutmetoden, exponerad av[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) klass layoutar formerna och/eller dirigerar om kopplingarna på alla diagram:s sidor. Den här metoden accepterar ett LayoutOptions-objekt som ett argument. Använd de olika egenskaperna som exponeras av klassen LayoutOptions för att automatiskt layouta former.

Bilden nedan visar diagram som laddas av kodavsnitten i den här artikeln, innan automatisk layout tillämpas. Kodavsnitten visar hur du ansöker[flödesschema layouter](/diagram/sv/java/create-2c-layout-and-auto-fit-shapes/) och[kompakta trädlayouter](/diagram/sv/java/create-2c-layout-and-auto-fit-shapes/).

**Källan diagram.** 

![todo:image_alt_text](create-layout-and-auto-fit-shapes_1.png)

Kodavsnitten i den här artikeln tar källan diagram och tillämpar flera typer av automatisk layout på den och sparar var och en i en separat fil.

|<p>**Layout former botten till toppen** </p><p>![todo:image_alt_text](create-layout-and-auto-fit-shapes_2.png)</p>|<p>**Layoutformer uppifrån och ned** </p><p>![todo:image_alt_text](create-layout-and-auto-fit-shapes_3.png)</p>|
|:- |:- |
|<p>**Layoutformer från vänster till höger** </p><p>![todo:image_alt_text](create-layout-and-auto-fit-shapes_4.png)</p>|<p>**Layoutformer från höger till vänster** </p><p>![todo:image_alt_text](create-layout-and-auto-fit-shapes_5.png)</p>|
Så här layoutar du former i flödesdiagramstil:

1. Skapa en instans av klassen Diagram.
1. Skapa en instans av klassen LayoutOptions och ställ in flödesschema-stilrelaterade egenskaper.
1. Anropa klassens layoutmetod Diagram genom att skicka LayoutOptions.
1. Ring Diagram-klassens Spara-metod för att skriva Visio-ritningen.
### **Exempel på programmering av flödesschema**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Diagrams-LayOutShapesInFlowchartStyle-LayOutShapesInFlowchartStyle.java" >}}
### **Lägga ut former i kompakt trädstil**
 Den kompakta trädlayoutstilen försöker bygga en trädstruktur. Den använder samma indatafil som[exemplet ovan](/diagram/sv/java/create-2c-layout-and-auto-fit-shapes/)och sparar ut till flera olika kompakta trädstilar.

|<p>**Kompakt trädlayout - ner och höger** </p><p>![todo:image_alt_text](create-layout-and-auto-fit-shapes_6.png)</p>|
|:- |
|<p>**Kompakt trädlayout - ner och vänster** </p><p>![todo:image_alt_text](create-layout-and-auto-fit-shapes_7.png)</p>|


|<p>**Kompakt trädlayout - höger och ner** </p><p>![todo:image_alt_text](create-layout-and-auto-fit-shapes_8.png)</p>|<p>**Kompakt trädlayout - vänster och ner** </p><p>![todo:image_alt_text](create-layout-and-auto-fit-shapes_9.png)</p>|
|:- |:- |
Så här layoutar du former i kompakt trädstil:

1.  Skapa en instans av[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) klass.
1. Skapa en instans av klassen LayoutOptions och ange egenskaper för kompakt trädstil.
1. Anropa klassens layoutmetod Diagram genom att skicka LayoutOptions.
1. Anropa Diagram-klassens Spara-metod för att skriva Visio-filen.
#### **Kompakt trädstilsprogrammeringsexempel**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Diagrams-LayOutShapesInCompactTreeStyle-LayOutShapesInCompactTreeStyle.java" >}}
## **Autopassa Visio Diagram**
Aspose.Diagram API stöder automatisk anpassning av Visio-ritningen. Denna funktionsoperation hjälper till att föra yttre former innanför sidgränsen Visio.

Aspose.Diagram for Java API har klassen Diagram som representerar en Visio ritning. Klassen DiagramSaveOptions exponerar AutoFitPageToDrawingContent-egenskapen för att automatiskt anpassa Visio-ritningen.

Detta exempel fungerar enligt följande:

1. Skapa ett objekt av klassen Diagram.
1. Skapa ett objekt av klassen DiagramSaveOptions och skicka det resulterande filformatet.
1. Ställ in AutoFitPageToDrawingContent-egenskapen för DiagramSaveOptions-objektet.
1. Anropa Save-metoden för klassobjektet Diagram och skicka även hela filsökvägen och DiagramSaveOptions-objektet.
### **Auto-fit programmeringsexempel**
Följande exempelkod visar hur du automatiskt anpassar former i Visio diagram.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Diagrams-AutoFitShapesInVisio-AutoFitShapesInVisio.java" >}}
## **Arbetar med VBA Project**
### **Ändra VBA-modulkod i Visio Diagram**
Den här artikeln visar hur du ändrar en VBA-modulkod automatiskt med Aspose.Diagram for Java.

Vi har lagt till klasserna VbaModule, VbaModuleCollection, VbaProject, VbaProjectReference och VbaProjectReferenceCollection. Dessa klasser hjälper till att få kontroll över VBA-projekt. Utvecklare kan extrahera och ändra VBA-modulkod.
### **Modifiera VBA-modulkodprogrammeringsexempel**
Kontrollera detta kodexempel:

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Diagrams-ModifyVBAModuleCode-ModifyVBAModuleCode.java" >}}
### **Ta bort alla makron från Visio Diagram**
Aspose.Diagram for Java tillåter utvecklare att ta bort alla makron från Visio diagram.

JavaProjectData-egenskapen, exponerad av[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) klass, låter dig ta bort alla makron från Visio-ritningen.
### **Ta bort alla makron programmeringsexempel**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Diagrams-RemoveMacrosFromVisio-RemoveMacrosFromVisio.java" >}}
