---
title: Formen erstellen, gestalten und automatisch anpassen
type: docs
weight: 10
url: /de/java/create-layout-and-auto-fit-shapes/
---
## **Erstellen einer Diagram**
 Mit Aspose.Diagram for Java können Sie Microsoft Visio Diagramme aus Ihren eigenen Anwendungen lesen und erstellen, ohne Microsoft Office Automatisierung. Der erste Schritt beim Erstellen neuer Dokumente ist das Erstellen einer diagram. Dann[Fügen Sie Formen und Verbinder hinzu](/diagram/de/java/add-and-connect-visio-shapes/)um die diagram aufzubauen. Verwenden Sie den Standardkonstruktor von[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) Klasse, um eine neue diagram zu erstellen.
### **Programmierbeispiel**

{{< highlight java >}}
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

## **Layoutformen im Flussdiagrammstil**
 Bei bestimmten Arten von verbundenen Zeichnungen, wie z. B. Flussdiagrammen und Netzwerkdiagrammen, können Sie die verwenden**Layoutformen** Funktion zum automatischen Positionieren von Formen. Die automatische Positionierung ist schneller als das manuelle Ziehen jeder Form an eine neue Position.

Wenn Sie beispielsweise ein großes Flussdiagramm aktualisieren, um einen neuen Prozess einzuschließen, können Sie die Shapes, aus denen der Prozess besteht, hinzufügen und verbinden und dann die Layoutfunktion verwenden, um die aktualisierte Zeichnung automatisch zu gestalten.

 Die Layout-Methode, verfügbar gemacht durch die[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) Die Klasse legt die Formen an und/oder leitet die Anschlüsse auf allen Seiten von diagram um. Diese Methode akzeptiert ein LayoutOptions-Objekt als Argument. Verwenden Sie die verschiedenen Eigenschaften, die von der LayoutOptions-Klasse verfügbar gemacht werden, um Formen automatisch anzuordnen.

Das Bild unten zeigt den diagram, der von den Codeausschnitten in diesem Artikel geladen wird, bevor das automatische Layout angewendet wird. Die Codeschnipsel zeigen, wie man sich bewirbt[Flussdiagramm-Layouts](/diagram/de/java/create-2c-layout-and-auto-fit-shapes/) und[kompakte Baumlayouts](/diagram/de/java/create-2c-layout-and-auto-fit-shapes/).

**Die Quelle diagram.** 

![todo: Bild_alt_Text](create-layout-and-auto-fit-shapes_1.png)

Die Code-Snippets in diesem Artikel verwenden die Quelle diagram und wenden mehrere Arten von automatischem Layout darauf an, wobei sie jeweils in einer separaten Datei gespeichert werden.

|<p>**Layoutformen von unten nach oben** </p><p>![todo: Bild_alt_Text](create-layout-and-auto-fit-shapes_2.png)</p>|<p>**Layoutformen von oben nach unten** </p><p>![todo: Bild_alt_Text](create-layout-and-auto-fit-shapes_3.png)</p>|
|:- |:- |
|<p>**Layoutformen von links nach rechts** </p><p>![todo: Bild_alt_Text](create-layout-and-auto-fit-shapes_4.png)</p>|<p>**Layoutformen von rechts nach links** </p><p>![todo: Bild_alt_Text](create-layout-and-auto-fit-shapes_5.png)</p>|
So gestalten Sie Formen im Flussdiagrammstil:

1. Erstellen Sie eine Instanz der Klasse Diagram.
1. Erstellen Sie eine Instanz der LayoutOptions-Klasse und legen Sie die Eigenschaften für den Flussdiagrammstil fest.
1. Rufen Sie die Layout-Methode der Klasse Diagram auf, indem Sie LayoutOptions übergeben.
1. Rufen Sie die Save-Methode der Klasse Diagram auf, um die Zeichnung Visio zu schreiben.
### **Programmierbeispiel im Flussdiagrammstil**

{{< highlight java >}}
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

### **Anordnen von Formen im kompakten Baumstil**
 Der kompakte Baumlayoutstil versucht, eine Baumstruktur aufzubauen. Es verwendet die gleiche Eingabedatei wie die[Beispiel oben](/diagram/de/java/create-2c-layout-and-auto-fit-shapes/)und speichert in mehreren verschiedenen kompakten Baumstilen.

|<p>**Kompaktes Baumlayout - unten und rechts** </p><p>![todo: Bild_alt_Text](create-layout-and-auto-fit-shapes_6.png)</p>|
|:- |
|<p>**Kompaktes Baumlayout - unten und links** </p><p>![todo: Bild_alt_Text](create-layout-and-auto-fit-shapes_7.png)</p>|


|<p>**Kompaktes Baumlayout - rechts und unten** </p><p>![todo: Bild_alt_Text](create-layout-and-auto-fit-shapes_8.png)</p>|<p>**Kompaktes Baumlayout - links und unten** </p><p>![todo: Bild_alt_Text](create-layout-and-auto-fit-shapes_9.png)</p>|
|:- |:- |
Formen im kompakten Baumstil anordnen:

1.  Erstellen Sie eine Instanz der[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) Klasse.
1. Erstellen Sie eine Instanz der LayoutOptions-Klasse, und legen Sie kompakte Baumstileigenschaften fest.
1. Rufen Sie die Layout-Methode der Klasse Diagram auf, indem Sie LayoutOptions übergeben.
1. Rufen Sie die Save-Methode der Klasse Diagram auf, um die Datei Visio zu schreiben.
#### **Kompaktes Programmierbeispiel im Baumstil**

{{< highlight java >}}
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

## **Passen Sie die Visio Diagram automatisch an**
Aspose.Diagram API unterstützt die automatische Anpassung der Zeichnung Visio. Diese Feature-Operation hilft, äußere Formen innerhalb der Visio-Seitenbegrenzung zu bringen.

Aspose.Diagram for Java API hat die Diagram-Klasse, die eine Visio-Zeichnung darstellt. Die DiagramSaveOptions-Klasse macht die AutoFitPageToDrawingContent-Eigenschaft verfügbar, um die Visio-Zeichnung automatisch anzupassen.

Dieses Beispiel funktioniert wie folgt:

1. Erstellen Sie ein Objekt der Klasse Diagram.
1. Erstellen Sie ein Objekt der Klasse DiagramSaveOptions und übergeben Sie das resultierende Dateiformat.
1. Legen Sie die AutoFitPageToDrawingContent-Eigenschaft des DiagramSaveOptions-Objekts fest.
1. Rufen Sie die Save-Methode des Klassenobjekts Diagram auf und übergeben Sie auch den vollständigen Dateipfad und das DiagramSaveOptions-Objekt.
### **Programmierbeispiel für automatische Anpassung**
Der folgende Beispielcode zeigt, wie Formen in Visio diagram automatisch angepasst werden.


{{< highlight java >}}
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

## **Arbeiten mit VBA-Projekt**
### **Ändern Sie den VBA-Modulcode in Visio Diagram**
Dieser Artikel zeigt, wie Sie einen VBA-Modulcode automatisch mit Aspose.Diagram for Java ändern.

Wir haben die Klassen VbaModule, VbaModuleCollection, VbaProject, VbaProjectReference und VbaProjectReferenceCollection hinzugefügt. Diese Klassen helfen dabei, die Kontrolle über das VBA-Projekt zu erlangen. Entwickler können VBA-Modulcode extrahieren und ändern.
### **Programmierbeispiel für VBA-Modulcode ändern**
Bitte überprüfen Sie dieses Codebeispiel:


{{< highlight java >}}
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

### **Entfernen Sie alle Makros aus Visio Diagram**
Aspose.Diagram for Java ermöglicht Entwicklern, alle Makros aus Visio diagram zu entfernen.

Die JavaProjectData-Eigenschaft, die von der bereitgestellt wird[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) Klasse können Sie alle Makros aus der Zeichnung Visio entfernen.
### **Programmierbeispiel für alle Makros entfernen**

{{< highlight java >}}
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

