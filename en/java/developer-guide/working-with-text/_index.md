---
title: Working with Text
type: docs
weight: 120
url: /java/working-with-text/
---

## **Insert a Text Shape in the Visio Page**
Aspose.Diagram API lets developers to insert a text shape anywhere in the Visio page. To achieve this, the addText method of the [Page](https://reference.aspose.com/diagram/java/com.aspose.diagram/Page) class takes PinX, PinY, width, height and text parameters.
### **Insert a Text Shape Programming Sample**
The following piece of code adds a text shape in the Visio diagram.


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

## **Update Visio Shape Text**
As well as [creating diagrams](/diagram/java/load-or-create-a-visio-drawing/), Aspose.Diagram for Java lets you work with shapes in different ways. This article looks at how to access and update text in shapes.

The Text property, exposed by the [Shape](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) class, supports the Aspose.Diagram.Text object. The property can be used to retrieve or update a shape's text.

**Input diagram** 

![todo:image_alt_text](http://i.imgur.com/6aEp7h0.png)

**Diagram after the text in the central shape has been changed from Process to New Text** 

![todo:image_alt_text](http://i.imgur.com/o977cxw.png)

The process for updating a shape's text is straightforward:

1. Load a diagram.
1. Find a particular shape.
1. Set the new text.
1. Save the diagram.
### **Update Shape Text Programming Sample**
The following piece of code updates a shape's text. Shapes are identified by their IDs. The code segments below look for a shape called process and with the ID 1 and changes its text.


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

## **Apply Built-in or Custom Stylesheet to a Visio Shape**
Microsoft Visio style sheets store formatting information that can be applied to shapes for a consistent look and feel. Aspose.Diagram for Java allows you to apply style sheets from inside an application.

The TextStyle, FillStyle and LineStyle properties exposed by the [Shape](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) class support the [Aspose.Diagram.StyleSheet](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/stylesheet) object. The property can be used to retrieve style information and apply custom text, line and fill styles to a diagram.

**Input diagram** 

![todo:image_alt_text](http://i.imgur.com/feV1x2N.png)

**The diagram after applying a custom style sheet that defines text, line and fill styles** 

![todo:image_alt_text](http://i.imgur.com/Xk9W0wN.png)
### **Custom Styles in Microsoft Visio**
To apply custom styles to shapes in Microsoft Visio:

1. Open a diagram in Microsoft Visio.
1. Select **Define Styles** from the **Format** menu (Visio 2007), or right-click **Styles** in the **Drawing Explorer** window, and select **Define Styles** (Visio 2010).
1. In the **Define Styles** dialog, type a new name for your custom style sheet. For example, CustomStyle1.
1. Click the **Text**, **Line** and **Fill** buttons to set text, line and fill styles respectively.
1. Click **OK**.

After defining custom style sheets in Microsoft Visio, use the following code in a Java application to apply custom styles to your shapes. Note that the code samples below call the custom style sheet defined above: you need to know the name and location of the sheet you apply.

To apply custom styles programmatically:

1. Load a diagram.
1. Find the shape you want to apply a style to.
1. Load the stylesheet.
1. Apply styles.
1. Save the diagram.
#### **Apply Custom Styles Programming Sample**

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

## **Apply Different Style on the Each Text Value of a Shape**
As well as [creating diagrams](/diagram/java/load-or-create-a-visio-drawing/), Aspose.Diagram for Java lets you work with shapes in different ways. This article helps to add multiple text values to a shape and apply different style on each text value.

{{% alert color="primary" %}} 

The Shape element contains an element called Text, which contains the characters of the text and special elements (cp, pp, tp, and fld) that mark the end of one run and the beginning of the next. Char Element contains the formatting attributes for the shape's text, such as font, color, text style, case, position relative to the baseline, and point size.

{{% /alert %}} 
### **Adding Shape Text and Styles**
**Input diagram** 

![todo:image_alt_text](http://i.imgur.com/ZqgQPQC.png)

**Diagram after adding various text values to a shape with different style on each text value** 

![todo:image_alt_text](http://i.imgur.com/7UWhFbU.png)
#### **Adding Text and Styles Programming Sample**
The following piece of code add a shape's text and different styles.


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

## **Find and Replace the Text of a Shape**
The [Txt](https://reference.aspose.com/diagram/java/com.aspose.diagram/txt) Class allows you to edit the shape's text. The Replace method, exposed by the [Txt](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/txt) class, support changing the text of a shape.
The code examples in this article find and replace the shape's text on the page.

**Input diagram** 

![todo:image_alt_text](http://i.imgur.com/lW5xaP0.png)


**The diagram after the shape is edited** 

![todo:image_alt_text](http://i.imgur.com/m33W1Tk.png)

The process for changing the shape's text:

1. Load a diagram.
1. Find a particular text of a shape.
1. Replace text of this shape
1. Save the diagram.
### **Find and Replace Text Programming Sample**
The code snippets below show how to modify the shape's text. The code iterate through the shapes of a page.


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

## **Extract Plain Text from the Visio Diagram Page**
Aspose.Diagram API allows developers to extract plain text from the Visio diagram page. They can also iterate through the Visio diagram pages to cover the whole Visio diagram text.

Microsoft Office Visio adds the text to the shapes. The [Shape](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) class contains an element called Text, which contains the characters of the text and special elements (cp, pp, tp, and fld) that mark the end of one run and the beginning of the next.
### **Extract Plain Text Programming Sample**
The following piece of code iterates through the shapes of the Visio Page and filter plain text without formatting information.


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

