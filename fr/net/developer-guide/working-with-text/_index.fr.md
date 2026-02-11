---
title: Travailler avec du texte
type: docs
weight: 90
url: /fr/net/working-with-text/
description: Cette section explique comment insérer une forme de texte ou mettre à jour le texte de la forme avec Aspose.Diagram.
---
## **Insérer une forme de texte dans la page Visio**
 Aspose.Diagram API permet aux développeurs d'insérer une forme de texte n'importe où dans la page Visio. Pour ce faire, la méthode AddText de la[Page](http://www.aspose.com/api/net/diagram/aspose.diagram/page) La classe prend les paramètres PinX, PinY, largeur, hauteur et texte.
### **Insérer un exemple de programmation de forme de texte**
Le morceau de code suivant ajoute une forme de texte dans le Visio diagram.


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

## **Mise à jour Visio Texte de forme**
 Aussi bien que[création de diagrammes](/diagram/fr/net/load-or-create-a-visio-drawing/) , Aspose.Diagram for .NET vous permet de travailler avec des formes de différentes manières. Cet article explique comment accéder au texte et le mettre à jour dans les formes. La propriété Text, exposée par le[Forme](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) classe, prend en charge l'objet Aspose.Diagram.Text. La propriété peut être utilisée pour récupérer ou mettre à jour le texte d'une forme. Le processus de mise à jour du texte d'une forme est simple :

1. Charger un diagram.
1. Trouvez une forme particulière.
1. Définissez le nouveau texte.
1. Enregistrez le diagram.
### **Mise à jour de l'exemple de programmation de texte de forme**
Le morceau de code suivant met à jour le texte d'une forme. Les formes sont identifiées par leurs identifiants. Les segments de code ci-dessous recherchent une forme appelée processus et avec l'ID 1 et modifient son texte.


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

## **Appliquer une feuille de style intégrée ou personnalisée à une forme Visio**
Les feuilles de style Microsoft Visio stockent les informations de mise en forme qui peuvent être appliquées aux formes pour une apparence cohérente. Aspose.Diagram for .NET vous permet d'appliquer des feuilles de style depuis l'intérieur d'une application.

 Les propriétés TextStyle, FillStyle et LineStyle exposées par le[Forme](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) soutenir la classe[Aspose.Diagram.StyleSheet](http://www.aspose.com/api/net/diagram/aspose.diagram/stylesheet) objet. La propriété peut être utilisée pour récupérer des informations de style et appliquer des styles de texte, de ligne et de remplissage personnalisés à un diagram.
### **Styles personnalisés dans Microsoft Visio**
Pour appliquer des styles personnalisés aux formes dans Microsoft Visio :

1. Ouvrez un diagram au Microsoft Visio.
1.  Sélectionner**Définir les styles** du**Format** menu (Visio 2007), ou clic droit**modes** dans le**Explorateur de dessins** fenêtre et sélectionnez**Définir les styles** (Visio 2010).
1.  Dans le**Définir les styles** boîte de dialogue, saisissez un nouveau nom pour votre feuille de style personnalisée. Par exemple, CustomStyle1.
1.  Clique le**Texte**, **Ligne** et**Remplir** boutons pour définir respectivement les styles de texte, de ligne et de remplissage.
1.  Cliquez sur**D'ACCORD**.

Après avoir défini des feuilles de style personnalisées dans Microsoft Visio, utilisez le code suivant dans une application .NET pour appliquer des styles personnalisés à vos formes. Notez que les exemples de code ci-dessous appellent la feuille de style personnalisée définie ci-dessus : vous devez connaître le nom et l'emplacement de la feuille que vous appliquez. Pour appliquer des styles personnalisés par programmation :

1. Charger un diagram.
1. Recherchez la forme à laquelle vous souhaitez appliquer un style.
1. Chargez la feuille de style.
1. Appliquer des styles.
1. Enregistrez le diagram.
#### **Appliquer un exemple de programmation de styles personnalisés**

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

## **Appliquer un style différent sur chaque valeur de texte d'une forme**
 Aussi bien que[création de diagrammes](/diagram/fr/net/load-or-create-a-visio-drawing/), Aspose.Diagram for .NET vous permet de travailler avec des formes de différentes manières. Cet article vous aide à ajouter plusieurs valeurs de texte à une forme et à appliquer un style différent à chaque valeur de texte.

{{% alert color="primary" %}} 

L'élément Shape contient un élément appelé Text, qui contient les caractères du texte et des éléments spéciaux (cp, pp, tp et fld) qui marquent la fin d'une exécution et le début de la suivante. Char Element contient les attributs de mise en forme du texte de la forme, tels que la police, la couleur, le style de texte, la casse, la position par rapport à la ligne de base et la taille en points.

{{% /alert %}} 
### **Ajout de texte et de styles de forme**

|**Entrée diagram**|
|:- |
|![tâche : image_autre_texte](working-with-text_1.png)|


|**Diagram après avoir ajouté diverses valeurs de texte à une forme avec un style différent sur chaque valeur de texte**|
|:- |
|![tâche : image_autre_texte](working-with-text_2.png)|
#### **Exemple de programmation d'ajout de texte et de styles**
Le morceau de code suivant ajoute le texte d'une forme et différents styles.


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

## **Rechercher et remplacer le texte d'une forme**
 La[SMS](http://www.aspose.com/api/net/diagram/aspose.diagram/txt) La classe vous permet de modifier le texte de la forme. La méthode Replace, exposée par le[SMS](http://www.aspose.com/api/net/diagram/aspose.diagram/txt) classe, prend en charge la modification du texte d'une forme.
Les exemples de code de cet article recherchent et remplacent le texte de la forme sur la page.

|**Entrée diagram**|
|:- |
|![tâche : image_autre_texte](working-with-text_3.png)|


|**Le diagram après la modification de la forme**|
|:- |
|![tâche : image_autre_texte](working-with-text_4.png)|
Le processus de modification du texte de la forme :

1. Charger un diagram.
1. Trouver un texte particulier d'une forme.
1. Remplacer le texte de cette forme
1. Enregistrez le diagram.
### **Rechercher et remplacer un exemple de programmation de texte**
Les extraits de code ci-dessous montrent comment modifier le texte de la forme. Le code parcourt les formes d'une page.


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

## **Extraire le texte brut de la page Visio Diagram**
Aspose.Diagram API permet aux développeurs d'extraire du texte brut de la page Visio diagram. Ils peuvent également parcourir les pages Visio diagram pour couvrir l'ensemble du texte Visio diagram.

 Microsoft Office Visio ajoute le texte aux formes. La[Forme](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) La classe contient un élément appelé Text, qui contient les caractères du texte et des éléments spéciaux (cp, pp, tp et fld) qui marquent la fin d'une exécution et le début de la suivante.
### **Extraire un exemple de programmation en texte brut**
Le morceau de code suivant parcourt les formes de la page Visio et filtre le texte brut sans formater les informations.


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

