---
title: Arbeta med text
type: docs
weight: 120
url: /sv/java/working-with-text/
---
## **Infoga en textform på sidan Visio**
 Aspose.Diagram API låter utvecklare infoga en textform var som helst på sidan Visio. För att uppnå detta, addText-metoden för[Sida](https://reference.aspose.com/diagram/java/com.aspose.diagram/Page) klass tar PinX, PinY, bredd, höjd och textparametrar.
### **Infoga ett programmeringsexempel för textform**
Följande kodbit lägger till en textform i Visio diagram.


{{< highlight java >}}
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

## **Uppdatering Visio Formtext**
 Såväl som[skapa diagram](/diagram/sv/java/load-or-create-a-visio-drawing/), Aspose.Diagram for Java låter dig arbeta med former på olika sätt. Den här artikeln tittar på hur du kommer åt och uppdaterar text i former.

 Text-egenskapen, exponerad av[Form](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) klass, stöder objektet Aspose.Diagram.Text. Egenskapen kan användas för att hämta eller uppdatera en forms text.

**Ingång diagram** 

![todo:image_alt_text](http://i.imgur.com/6aEp7h0.png)

**Diagram efter att texten i den centrala formen har ändrats från Process till Ny text** 

![todo:image_alt_text](http://i.imgur.com/o977cxw.png)

Processen för att uppdatera en forms text är enkel:

1. Ladda ett diagram.
1. Hitta en viss form.
1. Ställ in den nya texten.
1. Spara diagram.
### **Uppdatera formtextprogrammeringsexempel**
Följande kodbit uppdaterar en forms text. Former identifieras med deras ID. Kodsegmenten nedan letar efter en form som kallas process och med ID 1 och ändrar dess text.


{{< highlight java >}}
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

## **Applicera inbyggd eller anpassad formatmall på en Visio-form**
Microsoft Visio stilmallar lagrar formateringsinformation som kan appliceras på former för ett konsekvent utseende och känsla. Aspose.Diagram for Java låter dig tillämpa stilmallar inifrån en applikation.

 Egenskaperna TextStyle, FillStyle och LineStyle som exponeras av[Form](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) klass stödja[Aspose.Diagram.StyleSheet](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/stylesheet) objekt. Egenskapen kan användas för att hämta stilinformation och tillämpa anpassade text-, linje- och fyllningsstilar på en diagram.

**Ingång diagram** 

![todo:image_alt_text](http://i.imgur.com/feV1x2N.png)

**diagram efter att ha tillämpat en anpassad formatmall som definierar text-, linje- och fyllningsstilar** 

![todo:image_alt_text](http://i.imgur.com/Xk9W0wN.png)
### **Anpassade stilar i Microsoft Visio**
Så här tillämpar du anpassade stilar på former i Microsoft Visio:

1. Öppna ett diagram i Microsoft Visio.
1.  Välj**Definiera stilar** från**Formatera** menyn (Visio 2007), eller högerklicka**Stilar** i**Rita Explorer** fönstret och välj**Definiera stilar** (Visio 2010).
1.  I den**Definiera stilar** skriv ett nytt namn för din anpassade stilmall. Till exempel CustomStyle1.
1.  Klicka på**Text**, **Linje** och**Fylla** knappar för att ställa in text-, linje- och fyllningsstilar.
1.  Klick**OK**.

Efter att ha definierat anpassade stilmallar i Microsoft Visio använder du följande kod i en Java-applikation för att tillämpa anpassade stilar på dina former. Observera att kodexemplen nedan kallar den anpassade stilmall som definierats ovan: du måste känna till namnet och platsen för arket du använder.

Så här tillämpar du anpassade stilar programmatiskt:

1. Ladda ett diagram.
1. Hitta formen du vill använda en stil på.
1. Ladda stilmallen.
1. Applicera stilar.
1. Spara diagram.
#### **Applicera anpassade stilar programmeringsexempel**

{{< highlight java >}}
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

## **Tillämpa annan stil på varje textvärde i en form**
 Såväl som[skapa diagram](/diagram/sv/java/load-or-create-a-visio-drawing/), Aspose.Diagram for Java låter dig arbeta med former på olika sätt. Den här artikeln hjälper dig att lägga till flera textvärden till en form och använda olika stilar på varje textvärde.

{{% alert color="primary" %}} 

Shape-elementet innehåller ett element som kallas Text, som innehåller tecknen i texten och specialelement (cp, pp, tp och fld) som markerar slutet på en körning och början på nästa. Char Element innehåller formateringsattribut för formens text, såsom teckensnitt, färg, textstil, skiftläge, position i förhållande till baslinjen och punktstorlek.

{{% /alert %}} 
### **Lägga till formtext och stilar**
**Ingång diagram** 

![todo:image_alt_text](http://i.imgur.com/ZqgQPQC.png)

**Diagram efter att ha lagt till olika textvärden till en form med olika stil på varje textvärde** 

![todo:image_alt_text](http://i.imgur.com/7UWhFbU.png)
#### **Lägga till text och stilar Programmeringsexempel**
Följande kodbit lägger till en forms text och olika stilar.


{{< highlight java >}}
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

## **Hitta och ersätt texten i en form**
 De[Text](https://reference.aspose.com/diagram/java/com.aspose.diagram/txt) Klass låter dig redigera formens text. Ersätt-metoden, exponerad av[Text](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/txt) klass, stöd för att ändra texten i en form.
Kodexemplen i den här artikeln hittar och ersätter formens text på sidan.

**Ingång diagram** 

![todo:image_alt_text](http://i.imgur.com/lW5xaP0.png)


**diagram efter formen har redigerats** 

![todo:image_alt_text](http://i.imgur.com/m33W1Tk.png)

Processen för att ändra formens text:

1. Ladda ett diagram.
1. Hitta en viss text av en form.
1. Byt ut text i denna form
1. Spara diagram.
### **Hitta och ersätt textprogrammeringsexempel**
Kodavsnitten nedan visar hur du ändrar formens text. Koden itererar genom formerna på en sida.


{{< highlight java >}}
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

## **Extrahera vanlig text från sidan Visio Diagram**
Aspose.Diagram API tillåter utvecklare att extrahera vanlig text från sidan Visio diagram. De kan också iterera genom sidorna Visio diagram för att täcka hela texten Visio diagram.

 Microsoft Office Visio lägger till texten i formerna. De[Form](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) klass innehåller ett element som heter Text, som innehåller tecknen i texten och specialelement (cp, pp, tp och fld) som markerar slutet på en körning och början på nästa.
### **Extrahera programmeringsexempel för vanlig text**
Följande kodbit itererar genom formerna på sidan Visio och filtrerar vanlig text utan att formatera information.


{{< highlight java >}}
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

