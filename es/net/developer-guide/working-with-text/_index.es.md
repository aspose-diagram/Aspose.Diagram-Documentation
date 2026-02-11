---
title: Trabajar con texto
type: docs
weight: 90
url: /es/net/working-with-text/
description: Esta sección explica cómo insertar una forma de texto o actualizar el texto de la forma con Aspose.Diagram.
---
## **Insertar una forma de texto en la página Visio**
 Aspose.Diagram API permite a los desarrolladores insertar una forma de texto en cualquier lugar de la página Visio. Para lograr esto, el método AddText del[Página](http://www.aspose.com/api/net/diagram/aspose.diagram/page) La clase toma los parámetros PinX, PinY, ancho, alto y texto.
### **Insertar una muestra de programación de forma de texto**
El siguiente fragmento de código agrega una forma de texto en el Visio diagram.


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

## **Actualizar Visio Texto de forma**
 Tanto como[creando diagramas](/diagram/es/net/load-or-create-a-visio-drawing/) , Aspose.Diagram for .NET le permite trabajar con formas de diferentes maneras. Este artículo analiza cómo acceder y actualizar el texto en las formas. La propiedad Text, expuesta por el[Forma](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) clase, admite el objeto Aspose.Diagram.Text. La propiedad se puede utilizar para recuperar o actualizar el texto de una forma. El proceso para actualizar el texto de una forma es sencillo:

1. Cargue un diagram.
1. Encuentra una forma particular.
1. Establecer el nuevo texto.
1. Guarda el diagram.
### **Actualizar muestra de programación de texto de forma**
El siguiente fragmento de código actualiza el texto de una forma. Las formas se identifican por sus ID. Los segmentos de código a continuación buscan una forma llamada proceso y con el ID 1 y cambia su texto.


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

## **Aplicar una hoja de estilo integrada o personalizada a una forma Visio**
Microsoft Visio Las hojas de estilo almacenan información de formato que se puede aplicar a las formas para lograr una apariencia uniforme. Aspose.Diagram for .NET le permite aplicar hojas de estilo desde dentro de una aplicación.

 Las propiedades TextStyle, FillStyle y LineStyle expuestas por el[Forma](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) apoyo de la clase[Aspose.Diagram.StyleSheet](http://www.aspose.com/api/net/diagram/aspose.diagram/stylesheet) objeto. La propiedad se puede utilizar para recuperar información de estilo y aplicar estilos personalizados de texto, línea y relleno a un diagram.
### **Estilos personalizados en Microsoft Visio**
Para aplicar estilos personalizados a formas en Microsoft Visio:

1. Abra un diagram en Microsoft Visio.
1.  Seleccione**Definir estilos** desde el**Formato** menú (Visio 2007), o haga clic con el botón derecho**Estilos** en el**Explorador de dibujo** ventana y seleccione**Definir estilos** (Visio 2010).
1.  En el**Definir estilos** cuadro de diálogo, escriba un nuevo nombre para su hoja de estilo personalizada. Por ejemplo, CustomStyle1.
1.  Haga clic en el**Texto**, **Línea** y**Llenar** botones para establecer estilos de texto, línea y relleno respectivamente.
1.  Hacer clic**OK**.

Después de definir hojas de estilo personalizadas en Microsoft Visio, use el siguiente código en una aplicación .NET para aplicar estilos personalizados a sus formas. Tenga en cuenta que los ejemplos de código a continuación llaman a la hoja de estilo personalizada definida anteriormente: necesita saber el nombre y la ubicación de la hoja que aplica. Para aplicar estilos personalizados mediante programación:

1. Cargue un diagram.
1. Encuentre la forma a la que desea aplicar un estilo.
1. Cargue la hoja de estilo.
1. Aplicar estilos.
1. Guarda el diagram.
#### **Aplicar muestra de programación de estilos personalizados**

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

## **Aplicar un estilo diferente en cada valor de texto de una forma**
 Tanto como[creando diagramas](/diagram/es/net/load-or-create-a-visio-drawing/), Aspose.Diagram for .NET le permite trabajar con formas de diferentes maneras. Este artículo ayuda a agregar múltiples valores de texto a una forma y aplicar un estilo diferente en cada valor de texto.

{{% alert color="primary" %}} 

El elemento Forma contiene un elemento denominado Texto, que contiene los caracteres del texto y elementos especiales (cp, pp, tp y fld) que marcan el final de una ejecución y el comienzo de la siguiente. Char Element contiene los atributos de formato para el texto de la forma, como fuente, color, estilo de texto, mayúsculas y minúsculas, posición relativa a la línea de base y tamaño de punto.

{{% /alert %}} 
### **Adición de texto y estilos de formas**

|**Entrada diagram**|
|:- |
|![todo:imagen_alternativa_texto](working-with-text_1.png)|


|**Diagram después de agregar varios valores de texto a una forma con un estilo diferente en cada valor de texto**|
|:- |
|![todo:imagen_alternativa_texto](working-with-text_2.png)|
#### **Ejemplo de programación de adición de texto y estilos**
El siguiente fragmento de código agrega el texto de una forma y diferentes estilos.


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

## **Buscar y reemplazar el texto de una forma**
 los[TXT](http://www.aspose.com/api/net/diagram/aspose.diagram/txt) La clase le permite editar el texto de la forma. El método Reemplazar, expuesto por el[TXT](http://www.aspose.com/api/net/diagram/aspose.diagram/txt) class, admite cambiar el texto de una forma.
Los ejemplos de código de este artículo buscan y reemplazan el texto de la forma en la página.

|**Entrada diagram**|
|:- |
|![todo:imagen_alternativa_texto](working-with-text_3.png)|


|**El diagram después de editar la forma.**|
|:- |
|![todo:imagen_alternativa_texto](working-with-text_4.png)|
El proceso para cambiar el texto de la forma:

1. Cargue un diagram.
1. Encuentra un texto particular de una forma.
1. Reemplazar el texto de esta forma
1. Guarda el diagram.
### **Ejemplo de programación de buscar y reemplazar texto**
Los fragmentos de código a continuación muestran cómo modificar el texto de la forma. El código itera a través de las formas de una página.


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

## **Extraer texto sin formato de la página Visio Diagram**
Aspose.Diagram API permite a los desarrolladores extraer texto sin formato de la página Visio diagram. También pueden iterar a través de las páginas Visio diagram para cubrir todo el texto Visio diagram.

 Microsoft Office Visio agrega el texto a las formas. los[Forma](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class contiene un elemento llamado Texto, que contiene los caracteres del texto y elementos especiales (cp, pp, tp y fld) que marcan el final de una ejecución y el comienzo de la siguiente.
### **Extraer muestra de programación de texto sin formato**
El siguiente fragmento de código itera a través de las formas de la página Visio y filtra el texto sin formato sin información de formato.


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

