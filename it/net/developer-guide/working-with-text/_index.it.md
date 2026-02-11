---
title: Lavorare con il testo
type: docs
weight: 90
url: /it/net/working-with-text/
description: Questa sezione spiega come inserire una forma di testo o aggiornare il testo della forma con Aspose.Diagram.
---
## **Inserisci una forma di testo nella pagina Visio**
 Aspose.Diagram API consente agli sviluppatori di inserire una forma di testo ovunque nella pagina Visio. Per ottenere ciò, il metodo AddText di[Pagina](http://www.aspose.com/api/net/diagram/aspose.diagram/page) class accetta i parametri PinX, PinY, larghezza, altezza e testo.
### **Inserisci un esempio di programmazione di forme di testo**
Il seguente pezzo di codice aggiunge una forma di testo nel Visio diagram.

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
## **Aggiorna Visio Forma testo**
 Così come[creazione di diagrammi](/diagram/it/net/load-or-create-a-visio-drawing/) , Aspose.Diagram for .NET consente di lavorare con le forme in modi diversi. Questo articolo illustra come accedere e aggiornare il testo nelle forme. La proprietà Text, esposta da[Forma](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class, supporta l'oggetto Aspose.Diagram.Text. La proprietà può essere utilizzata per recuperare o aggiornare il testo di una forma. Il processo per aggiornare il testo di una forma è semplice:

1. Carica un diagram.
1. Trova una forma particolare.
1. Imposta il nuovo testo.
1. Salva lo diagram.
### **Aggiornamento dell'esempio di programmazione del testo della forma**
Il seguente pezzo di codice aggiorna il testo di una forma. Le forme sono identificate dai relativi ID. I segmenti di codice seguenti cercano una forma chiamata processo e con l'ID 1 e ne modificano il testo.

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
## **Applicare il foglio di stile integrato o personalizzato a una forma Visio**
fogli di stile Microsoft Visio memorizzano le informazioni di formattazione che possono essere applicate alle forme per un aspetto coerente. Aspose.Diagram for .NET consente di applicare fogli di stile dall'interno di un'applicazione.

 Le proprietà TextStyle, FillStyle e LineStyle esposte da[Forma](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) classe sostenere il[Aspose.Diagram.StyleSheet](http://www.aspose.com/api/net/diagram/aspose.diagram/stylesheet) oggetto. La proprietà può essere utilizzata per recuperare informazioni sullo stile e applicare stili di testo, linea e riempimento personalizzati a un diagram.
### **Stili personalizzati in Microsoft Visio**
Per applicare stili personalizzati alle forme in Microsoft Visio:

1. Apri uno diagram in Microsoft Visio.
1.  Selezionare**Definisci stili** dal**Formato** menu (Visio 2007) o fare clic con il pulsante destro del mouse**Stili** nel**Esploratore di disegni** finestra e selezionare**Definisci stili** (Visio 2010).
1.  Nel**Definisci stili** finestra di dialogo, digitare un nuovo nome per il foglio di stile personalizzato. Ad esempio, CustomStyle1.
1.  Clicca il**Testo**, **Linea** e**Riempire** pulsanti per impostare rispettivamente gli stili di testo, linea e riempimento.
1.  Clic**OK**.

Dopo aver definito i fogli di stile personalizzati in Microsoft Visio, utilizzare il seguente codice in un'applicazione .NET per applicare stili personalizzati alle forme. Si noti che gli esempi di codice seguenti richiamano il foglio di stile personalizzato definito sopra: è necessario conoscere il nome e la posizione del foglio che si applica. Per applicare gli stili personalizzati a livello di codice:

1. Carica un diagram.
1. Trova la forma a cui vuoi applicare uno stile.
1. Carica il foglio di stile.
1. Applicare stili.
1. Salva lo diagram.
#### **Applicare l'esempio di programmazione di stili personalizzati**
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
## **Applica uno stile diverso a ciascun valore di testo di una forma**
 Così come[creazione di diagrammi](/diagram/it/net/load-or-create-a-visio-drawing/), Aspose.Diagram for .NET consente di lavorare con le forme in modi diversi. Questo articolo aiuta ad aggiungere più valori di testo a una forma e ad applicare uno stile diverso a ogni valore di testo.

{{% alert color="primary" %}} 

L'elemento Shape contiene un elemento chiamato Text, che contiene i caratteri del testo e gli elementi speciali (cp, pp, tp e fld) che segnano la fine di un'esecuzione e l'inizio della successiva. L'elemento Char contiene gli attributi di formattazione per il testo della forma, come carattere, colore, stile del testo, maiuscole e minuscole, posizione rispetto alla linea di base e dimensione in punti.

{{% /alert %}} 
### **Aggiunta di forme di testo e stili**

|**Inserisci diagram**|
|:- |
|![cose da fare:immagine_alt_testo](working-with-text_1.png)|


|**Diagram dopo aver aggiunto vari valori di testo a una forma con uno stile diverso su ciascun valore di testo**|
|:- |
|![cose da fare:immagine_alt_testo](working-with-text_2.png)|
#### **Esempio di programmazione dell'aggiunta di testo e stili**
Il seguente pezzo di codice aggiunge il testo di una forma e diversi stili.

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
## **Trova e sostituisci il testo di una forma**
 Il[Testo](http://www.aspose.com/api/net/diagram/aspose.diagram/txt) La classe ti consente di modificare il testo della forma. Il metodo Replace, esposto da[Testo](http://www.aspose.com/api/net/diagram/aspose.diagram/txt) class, supporta la modifica del testo di una forma.
Gli esempi di codice in questo articolo trovano e sostituiscono il testo della forma nella pagina.

|**Inserisci diagram**|
|:- |
|![cose da fare:immagine_alt_testo](working-with-text_3.png)|


|**Il diagram dopo che la forma è stata modificata**|
|:- |
|![cose da fare:immagine_alt_testo](working-with-text_4.png)|
Il processo per modificare il testo della forma:

1. Carica un diagram.
1. Trova un particolare testo di una forma.
1. Sostituisci il testo di questa forma
1. Salva lo diagram.
### **Esempio di programmazione di testo Trova e sostituisci**
I frammenti di codice seguenti mostrano come modificare il testo della forma. Il codice scorre le forme di una pagina.

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
## **Estrai testo normale dalla pagina Visio Diagram**
Aspose.Diagram API consente agli sviluppatori di estrarre testo normale dalla pagina Visio diagram. Possono anche scorrere le pagine Visio diagram per coprire l'intero testo Visio diagram.

 Microsoft Office Visio aggiunge il testo alle forme. Il[Forma](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class contiene un elemento chiamato Text, che contiene i caratteri del testo e gli elementi speciali (cp, pp, tp e fld) che segnano la fine di un'esecuzione e l'inizio della successiva.
### **Estrai un esempio di programmazione in testo normale**
La parte di codice seguente scorre le forme della pagina Visio e filtra il testo normale senza informazioni di formattazione.

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
