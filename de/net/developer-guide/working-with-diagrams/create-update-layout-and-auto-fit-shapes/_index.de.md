---
title: Formen erstellen, aktualisieren, anordnen und automatisch anpassen
type: docs
weight: 10
url: /de/net/create-update-layout-and-auto-fit-shapes/
description: Verwenden Sie C# Diagram API zum Erstellen, Aktualisieren und automatischen Layout von Formen in Visio-Dateien mit C# in Ihren Anwendungen. Vollständige Anleitung mit C# Codebeispielen.
---
## **Erstellen einer Diagram**
 Mit Aspose.Diagram for .NET können Sie Microsoft Visio Diagramme aus Ihren eigenen Anwendungen lesen und erstellen, ohne Microsoft Office Automatisierung. Der erste Schritt beim Erstellen neuer Dokumente ist das Erstellen einer diagram. Dann[Fügen Sie Formen und Verbinder hinzu](https://docs.aspose.com/diagram/net/add-retrieve-copy-and-read-visio-shape-data/)um die diagram aufzubauen. Verwenden Sie den Standardkonstruktor von[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) Klasse, um eine neue diagram zu erstellen.
### **Programmierbeispiel**
```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Diagrams();

// Create directory if it is not already present.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
    System.IO.Directory.CreateDirectory(dataDir);
// Initialize a new Visio
Diagram diagram = new Diagram();
dataDir = dataDir + "CreateDiagram_out.vsdx";
// Save in the VSDX format
diagram.Save(dataDir, SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Layoutformen im Flussdiagrammstil**
 Bei bestimmten Arten von verbundenen Zeichnungen, wie z. B. Flussdiagrammen und Netzwerkdiagrammen, können Sie die verwenden**Layoutformen** Funktion zum automatischen Positionieren von Formen. Die automatische Positionierung ist schneller als das manuelle Ziehen jeder Form an eine neue Position.

Wenn Sie beispielsweise ein großes Flussdiagramm aktualisieren, um einen neuen Prozess einzuschließen, können Sie die Shapes, aus denen der Prozess besteht, hinzufügen und verbinden und dann die Layoutfunktion verwenden, um die aktualisierte Zeichnung automatisch zu gestalten.

 Die Layout-Methode, verfügbar gemacht durch die[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) Die Klasse legt die Formen an und/oder leitet die Anschlüsse auf allen Seiten von diagram um. Diese Methode akzeptiert eine[LayoutOptionen](https://reference.aspose.com/diagram/net/aspose.diagram.autolayout/layoutoptions)Objekt als Argument. Verwenden Sie die verschiedenen Eigenschaften, die von der LayoutOptions-Klasse verfügbar gemacht werden, um Formen automatisch anzuordnen.

Das Bild unten zeigt den diagram, der von den Codeausschnitten in diesem Artikel geladen wird, bevor das automatische Layout angewendet wird. Die Codeschnipsel zeigen, wie man sich bewirbt[Flussdiagramm-Layouts](https://docs.aspose.com/diagram/net/create-update-layout-and-auto-fit-shapes/) und[kompakte Baumlayouts](https://docs.aspose.com/diagram/net/create-update-layout-and-auto-fit-shapes/).

**Die Quelle diagram.**

![todo: Bild_alt_Text](create-update-layout-and-auto-fit-shapes_1.png)

Die Code-Snippets in diesem Artikel verwenden die Quelle diagram und wenden mehrere Arten von automatischem Layout darauf an, wobei sie jeweils in einer separaten Datei gespeichert werden.

|<p>**Layoutformen von unten nach oben** </p><p>![todo: Bild_alt_Text](create-update-layout-and-auto-fit-shapes_2.png)</p>|<p>**Layoutformen von oben nach unten** </p><p>![todo: Bild_alt_Text](create-update-layout-and-auto-fit-shapes_3.png)</p>|
|:- |:- |
|<p>**Layoutformen von links nach rechts** </p><p>![todo: Bild_alt_Text](create-update-layout-and-auto-fit-shapes_4.png)</p>|<p>**Layoutformen von rechts nach links** </p><p>![todo: Bild_alt_Text](create-update-layout-and-auto-fit-shapes_5.png)</p>|
So gestalten Sie Formen im Flussdiagrammstil:

1. Erstellen Sie eine Instanz der Klasse Diagram.
1. Erstellen Sie eine Instanz der LayoutOptions-Klasse und legen Sie die Eigenschaften für den Flussdiagrammstil fest.
1. Rufen Sie die Layout-Methode der Klasse Diagram auf, indem Sie LayoutOptions übergeben.
1. Rufen Sie die Save-Methode der Klasse Diagram auf, um die Zeichnung Visio zu schreiben.
### **Programmierbeispiel im Flussdiagrammstil**
```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Diagrams();

// Load an existing Visio diagram
string fileName = "LayOutShapesInFlowchartStyle.vdx";
Diagram diagram = new Diagram(dataDir + fileName);

// Set layout options 
LayoutOptions flowChartOptions = new LayoutOptions();
flowChartOptions.LayoutStyle = LayoutStyle.FlowChart;
flowChartOptions.SpaceShapes = 1f;
flowChartOptions.EnlargePage = true;

// Set layout direction as BottomToTop and then save
flowChartOptions.Direction = LayoutDirection.BottomToTop;
diagram.Layout(flowChartOptions);
diagram.Save(dataDir + "sample_btm_top_out.vdx", SaveFileFormat.VDX);

// Set layout direction as TopToBottom and then save
diagram = new Diagram(dataDir + fileName);
flowChartOptions.Direction = LayoutDirection.TopToBottom;
diagram.Layout(flowChartOptions);
diagram.Save(dataDir + "sample_top_btm_out.vdx", SaveFileFormat.VDX);

// Set layout direction as LeftToRight and then save
diagram = new Diagram(dataDir + fileName);
flowChartOptions.Direction = LayoutDirection.LeftToRight;
diagram.Layout(flowChartOptions);
diagram.Save(dataDir + "sample_left_right_out.vdx", SaveFileFormat.VDX);

// Set layout direction as RightToLeft and then save
diagram = new Diagram(dataDir + fileName);
flowChartOptions.Direction = LayoutDirection.RightToLeft;
diagram.Layout(flowChartOptions);
diagram.Save(dataDir + "sample_right_left_out.vdx", SaveFileFormat.VDX);

{{< /highlight >}}
```
### **Anordnen von Formen im kompakten Baumstil**
 Der kompakte Baumlayoutstil versucht, eine Baumstruktur aufzubauen. Es verwendet die gleiche Eingabedatei wie die[Beispiel oben](https://docs.aspose.com/diagram/net/create-update-layout-and-auto-fit-shapes/)und speichert in mehreren verschiedenen kompakten Baumstilen.

|<p>**Kompaktes Baumlayout - unten und rechts** </p><p>![todo: Bild_alt_Text](create-update-layout-and-auto-fit-shapes_6.png)</p>|
|:- |
|<p>**Kompaktes Baumlayout - unten und links** </p><p>![todo: Bild_alt_Text](create-update-layout-and-auto-fit-shapes_7.png)</p>|


|<p>**Kompaktes Baumlayout - rechts und unten** </p><p>![todo: Bild_alt_Text](create-update-layout-and-auto-fit-shapes_8.png)</p>|<p>**Kompaktes Baumlayout - links und unten** </p><p>![todo: Bild_alt_Text](create-update-layout-and-auto-fit-shapes_9.png)</p>|
|:- |:- |
Formen im kompakten Baumstil anordnen:

1.  Erstellen Sie eine Instanz der[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) Klasse.
1. Erstellen Sie eine Instanz der LayoutOptions-Klasse, und legen Sie kompakte Baumstileigenschaften fest.
1. Rufen Sie die Layout-Methode der Klasse Diagram auf, indem Sie LayoutOptions übergeben.
1. Rufen Sie die Save-Methode der Klasse Diagram auf, um die Datei Visio zu schreiben.
#### **Kompaktes Programmierbeispiel im Baumstil**
```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Diagrams();

string fileName = "LayOutShapesInCompactTreeStyle.vdx";
// Load an existing Visio diagram
Diagram diagram = new Diagram(dataDir + fileName);

// Set layout options 
LayoutOptions compactTreeOptions = new LayoutOptions();
compactTreeOptions.LayoutStyle = LayoutStyle.CompactTree;
compactTreeOptions.EnlargePage = true;

// Set layout direction as DownThenRight and then save
compactTreeOptions.Direction = LayoutDirection.DownThenRight;
diagram.Layout(compactTreeOptions);
diagram.Save(dataDir + "sample_down_right.vdx", SaveFileFormat.VDX);

// Set layout direction as DownThenLeft and then save
diagram = new Diagram(dataDir + fileName);
compactTreeOptions.Direction = LayoutDirection.DownThenLeft;
diagram.Layout(compactTreeOptions);
diagram.Save(dataDir + "sample_down_left.vdx", SaveFileFormat.VDX);

// Set layout direction as RightThenDown and then save
diagram = new Diagram(dataDir + fileName);
compactTreeOptions.Direction = LayoutDirection.RightThenDown;
diagram.Layout(compactTreeOptions);
diagram.Save(dataDir + "sample_right_down.vdx", SaveFileFormat.VDX);

// Set layout direction as LeftThenDown and then save
diagram = new Diagram(dataDir + fileName);
compactTreeOptions.Direction = LayoutDirection.LeftThenDown;
diagram.Layout(compactTreeOptions);
diagram.Save(dataDir + "sample_left_down.vdx", SaveFileFormat.VDX);

{{< /highlight >}}
```
## **Passen Sie die Visio Diagram automatisch an**
 Aspose.Diagram API unterstützt die automatische Anpassung der Zeichnung Visio. Diese Feature-Operation hilft, äußere Formen innerhalb der Visio-Seitenbegrenzung zu bringen. Aspose.Diagram for .NET API hat die[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) Klasse, die eine Visio-Zeichnung darstellt. Das[DiagrammSaveOptions](https://reference.aspose.com/diagram/net/aspose.diagram.saving/diagramsaveoptions) -Klasse macht die AutoFitPageToDrawingContent-Eigenschaft verfügbar, um die Visio-Zeichnung automatisch anzupassen.

Dieses Beispiel funktioniert wie folgt:

1. Erstellen Sie ein Objekt der Klasse Diagram.
1. Erstellen Sie ein Objekt der Klasse DiagramSaveOptions und übergeben Sie das resultierende Dateiformat.
1. Legen Sie die AutoFitPageToDrawingContent-Eigenschaft des DiagramSaveOptions-Objekts fest.
1. Rufen Sie die Save-Methode des Klassenobjekts Diagram auf und übergeben Sie auch den vollständigen Dateipfad und das DiagramSaveOptions-Objekt.
### **Programmierbeispiel für automatische Anpassung**
Der folgende Beispielcode zeigt, wie Formen in Visio diagram automatisch angepasst werden.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Diagrams();

// Load a Visio diagram
Diagram diagram = new Diagram(dataDir + "BFlowcht.vsdx");

// Use saving options
DiagramSaveOptions options = new DiagramSaveOptions(SaveFileFormat.VSDX);
// Set Auto fit page property
options.AutoFitPageToDrawingContent = true;

// Save Visio diagram
diagram.Save(dataDir + "AutoFitShapesInVisio_out.vsdx", options);

{{< /highlight >}}
```
## **Arbeiten mit VBA-Projekt**
### **Ändern Sie den VBA-Modulcode in Visio Diagram**
 Dieser Artikel zeigt, wie Sie einen VBA-Modulcode automatisch mit Aspose.Diagram for .NET ändern. Wir haben hinzugefügt[VbaModul](http://www.aspose.com/api/net/diagram/aspose.diagram.vba/VbaModule), [VbaModuleCollection](http://www.aspose.com/api/net/diagram/aspose.diagram.vba/VbaModuleCollection), [VbaProjekt](http://www.aspose.com/api/net/diagram/aspose.diagram.vba/VbaProject), [VbaProjectReference](http://www.aspose.com/api/net/diagram/aspose.diagram.vba/VbaProjectReference) und[VbaProjectReferenceCollection](http://www.aspose.com/api/net/diagram/aspose.diagram.vba/VbaProjectReferenceCollection) Klassen. Diese Klassen helfen dabei, die Kontrolle über das VBA-Projekt zu erlangen. Entwickler können VBA-Modulcode extrahieren und ändern.
### **Programmierbeispiel für VBA-Modulcode ändern**
Bitte überprüfen Sie dieses Codebeispiel:

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Diagrams();

// Load an existing Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdm", LoadFileFormat.VSDM);
// Extract VBA project
Aspose.Diagram.Vba.VbaProject v = diagram.VbaProject;
// Iterate through the modules and modify VBA module code
foreach (VbaModule module in diagram.VbaProject.Modules)
{
    string code = module.Codes;
    if (code.Contains("This is test message."))
        code = code.Replace("This is test message.", "This is Aspose.Diagram message.");
    module.Codes = code;
}
// Save the Visio diagram
diagram.Save(dataDir + "ModifyVBAModule_out.vssm", SaveFileFormat.VSSM);

{{< /highlight >}}
```
### **Entfernen Sie alle Makros aus Visio Diagram**
 Aspose.Diagram for .NET ermöglicht Entwicklern das Entfernen aller Makros aus Visio diagram. Die VbProjectData-Eigenschaft, die von der[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) Klasse können Sie alle Makros aus der Zeichnung Visio entfernen.
### **Programmierbeispiel für alle Makros entfernen**
```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Diagrams();

// Load a Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Remove all macros
diagram.VbProjectData = null;

// Save diagram
diagram.Save(dataDir + "RemoveMacrosFromVisio_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Erstellen eines neuen Diagram mit VSTO**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/)ermöglicht Entwicklern das Erstellen und Arbeiten mit Microsoft Office Visio Diagrammen und die Integration von Funktionen in ihre Softwareanwendungen. Es gibt andere Möglichkeiten, mit Visio-Dateien zu arbeiten, am häufigsten Microsoft-Automatisierung. Leider hat das einige Einschränkungen. Aspose.Diagram ist leistungsstark und schnell und arbeitet selbstständig ohne Microsoft Office Installation.

 Dieser Migrationsartikel zeigt die Verwendung von first[VSTO](https://docs.aspose.com/diagram/net/create-update-layout-and-auto-fit-shapes/) und dann[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) um eine neue diagram zu erstellen und ihr einige Formen hinzuzufügen. Sie werden feststellen, dass der Code Aspose.Diagram kürzer als der VSTO-Code ist. Sie können den Code gerne als Grundlage für Ihre eigene Entwicklung verwenden und ihn Ihren Anforderungen entsprechend erweitern. Mit VSTO können Sie mit Microsoft-Visio-Dateien programmieren. So erstellen Sie eine neue diagram:

1. Erstellen Sie ein Visio-Anwendungsobjekt.
1. Machen Sie das Anwendungsobjekt unsichtbar.
1. Erstellen Sie eine leere diagram.
1. Fügen Sie Formen aus Visio-Mastern (Schablonen) hinzu.
1. Speichern Sie die Datei als VDX.
### **Neues Diagram mit VSTO-Programmierbeispiel erstellen**
{{% alert color="primary" %}}

mit Visio = Microsoft.Office.Interop.Visio;
Importe Visio = Microsoft.Office.Interop.Visio

{{% /alert %}}


**Beispiel:**

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_KnowledgeBase();

Visio.Application vdxApp = null;
Visio.Document vdxDoc = null;
try
{
    // Create Visio Application Object
    vdxApp = new Visio.Application();

    // Make Visio Application Invisible
    vdxApp.Visible = false;

    // Create a new diagram
    vdxDoc = vdxApp.Documents.Add("");

    // Load Visio Stencil
    Visio.Documents visioDocs = vdxApp.Documents;
    Visio.Document visioStencil = visioDocs.OpenEx("Basic Shapes.vss",
        (short)Microsoft.Office.Interop.Visio.VisOpenSaveArgs.visOpenHidden);

    // Set active page
    Visio.Page visioPage = vdxApp.ActivePage;

    // Add a new rectangle shape
    Visio.Master visioRectMaster = visioStencil.Masters.get_ItemU(@"Rectangle");
    Visio.Shape visioRectShape = visioPage.Drop(visioRectMaster, 4.25, 5.5);
    visioRectShape.Text = @"Rectangle text.";

    // Add a new star shape
    Visio.Master visioStarMaster = visioStencil.Masters.get_ItemU(@"Star 7");
    Visio.Shape visioStarShape = visioPage.Drop(visioStarMaster, 2.0, 5.5);
    visioStarShape.Text = @"Star text.";

    // Add a new hexagon shape
    Visio.Master visioHexagonMaster = visioStencil.Masters.get_ItemU(@"Hexagon");
    Visio.Shape visioHexagonShape = visioPage.Drop(visioHexagonMaster, 7.0, 5.5);
    visioHexagonShape.Text = @"Hexagon text.";


    // Save diagram as VDX
    vdxDoc.SaveAs(dataDir + "CreatingDiagramWithVSTO_out.vdx");
}
catch (Exception ex)
{
    Console.WriteLine(ex.Message + "\nThis example will only work if you apply a valid Aspose License. You can purchase full license or get 30 day temporary license from http:// Www.aspose.com/purchase/default.aspx.");
}
            

{{< /highlight >}}
```
## **Erstellen einer neuen Diagram mit Aspose.Diagram for .NET**
Mit Aspose.Diagram API benötigen Entwickler keine Microsoft Office Visio Installation auf der Maschine und können unabhängig von Microsoft Office Automation arbeiten.

So erstellen Sie eine neue diagram:

1. Erstellen Sie eine leere diagram.
1. Fügen Sie Formen aus Visio-Mastern (Schablonen) hinzu.
1. Speichern Sie die Datei als VDX.
### **Neu Diagram mit Aspose.Diagram for .NET Programmierbeispiel**
{{% alert color="primary" %}}

mit Aspose.Diagram;
Importiert Aspose.Diagram

{{% /alert %}}

Beispiel:

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_KnowledgeBase();

// Create a new diagram
Diagram diagram = new Diagram(dataDir + "Basic Shapes.vss");

// Add a new rectangle shape
long shapeId = diagram.AddShape(4.25, 5.5, 2, 1, @"Rectangle", 0);
Shape shape = diagram.Pages[0].Shapes.GetShape(shapeId);
shape.Text.Value.Add(new Txt(@"Rectangle text."));

// Add a new star shape
shapeId = diagram.AddShape(2.0, 5.5, 2, 2, @"Star 7", 0);
shape = diagram.Pages[0].Shapes.GetShape(shapeId);
shape.Text.Value.Add(new Txt(@"Star text."));

// Add a new hexagon shape
shapeId = diagram.AddShape(7.0, 5.5, 2, 2, @"Hexagon", 0);
shape = diagram.Pages[0].Shapes.GetShape(shapeId);
shape.Text.Value.Add(new Txt(@"Hexagon text."));

// Save the new diagram
diagram.Save(dataDir + "CreatingDiagramWithAspose_out.vdx", SaveFileFormat.VDX);

{{< /highlight >}}
```
## **Shape-Eigenschaften aktualisieren**
 Bei der Arbeit mit Microsoft Visio Diagrammen können Benutzer Formattribute aktualisieren, einschließlich Text, Stil, Position, Höhe und Breite. Als Softwareentwickler, der mit Visio-Dateien arbeitet, werden Sie aufgefordert, dies programmgesteuert zu tun. Die gute Nachricht ist, dass es möglich ist, entweder die Mechanismen zum Programmieren mit Visio-Dateien zu verwenden, die Microsoft bereitstellt, VSTO, oder zu verwenden[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/).

 Das folgende Thema zeigt die Verwendung[VSTO](https://products.aspose.com/diagram/net/) und[Aspose.Diagram](https://products.aspose.com/diagram/net/) Formeigenschaften zu aktualisieren. Die folgenden Codeausschnitte zeigen, wie Formeigenschaften für VSTO und Aspose.Diagram for .NET aktualisiert werden. Sie können den Code gerne verwenden und auf Ihre spezielle Situation anwenden.
### **Aktualisieren von Shape-Eigenschaften mit VSTO**
Mit VSTO können Sie mit Microsoft Visio-Dateien programmieren. So aktualisieren Sie Formeigenschaften:

1. Erstellen Sie ein Visio-Anwendungsobjekt.
1. Machen Sie das Anwendungsobjekt unsichtbar.
1. Öffnen Sie eine vorhandene Visio VSD-Datei.
1. Finden Sie die gewünschte Form.
1. Aktualisieren Sie die Formeigenschaften (Text, Textstil, Position und Größe).
1. Speichern Sie die Datei als VDX.
#### **Aktualisieren von Shape-Eigenschaften mit VSTO-Programmierbeispiel**
{{% alert color="primary" %}}

mit Visio = Microsoft.Office.Interop.Visio;
Importe Visio = Microsoft.Office.Interop.Visio

{{% /alert %}}

**Beispiel:**

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_KnowledgeBase();

Visio.Application vsdApp = null;
Visio.Document vsdDoc = null;
try
{
    // Create Visio Application Object
    vsdApp = new Visio.Application();

    // Make Visio Application Invisible
    vsdApp.Visible = false;

    // Create a document object and load a diagram
    vsdDoc = vsdApp.Documents.Open(dataDir + "Drawing1.vsd");

    // Create page object to get required page
    Visio.Page page = vsdApp.ActivePage;

    // Create shape object to get required shape
    Visio.Shape shape = page.Shapes["Process1"];

    // Set shape text and text style
    shape.Text = "Hello World";
    shape.TextStyle = "CustomStyle1";

    // Set shape's position
    shape.get_Cells("PinX").ResultIU = 5;
    shape.get_Cells("PinY").ResultIU = 5;

    // Set shape's height and width
    shape.get_Cells("Height").ResultIU = 2;
    shape.get_Cells("Width").ResultIU = 3;

    // Save file as VDX
    vsdDoc.SaveAs(dataDir + "Drawing1.vdx");
}
catch (Exception ex)
{
    Console.WriteLine(ex.Message + "\nThis example will only work if you apply a valid Aspose License. You can purchase full license or get 30 day temporary license from http:// Www.aspose.com/purchase/default.aspx.");
}           

{{< /highlight >}}
```
### **Aktualisieren der Shape-Eigenschaften mit Aspose.Diagram for .NET**
Mit Aspose.Diagram API benötigen Entwickler keine Microsoft Office Visio auf der Maschine und können unabhängig von Microsoft Office Automation arbeiten.

So aktualisieren Sie Formeigenschaften mit Aspose.Diagram for .NET:

1. Öffnen Sie eine vorhandene Visio VSD-Datei.
1. Finden Sie die gewünschte Form.
1. Aktualisieren Sie die Formeigenschaften (Text, Textstil, Position und Größe).
1. Speichern Sie die Datei als VDX.
#### **Aktualisieren von Shape-Eigenschaften mit Aspose.Diagram for .NET Programmierbeispiel**
{{% alert color="primary" %}}

mit Aspose.Diagram;
Importiert Aspose.Diagram

{{% /alert %}}

**Beispiel:**

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
try
{
    // The path to the documents directory.
    string dataDir = RunExamples.GetDataDir_KnowledgeBase();

    // Save the uploaded file as PDF
    Diagram diagram = new Diagram(dataDir + "Drawing1.vsd");

    // Find a particular shape and update its properties
    foreach (Aspose.Diagram.Shape shape in diagram.Pages[0].Shapes)
    {
        if (shape.Name.ToLower() == "process1")
        {
            shape.Text.Value.Clear();
            shape.Text.Value.Add(new Txt("Hello World"));

            // Find custom style sheet and set as shape's text style
            foreach (StyleSheet styleSheet in diagram.StyleSheets)
            {
                if (styleSheet.Name == "CustomStyle1")
                {
                    shape.TextStyle = styleSheet;
                }
            }

            // Set horizontal and vertical position of the shape
            shape.XForm.PinX.Value = 5;
            shape.XForm.PinY.Value = 5;

            // Set height and width of the shape
            shape.XForm.Height.Value = 2;
            shape.XForm.Width.Value = 3;
        }
    }

    // Save shape as VDX
    diagram.Save(dataDir + "UpdateShapePropsWithAspose_out.vdx", SaveFileFormat.VDX);
}
catch (Exception ex)
{
    Console.WriteLine(ex.Message);
}

{{< /highlight >}}
```
