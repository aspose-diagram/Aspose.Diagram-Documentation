---
title: Arbeiten mit Text
type: docs
weight: 90
url: /de/net/working-with-text/
description: In diesem Abschnitt wird erläutert, wie Sie eine Textform einfügen oder den Text der Form mit Aspose.Diagram aktualisieren.
---
## **Fügen Sie eine Textform in die Seite Visio ein**
 Mit Aspose.Diagram API können Entwickler überall auf der Visio-Seite eine Textform einfügen. Um dies zu erreichen, wird die AddText-Methode des[Buchseite](http://www.aspose.com/api/net/diagram/aspose.diagram/page) Die Klasse nimmt PinX-, PinY-, Breiten-, Höhen- und Textparameter an.
### **Fügen Sie ein Textform-Programmierbeispiel ein**
Der folgende Codeabschnitt fügt eine Textform in Visio diagram hinzu.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_ShapeText();

// Create a new diagram
Diagram diagram = new Diagram();
// Set parameters and add text to a Visio page
double PinX = 1, PinY = 1, Width = 1, Height = 1;                  
diagram.Pages[0].AddText(PinX, PinY, Width, Height, "Test text");
// Save diagram 
diagram.Save(dataDir + "InsertTextShape_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Aktualisieren Sie Visio Shape-Text**
 Ebenso gut wie[Diagramme erstellen](/diagram/de/net/load-or-create-a-visio-drawing/) , Aspose.Diagram for .NET lässt Sie auf unterschiedliche Weise mit Formen arbeiten. In diesem Artikel wird beschrieben, wie Sie auf Text in Formen zugreifen und ihn aktualisieren. Die Text-Eigenschaft, verfügbar gemacht durch die[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) Klasse, unterstützt das Objekt Aspose.Diagram.Text. Die Eigenschaft kann verwendet werden, um den Text einer Form abzurufen oder zu aktualisieren. Der Vorgang zum Aktualisieren des Texts einer Form ist unkompliziert:

1. Laden Sie eine diagram.
1. Finden Sie eine bestimmte Form.
1. Legen Sie den neuen Text fest.
1. Speichern Sie die diagram.
### **Programmierbeispiel für Formtext aktualisieren**
Der folgende Codeabschnitt aktualisiert den Text einer Form. Shapes werden anhand ihrer IDs identifiziert. Die folgenden Codesegmente suchen nach einer Form namens process und mit der ID 1 und ändern ihren Text.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_ShapeText();

// Call the diagram constructor to load diagram from a VDX file
Diagram diagram = new Diagram(dataDir + "UpdateShapeText.vsd");
// Get page by name
Page page = diagram.Pages.GetPage("Flow 1");
// Find a particular shape and update its text
foreach (Aspose.Diagram.Shape shape in page.Shapes)
{
    if (shape.NameU.ToLower() == "process" && shape.ID == 1)
    {
        shape.Text.Value.Clear();
        shape.Text.Value.Add(new Txt("New Text"));
    }
}
// Save diagram
diagram.Save(dataDir + "UpdateShapeText_out.vdx", SaveFileFormat.VDX);

{{< /highlight >}}

## **Wenden Sie ein integriertes oder benutzerdefiniertes Stylesheet auf eine Visio-Form an**
Microsoft Visio Stylesheets speichern Formatierungsinformationen, die für ein konsistentes Erscheinungsbild auf Formen angewendet werden können. Mit Aspose.Diagram for .NET können Sie Stylesheets aus einer Anwendung heraus anwenden.

 Die Eigenschaften TextStyle, FillStyle und LineStyle, die von der bereitgestellt werden[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) Klasse unterstützt die[Aspose.Diagram.StyleSheet](http://www.aspose.com/api/net/diagram/aspose.diagram/stylesheet) Objekt. Die Eigenschaft kann verwendet werden, um Stilinformationen abzurufen und benutzerdefinierte Text-, Linien- und Füllstile auf einen diagram anzuwenden.
### **Benutzerdefinierte Stile unter Microsoft Visio**
So wenden Sie benutzerdefinierte Stile auf Formen in Microsoft Visio an:

1. Öffnen Sie eine diagram in Microsoft Visio.
1.  Auswählen**Stile definieren** von dem**Format** Menü (Visio 2007), oder klicken Sie mit der rechten Maustaste**Stile** in dem**Zeichnungs-Explorer** Fenster und wählen Sie aus**Stile definieren** (Visio 2010).
1.  In dem**Stile definieren** Geben Sie im Dialogfeld einen neuen Namen für Ihr benutzerdefiniertes Stylesheet ein. Beispiel: CustomStyle1.
1.  Drücke den**Text**, **Linie** und**Füllen** Schaltflächen zum Festlegen von Text-, Linien- und Füllstilen.
1.  Klicken**OK**.

Nachdem Sie benutzerdefinierte Stylesheets in Microsoft Visio definiert haben, verwenden Sie den folgenden Code in einer .NET-Anwendung, um benutzerdefinierte Stile auf Ihre Formen anzuwenden. Beachten Sie, dass die folgenden Codebeispiele das oben definierte benutzerdefinierte Stylesheet aufrufen: Sie müssen den Namen und den Speicherort des angewendeten Sheets kennen. So wenden Sie benutzerdefinierte Stile programmgesteuert an:

1. Laden Sie eine diagram.
1. Suchen Sie die Form, auf die Sie einen Stil anwenden möchten.
1. Laden Sie das Stylesheet.
1. Stile anwenden.
1. Speichern Sie die diagram.
#### **Wenden Sie das Programmierbeispiel für benutzerdefinierte Stile an**

{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_ShapeText();

// Load diagram
Diagram vsdDiagram = new Diagram(dataDir + "ApplyCustomStyleSheets.vsd");
// Get page by name
Page page = vsdDiagram.Pages.GetPage("Flow 1");

Shape sourceShape = null;
// Find the shape to apply the style
foreach (Aspose.Diagram.Shape shape in page.Shapes)
{
    if (shape.Name == "Process")
    {
        sourceShape = shape;
        break;
    }
}

StyleSheet customStyleSheet = null;

// Find the required style sheet
foreach (StyleSheet styleSheet in vsdDiagram.StyleSheets)
{
    if (styleSheet.Name == "Basic")
    {
        customStyleSheet = styleSheet;
        break;
    }
}

if (sourceShape != null && customStyleSheet != null)
{
    // Apply text style
    sourceShape.TextStyle = customStyleSheet;
    // Apply fill style
    sourceShape.FillStyle = customStyleSheet;
    // Apply line style
    sourceShape.LineStyle = customStyleSheet;
}

// Save changed diagram as VDX
vsdDiagram.Save(dataDir + "ApplyCustomStyleSheets_out.vdx", SaveFileFormat.VDX);

{{< /highlight >}}

## **Wenden Sie einen anderen Stil auf die einzelnen Textwerte einer Form an**
 Ebenso gut wie[Diagramme erstellen](/diagram/de/net/load-or-create-a-visio-drawing/), Aspose.Diagram for .NET lässt Sie auf unterschiedliche Weise mit Formen arbeiten. Dieser Artikel hilft beim Hinzufügen mehrerer Textwerte zu einer Form und beim Anwenden eines anderen Stils auf jeden Textwert.

{{% alert color="primary" %}} 

Das Shape-Element enthält ein Element namens Text, das die Zeichen des Textes und spezielle Elemente (cp, pp, tp und fld) enthält, die das Ende eines Laufs und den Beginn des nächsten markieren. Char-Element enthält die Formatierungsattribute für den Text der Form, z. B. Schriftart, Farbe, Textstil, Groß-/Kleinschreibung, Position relativ zur Grundlinie und Punktgröße.

{{% /alert %}} 
### **Hinzufügen von Formtext und -stilen**

|**Geben Sie diagram ein**|
|:- |
|![todo: Bild_alt_Text](working-with-text_1.png)|


|**Diagram nach dem Hinzufügen verschiedener Textwerte zu einer Form mit unterschiedlichem Stil für jeden Textwert**|
|:- |
|![todo: Bild_alt_Text](working-with-text_2.png)|
#### **Hinzufügen von Text und Stilen Programmierbeispiel**
Der folgende Codeabschnitt fügt den Text einer Form und verschiedene Stile hinzu.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_ShapeText();

// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-1");
// Get shape by ID
Shape shape = page.Shapes.GetShape(1);
// Clear shape text values and chars
shape.Text.Value.Clear();
shape.Chars.Clear();

// Mark character run and add text
shape.Text.Value.Add(new Cp(0));
shape.Text.Value.Add(new Txt("TextStyle_Regular\n"));
shape.Text.Value.Add(new Cp(1));
shape.Text.Value.Add(new Txt("TextStyle_Bold_Italic\n"));
shape.Text.Value.Add(new Cp(2));
shape.Text.Value.Add(new Txt("TextStyle_Underline_Italic\n"));
shape.Text.Value.Add(new Cp(3));
shape.Text.Value.Add(new Txt("TextStyle_Bold_Italic_Underline"));

// Add formatting characters
shape.Chars.Add(new Aspose.Diagram.Char());
shape.Chars.Add(new Aspose.Diagram.Char());
shape.Chars.Add(new Aspose.Diagram.Char());
shape.Chars.Add(new Aspose.Diagram.Char());

// Set properties e.g. color, font, size and style etc.
shape.Chars[0].IX = 0;
shape.Chars[0].Color.Value = "#FF0000";
shape.Chars[0].Font.Value = 4;
shape.Chars[0].Size.Value = 0.22;
shape.Chars[0].Style.Value = StyleValue.Undefined;

// Set properties e.g. color, font, size and style etc.
shape.Chars[1].IX = 1;
shape.Chars[1].Color.Value = "#FF00FF";
shape.Chars[1].Font.Value = 4;
shape.Chars[1].Size.Value = 0.22;
shape.Chars[1].Style.Value = StyleValue.Bold | StyleValue.Italic;

// Set properties e.g. color, font, size and style etc.
shape.Chars[2].IX = 2;
shape.Chars[2].Color.Value = "#00FF00";
shape.Chars[2].Font.Value = 4;
shape.Chars[2].Size.Value = 0.22;
shape.Chars[2].Style.Value = StyleValue.Underline | StyleValue.Italic;

// Set properties e.g. color, font, size and style etc.
shape.Chars[3].IX = 3;
shape.Chars[3].Color.Value = "#3333FF";
shape.Chars[3].Font.Value = 4;
shape.Chars[3].Size.Value = 0.22;
shape.Chars[3].Style.Value = StyleValue.Bold | StyleValue.Italic | StyleValue.Underline;
// Save diagram
diagram.Save(dataDir + "ApplyFontOnText_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Suchen und ersetzen Sie den Text einer Form**
 Das[Txt](http://www.aspose.com/api/net/diagram/aspose.diagram/txt) Mit der Klasse können Sie den Text der Form bearbeiten. Die Replace-Methode, verfügbar gemacht durch die[Txt](http://www.aspose.com/api/net/diagram/aspose.diagram/txt) Klasse, unterstützen Sie das Ändern des Textes einer Form.
Die Codebeispiele in diesem Artikel suchen und ersetzen den Text der Form auf der Seite.

|**Geben Sie diagram ein**|
|:- |
|![todo: Bild_alt_Text](working-with-text_3.png)|


|**Die diagram, nachdem die Form bearbeitet wurde**|
|:- |
|![todo: Bild_alt_Text](working-with-text_4.png)|
Der Prozess zum Ändern des Textes der Form:

1. Laden Sie eine diagram.
1. Finden Sie einen bestimmten Text einer Form.
1. Text dieser Form ersetzen
1. Speichern Sie die diagram.
### **Programmierbeispiel zum Suchen und Ersetzen von Text**
Die folgenden Codeausschnitte zeigen, wie der Text der Form geändert werden kann. Der Code durchläuft die Shapes einer Seite.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_ShapeText();

// Prepare a collection old and new text
Dictionary<string, string> replacements = new Dictionary<string, string>();
replacements.Add("[[CompanyName]]", "Research Society of XYZ");
replacements.Add("[[EmployeeName]]", "James Bond");
replacements.Add("[[SubjectTitle]]", "The affect of the internet on social behavior in the industrialize world");
replacements.Add("[[TimePeriod]]", DateTime.Now.AddYears(-1).ToString("dd/MMMM/yyyy") + " -- " + DateTime.Now.ToString("dd/MMMM/yyyy"));
replacements.Add("[[SubmissionDate]]", DateTime.Now.AddDays(-7).ToString("dd/MMMM/yyyy"));
replacements.Add("[[AmountReq]]", "$100,000");
replacements.Add("[[DateApproved]]", DateTime.Now.AddDays(1).ToString("dd/MMMM/yyyy"));

// Load diagram
Diagram diagram = new Diagram(dataDir + "FindReplaceText.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-1");

// Iterate through the shapes of a page
foreach (Shape shape in page.Shapes)
{
    foreach (KeyValuePair<string, string> kvp in replacements)
    {
        foreach (FormatTxt txt in shape.Text.Value)
        {
            Txt tx = txt as Txt;
            if (tx != null && tx.Text.Contains(kvp.Key))
            {
                // Find and replace text of a shape
                tx.Text = tx.Text.Replace(kvp.Key, kvp.Value);
            }
        }
    }
}
// Save the diagram
diagram.Save(dataDir + "FindAndReplaceShapeText_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Extrahieren Sie Klartext von der Seite Visio Diagram**
Aspose.Diagram API ermöglicht es Entwicklern, Klartext aus der Seite Visio diagram zu extrahieren. Sie können auch die Visio diagram-Seiten durchlaufen, um den gesamten Visio diagram-Text abzudecken.

 Microsoft Office Visio fügt den Text zu den Formen hinzu. Das[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) Klasse enthält ein Element namens Text, das die Zeichen des Textes und spezielle Elemente (cp, pp, tp und fld) enthält, die das Ende eines Laufs und den Beginn des nächsten markieren.
### **Extrahieren Sie ein Klartext-Programmierbeispiel**
Der folgende Codeabschnitt durchläuft die Formen der Seite Visio und filtert einfachen Text ohne Formatierungsinformationen.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
static string text = "";
public static void Run()
{
    // The path to the documents directory.
    string dataDir = RunExamples.GetDataDir_ShapeText();
    // Load diagram
    Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

    // Get Visio diagram page
    Aspose.Diagram.Page page = diagram.Pages.GetPage("Page-1");

    // Iterate through the shapes
    foreach (Aspose.Diagram.Shape shape in page.Shapes)
    {
        // Extract plain text from the shape
        GetShapeText(shape);
    }
    // Display extracted text
    Console.WriteLine(text);
}
private static void GetShapeText(Aspose.Diagram.Shape shape)
{
    // Filter shape text
    if (shape.Text.Value.Text != "")
        text += Regex.Replace(shape.Text.Value.Text, "\\<.*?>", "");

    // For image shapes
    if (shape.Type == TypeValue.Foreign)
        text += (shape.Name);

    // For group shapes
    if (shape.Type == TypeValue.Group)
        foreach (Aspose.Diagram.Shape subshape in shape.Shapes)
        {
            GetShapeText(subshape);
        }
}

{{< /highlight >}}

