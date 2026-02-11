---
title: Skapa, layouta och automatiskt anpassa former
type: docs
weight: 10
url: /sv/java/create-layout-and-auto-fit-shapes/
---
## **Skapar ett Diagram**
 Aspose.Diagram for Java låter dig läsa och skapa Microsoft Visio diagram från dina egna applikationer, utan Microsoft Office Automation. Det första steget när du skapar nya dokument är att skapa en diagram. Sedan[lägg till former och kontakter](/diagram/sv/java/add-and-connect-visio-shapes/)för att bygga upp diagram. Använd standardkonstruktorn för[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) klass för att skapa en ny diagram.
### **Programmeringsexempel**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(CreateDiagram.class);
// Create directory if it is not already present.
File file = new File(dataDir);
if (!file.exists())
	file.mkdir();
// initialize a new Diagram
Diagram diagram = new Diagram();
// save in the VSDX format
diagram.save(dataDir + "CreateDiagram_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
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
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(LayOutShapesInFlowchartStyle.class);     

// load an existing Visio diagram
String fileName = "LayOutShapesInFlowchartStyle.vdx";
Diagram diagram = new Diagram(dataDir + fileName);

// set layout options 
LayoutOptions flowChartOptions = new LayoutOptions();
flowChartOptions.setLayoutStyle(LayoutStyle.FLOW_CHART);
flowChartOptions.setSpaceShapes(1f);
flowChartOptions.setEnlargePage(true);

// set layout direction as BottomToTop and then save
flowChartOptions.setDirection(LayoutDirection.BOTTOM_TO_TOP);
diagram.layout(flowChartOptions);
diagram.save(dataDir + "sample_btm_top.vdx", SaveFileFormat.VDX);

// set layout direction as TopToBottom and then save
diagram = new Diagram(dataDir + fileName);
flowChartOptions.setDirection(LayoutDirection.TOP_TO_BOTTOM);
diagram.layout(flowChartOptions);
diagram.save(dataDir + "sample_top_btm.vdx", SaveFileFormat.VDX);

// set layout direction as LeftToRight and then save
diagram = new Diagram(dataDir + fileName);
flowChartOptions.setDirection(LayoutDirection.LEFT_TO_RIGHT);
diagram.layout(flowChartOptions);
diagram.save(dataDir + "sample_left_right.vdx", SaveFileFormat.VDX);

// set layout direction as RightToLeft and then save
diagram = new Diagram(dataDir + fileName);
flowChartOptions.setDirection(LayoutDirection.RIGHT_TO_LEFT);
diagram.layout(flowChartOptions);
diagram.save(dataDir + "sample_right_left.vdx", SaveFileFormat.VDX);

{{< /highlight >}}
```
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
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(LayOutShapesInCompactTreeStyle.class);
        
String fileName = "LayOutShapesInCompactTreeStyle.vdx";
// load an existing Visio diagram
Diagram diagram = new Diagram(dataDir + fileName);

// set layout options 
LayoutOptions compactTreeOptions = new LayoutOptions();
compactTreeOptions.setLayoutStyle(LayoutStyle.COMPACT_TREE);
compactTreeOptions.setEnlargePage(true);

// set layout direction as DownThenRight and then save
compactTreeOptions.setDirection(LayoutDirection.DOWN_THEN_RIGHT);
diagram.layout(compactTreeOptions);
diagram.save(dataDir + "sample_down_right.vdx", SaveFileFormat.VDX);

// set layout direction as DownThenLeft and then save
diagram = new Diagram(dataDir + fileName);
compactTreeOptions.setDirection(LayoutDirection.DOWN_THEN_LEFT);
diagram.layout(compactTreeOptions);
diagram.save(dataDir + "sample_down_left.vdx", SaveFileFormat.VDX);

// set layout direction as RightThenDown and then save
diagram = new Diagram(dataDir + fileName);
compactTreeOptions.setDirection(LayoutDirection.RIGHT_THEN_DOWN);
diagram.layout(compactTreeOptions);
diagram.save(dataDir + "sample_right_down.vdx", SaveFileFormat.VDX);

// set layout direction as LeftThenDown and then save
diagram = new Diagram(dataDir + fileName);
compactTreeOptions.setDirection(LayoutDirection.LEFT_THEN_DOWN);
diagram.layout(compactTreeOptions);
diagram.save(dataDir + "sample_left_down.vdx", SaveFileFormat.VDX);

{{< /highlight >}}
```
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

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(AutoFitShapesInVisio.class);
// load a Visio diagram
Diagram diagram = new Diagram(dataDir + "BFlowcht.vsdx");

// use saving options
DiagramSaveOptions options = new DiagramSaveOptions(SaveFileFormat.VSDX);
// set Auto fit page property
options.setAutoFitPageToDrawingContent(true);

// save Visio diagram
diagram.save(dataDir + "AutoFitShapesInVisio_Out.vsdx", options);

{{< /highlight >}}
```
## **Arbetar med VBA Project**
### **Ändra VBA-modulkod i Visio Diagram**
Den här artikeln visar hur du ändrar en VBA-modulkod automatiskt med Aspose.Diagram for Java.

Vi har lagt till klasserna VbaModule, VbaModuleCollection, VbaProject, VbaProjectReference och VbaProjectReferenceCollection. Dessa klasser hjälper till att få kontroll över VBA-projekt. Utvecklare kan extrahera och ändra VBA-modulkod.
### **Modifiera VBA-modulkodprogrammeringsexempel**
Kontrollera detta kodexempel:

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// load an existing Visio diagram
String dataDir = Utils.getDataDir(ModifyVBAModuleCode.class);
InputStream input = new FileInputStream(dataDir + "macro.vsdm");
Diagram diagram = new Diagram(input);
// extract VBA project
VbaProject v = diagram.getVbaProject();
// Iterate through the modules and modify VBA macro code
for (int i = 0; i < diagram.getVbaProject().getModules().getCount(); i++) {
	VbaModule module = diagram.getVbaProject().getModules().get(i);
	String code = module.getCodes();
	if (code.contains("This is test message."))
		code = code.replace("This is test message.", "This is Aspose.Diagram message.");
	module.setCodes(code);
}
// save the Visio diagram
diagram.save(dataDir + "out.vssm", SaveFileFormat.VSSM);

{{< /highlight >}}
```
### **Ta bort alla makron från Visio Diagram**
Aspose.Diagram for Java tillåter utvecklare att ta bort alla makron från Visio diagram.

JavaProjectData-egenskapen, exponerad av[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) klass, låter dig ta bort alla makron från Visio-ritningen.
### **Ta bort alla makron programmeringsexempel**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(RemoveMacrosFromVisio.class);  
// load a Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// remove all macros
diagram.setVbProjectData(null);

// Save diagram
diagram.save(dataDir + "RemoveMacrosFromVisio_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
