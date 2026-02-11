---
title: Arbeiten mit Text
type: docs
weight: 120
url: /de/java/working-with-text/
---
## **Fügen Sie eine Textform in die Seite Visio ein**
 Mit Aspose.Diagram API können Entwickler überall auf der Visio-Seite eine Textform einfügen. Um dies zu erreichen, wird die addText-Methode des[Buchseite](https://reference.aspose.com/diagram/java/com.aspose.diagram/Page) Die Klasse nimmt PinX-, PinY-, Breiten-, Höhen- und Textparameter an.
### **Fügen Sie ein Textform-Programmierbeispiel ein**
Der folgende Codeabschnitt fügt eine Textform in Visio diagram hinzu.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getSharedDataDir(InsertTextShape.class) + "Text/";
// create a new diagram
Diagram diagram = new Diagram();
// set parameters
double PinX = 1, PinY = 1, Width = 1, Height = 1;
String text = "Test text";
// add text to a Visio page
diagram.getPages().getPage(0).addText(PinX, PinY, Width, Height, text);
// save diagram 
diagram.save(dataDir + "InsertTextShape_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Aktualisieren Sie Visio Shape-Text**
 Ebenso gut wie[Diagramme erstellen](/diagram/de/java/load-or-create-a-visio-drawing/), Aspose.Diagram for Java lässt Sie auf unterschiedliche Weise mit Formen arbeiten. In diesem Artikel wird beschrieben, wie Sie auf Text in Formen zugreifen und ihn aktualisieren.

 Die Text-Eigenschaft, verfügbar gemacht durch die[Form](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) Klasse, unterstützt das Objekt Aspose.Diagram.Text. Die Eigenschaft kann verwendet werden, um den Text einer Form abzurufen oder zu aktualisieren.

**Geben Sie diagram ein** 

![todo: Bild_alt_Text](http://i.imgur.com/6aEp7h0.png)

**Diagram, nachdem der Text in der zentralen Form von „Prozess“ in „Neuer Text“ geändert wurde** 

![todo: Bild_alt_Text](http://i.imgur.com/o977cxw.png)

Der Vorgang zum Aktualisieren des Texts einer Form ist unkompliziert:

1. Laden Sie eine diagram.
1. Finden Sie eine bestimmte Form.
1. Legen Sie den neuen Text fest.
1. Speichern Sie die diagram.
### **Programmierbeispiel für Formtext aktualisieren**
Der folgende Codeabschnitt aktualisiert den Text einer Form. Shapes werden anhand ihrer IDs identifiziert. Die folgenden Codesegmente suchen nach einer Form namens process und mit der ID 1 und ändern ihren Text.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(UpdateShapeText.class); 
//Call the diagram constructor to load diagram from a VDX file
Diagram diagram = new Diagram(dataDir + "UpdateShapeText.vsd");
// get page by name
Page page = diagram.getPages().getPage("Flow 1");
//Find a particular shape and update its text
for (Shape shape :(Iterable<Shape>) page.getShapes())
{
    if (shape.getNameU().toLowerCase() == "process" && shape.getID() == 1)
    {
        shape.getText().getValue().clear();
        shape.getText().getValue().add(new Txt("New Text"));
    }
}
// save diagram
diagram.save(dataDir + "UpdateShapeText_Out.vdx", SaveFileFormat.VDX);

{{< /highlight >}}
```
## **Wenden Sie ein integriertes oder benutzerdefiniertes Stylesheet auf eine Visio-Form an**
Microsoft Visio Stylesheets speichern Formatierungsinformationen, die für ein konsistentes Erscheinungsbild auf Formen angewendet werden können. Mit Aspose.Diagram for Java können Sie Stylesheets aus einer Anwendung heraus anwenden.

 Die Eigenschaften TextStyle, FillStyle und LineStyle, die von der bereitgestellt werden[Form](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) Klasse unterstützt die[Aspose.Diagram.StyleSheet](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/stylesheet) Objekt. Die Eigenschaft kann verwendet werden, um Stilinformationen abzurufen und benutzerdefinierte Text-, Linien- und Füllstile auf einen diagram anzuwenden.

**Geben Sie diagram ein** 

![todo: Bild_alt_Text](http://i.imgur.com/feV1x2N.png)

**Die diagram nach dem Anwenden eines benutzerdefinierten Stylesheets, das Text-, Linien- und Füllstile definiert** 

![todo: Bild_alt_Text](http://i.imgur.com/Xk9W0wN.png)
### **Benutzerdefinierte Stile unter Microsoft Visio**
So wenden Sie benutzerdefinierte Stile auf Formen in Microsoft Visio an:

1. Öffnen Sie eine diagram in Microsoft Visio.
1.  Auswählen**Stile definieren** von dem**Format** Menü (Visio 2007), oder klicken Sie mit der rechten Maustaste**Stile** in dem**Zeichnungs-Explorer** Fenster und wählen Sie aus**Stile definieren** (Visio 2010).
1.  In dem**Stile definieren** Geben Sie im Dialogfeld einen neuen Namen für Ihr benutzerdefiniertes Stylesheet ein. Beispiel: CustomStyle1.
1.  Drücke den**Text**, **Linie** und**Füllen** Schaltflächen zum Festlegen von Text-, Linien- und Füllstilen.
1.  Klicken**OK**.

Nachdem Sie benutzerdefinierte Stylesheets in Microsoft Visio definiert haben, verwenden Sie den folgenden Code in einer Java-Anwendung, um benutzerdefinierte Stile auf Ihre Formen anzuwenden. Beachten Sie, dass die folgenden Codebeispiele das oben definierte benutzerdefinierte Stylesheet aufrufen: Sie müssen den Namen und den Speicherort des angewendeten Sheets kennen.

So wenden Sie benutzerdefinierte Stile programmgesteuert an:

1. Laden Sie eine diagram.
1. Suchen Sie die Form, auf die Sie einen Stil anwenden möchten.
1. Laden Sie das Stylesheet.
1. Stile anwenden.
1. Speichern Sie die diagram.
#### **Wenden Sie das Programmierbeispiel für benutzerdefinierte Stile an**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ApplyCustomStyleSheets.class);

//Load diagram
Diagram diagram = new Diagram(dataDir + "ApplyCustomStyleSheets.vsd");
Shape sourceShape = null;
        
// get page by name
Page page = diagram.getPages().getPage("Flow 1");
//Find the shape that you want to apply style to
for (com.aspose.diagram.Shape shape : (Iterable<Shape>) page.getShapes())
{
    if (shape.getName() == "Process") {
        sourceShape = shape;
        break;
    }
}

StyleSheet customStyleSheet = null;

//Find the required style sheet
for (StyleSheet styleSheet : (Iterable<StyleSheet>) diagram.getStyleSheets())
{
    if (styleSheet.getName() == "CustomStyle1")
    {
        customStyleSheet = styleSheet;
        break;
    }
}

if (sourceShape != null && customStyleSheet != null)
{
    //Apply text style
    sourceShape.setTextStyle(customStyleSheet);
    //Apply fill style
    sourceShape.setFillStyle(customStyleSheet);
    //Apply line style
    sourceShape.setLineStyle(customStyleSheet);
}

 //Save the changed diagram as VDX
diagram.save(dataDir + "ApplyCustomStyleSheets_Out.vdx", SaveFileFormat.VDX);

{{< /highlight >}}
```
## **Wenden Sie einen anderen Stil auf die einzelnen Textwerte einer Form an**
 Ebenso gut wie[Diagramme erstellen](/diagram/de/java/load-or-create-a-visio-drawing/), Aspose.Diagram for Java lässt Sie auf unterschiedliche Weise mit Formen arbeiten. Dieser Artikel hilft beim Hinzufügen mehrerer Textwerte zu einer Form und beim Anwenden eines anderen Stils auf jeden Textwert.

{{% alert color="primary" %}} 

Das Shape-Element enthält ein Element namens Text, das die Zeichen des Textes und spezielle Elemente (cp, pp, tp und fld) enthält, die das Ende eines Laufs und den Beginn des nächsten markieren. Char-Element enthält die Formatierungsattribute für den Text der Form, z. B. Schriftart, Farbe, Textstil, Groß-/Kleinschreibung, Position relativ zur Grundlinie und Punktgröße.

{{% /alert %}} 
### **Hinzufügen von Formtext und -stilen**
**Geben Sie diagram ein** 

![todo: Bild_alt_Text](http://i.imgur.com/ZqgQPQC.png)

**Diagram nach dem Hinzufügen verschiedener Textwerte zu einer Form mit unterschiedlichem Stil für jeden Textwert** 

![todo: Bild_alt_Text](http://i.imgur.com/7UWhFbU.png)
#### **Hinzufügen von Text und Stilen Programmierbeispiel**
Der folgende Codeabschnitt fügt den Text einer Form und verschiedene Stile hinzu.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ApplyFontOnText.class);   
        
// load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get page by name
Page page = diagram.getPages().getPage("Page-1");
// get shape by ID
Shape shape = page.getShapes().getShape(1);
// clear shape text values and chars
shape.getText().getValue().clear();
shape.getChars().clear();

// mark character run and add text
shape.getText().getValue().add(new Cp(0));
shape.getText().getValue().add(new Txt("TextStyle_Regular\n"));
shape.getText().getValue().add(new Cp(1));
shape.getText().getValue().add(new Txt("TextStyle_Bold_Italic\n"));
shape.getText().getValue().add(new Cp(2));
shape.getText().getValue().add(new Txt("TextStyle_Underline_Italic\n"));
shape.getText().getValue().add(new Cp(3));
shape.getText().getValue().add(new Txt("TextStyle_Bold_Italic_Underline"));

// add formatting characters
shape.getChars().add(new Char());
shape.getChars().add(new Char());
shape.getChars().add(new Char());
shape.getChars().add(new Char());

//set properties e.g. color, font, size and style etc.
shape.getChars().get(0).setIX(0);
shape.getChars().get(0).getColor().setValue("#FF0000");
shape.getChars().get(0).getFont().setValue(1);
shape.getChars().get(0).getSize().setValue(0.22);
shape.getChars().get(0).getStyle().setValue(StyleValue.UNDEFINED);

//set properties e.g. color, font, size and style etc.
shape.getChars().get(1).setIX(1);
shape.getChars().get(1).getColor().setValue("#FF00FF");
shape.getChars().get(1).getFont().setValue(1);
shape.getChars().get(1).getSize().setValue(0.22);
shape.getChars().get(1).getStyle().setValue(StyleValue.BOLD | StyleValue.ITALIC);

//set properties e.g. color, font, size and style etc.
shape.getChars().get(2).setIX(2);
shape.getChars().get(2).getColor().setValue("#00FF00");
shape.getChars().get(2).getFont().setValue(1);
shape.getChars().get(2).getSize().setValue(0.22);
shape.getChars().get(2).getStyle().setValue(StyleValue.UNDERLINE | StyleValue.ITALIC);

//set properties e.g. color, font, size and style etc.
shape.getChars().get(3).setIX(3);
shape.getChars().get(3).getColor().setValue("#3333FF");
shape.getChars().get(3).getFont().setValue(1);
shape.getChars().get(3).getSize().setValue(0.22);
shape.getChars().get(3).getStyle().setValue(StyleValue.BOLD | StyleValue.ITALIC | StyleValue.UNDERLINE);
// save diagram
diagram.save(dataDir + "ApplyFontOnText_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Suchen und ersetzen Sie den Text einer Form**
 Das[Txt](https://reference.aspose.com/diagram/java/com.aspose.diagram/txt) Mit der Klasse können Sie den Text der Form bearbeiten. Die Replace-Methode, verfügbar gemacht durch die[Txt](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/txt) Klasse, unterstützen Sie das Ändern des Textes einer Form.
Die Codebeispiele in diesem Artikel suchen und ersetzen den Text der Form auf der Seite.

**Geben Sie diagram ein** 

![todo: Bild_alt_Text](http://i.imgur.com/lW5xaP0.png)


**Die diagram, nachdem die Form bearbeitet wurde** 

![todo: Bild_alt_Text](http://i.imgur.com/m33W1Tk.png)

Der Prozess zum Ändern des Textes der Form:

1. Laden Sie eine diagram.
1. Finden Sie einen bestimmten Text einer Form.
1. Text dieser Form ersetzen
1. Speichern Sie die diagram.
### **Programmierbeispiel zum Suchen und Ersetzen von Text**
Die folgenden Codeausschnitte zeigen, wie der Text der Form geändert werden kann. Der Code durchläuft die Shapes einer Seite.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(FindAndReplaceShapeText.class); 
// load diagram
Diagram diagram = new Diagram(dataDir + "FindReplaceText.vsdx");

DateFormat dateFormat = new SimpleDateFormat("dd/MMMM/yyyy");
Date myDate = new Date(System.currentTimeMillis());
Calendar cal = Calendar.getInstance();

// Prepare a collection old and new text
Hashtable<String, String> replacements = new Hashtable<String, String>();
replacements.put("[[CompanyName]]", "Research Society of XYZ");
replacements.put("[[CompanyName]]", "Research Society of XYZ");
replacements.put("[[EmplyeeName]]", "James Bond");
replacements.put("[[SubjectTitle]]", "The affect of the internet on social behavior in the industrialize world");

cal.setTime(myDate);
cal.add(Calendar.YEAR, -1);
System.out.println(dateFormat.format(cal.getTime()));
replacements.put("[[TimePeriod]]", dateFormat.format(cal.getTime()) + " -- " + dateFormat.format(myDate));

cal.setTime(myDate);
cal.add(Calendar.DAY_OF_MONTH, -7);
System.out.println(dateFormat.format(cal.getTime()));
replacements.put("[[SubmissionDate]]", dateFormat.format(cal.getTime()));
replacements.put("[[AmountReq]]", "$100,000");

cal.setTime(myDate);
cal.add(Calendar.DAY_OF_MONTH, 1);
System.out.println(dateFormat.format(cal.getTime()));
replacements.put("[[DateApproved]]", dateFormat.format(cal.getTime()));

// Iterate through the shapes of a page
for (Shape shape : (Iterable<Shape>) diagram.getPages().getPage("Page-1").getShapes())
{
    Set<String> keys = replacements.keySet();
    for(String key: keys)
    {
        for (FormatTxt txt : (Iterable<FormatTxt>) shape.getText().getValue())
        {
       	    Txt tx = (Txt)((txt instanceof Txt) ? txt : null);
            if (tx != null && tx.getText().contains(key))
            {
                //find and replace text of a shape
                tx.setText(tx.getText().replace(key, replacements.get(key)));
            }
        }
    }
}
// Save the diagram
diagram.save(dataDir + "FindAndReplaceShapeText_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Extrahieren Sie Klartext von der Seite Visio Diagram**
Aspose.Diagram API ermöglicht es Entwicklern, Klartext aus der Seite Visio diagram zu extrahieren. Sie können auch die Visio diagram-Seiten durchlaufen, um den gesamten Visio diagram-Text abzudecken.

 Microsoft Office Visio fügt den Text zu den Formen hinzu. Das[Form](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) Klasse enthält ein Element namens Text, das die Zeichen des Textes und spezielle Elemente (cp, pp, tp und fld) enthält, die das Ende eines Laufs und den Beginn des nächsten markieren.
### **Extrahieren Sie ein Klartext-Programmierbeispiel**
Der folgende Codeabschnitt durchläuft die Formen der Seite Visio und filtert einfachen Text ohne Formatierungsinformationen.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
static String text = "";
public static void main(String[] args) throws Exception
{
       // The path to the documents directory.
       String dataDir = Utils.getDataDir(GetPlainTextOfVisio.class);
       // load diagram
       Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

       // get Visio diagram page
       Page page = diagram.getPages().getPage("Page-1");

       // iterate through the shapes
       for (Shape shape :(Iterable<Shape>) page.getShapes())
       {
           // extract plain text from the shape
           GetShapeText(shape);
       }
       // display extracted text
       System.out.println(text);
}
   private static void GetShapeText(Shape shape)
   {
   	// filter shape text
       if (shape.getText().getValue().getText() != "")
       	text += (shape.getText().getValue().getText().replaceAll("\\<.*?>",""));

       // for image shapes
       if (shape.getType() == TypeValue.FOREIGN)
           text += (shape.getName());

       // for group shapes
       if (shape.getType() == TypeValue.GROUP)
           for(Shape subshape : (Iterable<Shape>) shape.getShapes())
           {
               GetShapeText(subshape);
           }
   }

{{< /highlight >}}
```
