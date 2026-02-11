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

```
{{< highlight "csharp" >}}
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
```
## **Uppdatering Visio Formtext**
 Såväl som[skapa diagram](/diagram/sv/net/load-or-create-a-visio-drawing/) , Aspose.Diagram for .NET låter dig arbeta med former på olika sätt. Den här artikeln tittar på hur du kommer åt och uppdaterar text i former. Text-egenskapen, exponerad av[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) klass, stöder objektet Aspose.Diagram.Text. Egenskapen kan användas för att hämta eller uppdatera en forms text. Processen för att uppdatera en forms text är enkel:

1. Ladda ett diagram.
1. Hitta en viss form.
1. Ställ in den nya texten.
1. Spara diagram.
### **Uppdatera formtextprogrammeringsexempel**
Följande kodbit uppdaterar en forms text. Former identifieras med deras ID. Kodsegmenten nedan letar efter en form som kallas process och med ID 1 och ändrar dess text.

```
{{< highlight "csharp" >}}
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
```
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
```
{{< highlight "csharp" >}}
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
```
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

```
{{< highlight "csharp" >}}
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
```
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

```
{{< highlight "csharp" >}}
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
```
## **Extrahera vanlig text från sidan Visio Diagram**
Aspose.Diagram API tillåter utvecklare att extrahera vanlig text från sidan Visio diagram. De kan också iterera genom sidorna Visio diagram för att täcka hela texten Visio diagram.

 Microsoft Office Visio lägger till texten i formerna. De[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) klass innehåller ett element som heter Text, som innehåller tecknen i texten och specialelement (cp, pp, tp och fld) som markerar slutet på en körning och början på nästa.
### **Extrahera programmeringsexempel för vanlig text**
Följande kodbit itererar genom formerna på sidan Visio och filtrerar vanlig text utan att formatera information.

```
{{< highlight "csharp" >}}
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
```
