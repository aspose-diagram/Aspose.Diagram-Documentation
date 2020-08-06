---
title: Working with Text
type: docs
weight: 90
url: /net/working-with-text/
---

## **Insert a Text Shape in the Visio Page**
Aspose.Diagram API lets developers to insert a text shape anywhere in the Visio page. To achieve this, the AddText method of the [Page](http://www.aspose.com/api/net/diagram/aspose.diagram/page) class takes PinX, PinY, width, height and text parameters.
### **Insert a Text Shape Programming Sample**
The following piece of code adds a text shape in the Visio diagram.

{{< gist "aspose-diagram" "cce69e51f567ea17ef24bc35fef0f689" "Examples-CSharp-Working-with-Text-InsertTextShape-InsertTextShape.cs" >}}
## **Update Visio Shape Text**
As well as [creating diagrams](/diagram/net/load-or-create-a-visio-drawing-html/), Aspose.Diagram for .NET lets you work with shapes in different ways. This article looks at how to access and update text in shapes. The Text property, exposed by the [Shape](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class, supports the Aspose.Diagram.Text object. The property can be used to retrieve or update a shape's text. The process for updating a shape's text is straightforward:

1. Load a diagram.
1. Find a particular shape.
1. Set the new text.
1. Save the diagram.
### **Update Shape Text Programming Sample**
The following piece of code updates a shape's text. Shapes are identified by their IDs. The code segments below look for a shape called process and with the ID 1 and changes its text.

{{< gist "aspose-diagram" "cce69e51f567ea17ef24bc35fef0f689" "Examples-CSharp-Working-with-Text-UpdateShapeText-UpdateShapeText.cs" >}}
## **Apply Built-in or Custom Stylesheet to a Visio Shape**
Microsoft Visio style sheets store formatting information that can be applied to shapes for a consistent look and feel. Aspose.Diagram for .NET allows you to apply style sheets from inside an application.

The TextStyle, FillStyle and LineStyle properties exposed by the [Shape](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class support the [Aspose.Diagram.StyleSheet](http://www.aspose.com/api/net/diagram/aspose.diagram/stylesheet) object. The property can be used to retrieve style information and apply custom text, line and fill styles to a diagram.
### **Custom Styles in Microsoft Visio**
To apply custom styles to shapes in Microsoft Visio:

1. Open a diagram in Microsoft Visio.
1. Select **Define Styles** from the **Format** menu (Visio 2007), or right-click **Styles** in the **Drawing Explorer** window, and select **Define Styles** (Visio 2010).
1. In the **Define Styles** dialog, type a new name for your custom style sheet. For example, CustomStyle1.
1. Click the **Text**, **Line** and **Fill** buttons to set text, line and fill styles respectively.
1. Click **OK**.

After defining custom style sheets in Microsoft Visio, use the following code in a .NET application to apply custom styles to your shapes. Note that the code samples below call the custom style sheet defined above: you need to know the name and location of the sheet you apply. To apply custom styles programmatically:

1. Load a diagram.
1. Find the shape you want to apply a style to.
1. Load the stylesheet.
1. Apply styles.
1. Save the diagram.
#### **Apply Custom Styles Programming Sample**
{{< gist "aspose-diagram" "cce69e51f567ea17ef24bc35fef0f689" "Examples-CSharp-Working-with-Text-ApplyCustomStyleSheets-ApplyCustomStyleSheets.cs" >}}
## **Apply Different Style on the Each Text Value of a Shape**
As well as [creating diagrams](/diagram/net/load-or-create-a-visio-drawing-html/), Aspose.Diagram for .NET lets you work with shapes in different ways. This article helps to add multiple text values to a shape and apply different style on each text value.

{{% alert color="primary" %}} 

The Shape element contains an element called Text, which contains the characters of the text and special elements (cp, pp, tp, and fld) that mark the end of one run and the beginning of the next. Char Element contains the formatting attributes for the shape's text, such as font, color, text style, case, position relative to the baseline, and point size.

{{% /alert %}} 
### **Adding Shape Text and Styles**

|**Input diagram**|
| :- |
|![todo:image_alt_text](working-with-text_1.png)|


|**Diagram after adding various text values to a shape with different style on each text value**|
| :- |
|![todo:image_alt_text](working-with-text_2.png)|
#### **Adding Text and Styles Programming Sample**
The following piece of code add a shape's text and different styles.

{{< gist "aspose-diagram" "cce69e51f567ea17ef24bc35fef0f689" "Examples-CSharp-Working-with-Text-ApplyFontOnText-ApplyFontOnText.cs" >}}
## **Find and Replace the Text of a Shape**
The [Txt](http://www.aspose.com/api/net/diagram/aspose.diagram/txt) Class allows you to edit the shape's text. The Replace method, exposed by the [Txt](http://www.aspose.com/api/net/diagram/aspose.diagram/txt) class, support changing the text of a shape.
The code examples in this article find and replace the shape's text on the page.

|**Input diagram**|
| :- |
|![todo:image_alt_text](working-with-text_3.png)|


|**The diagram after the shape is edited**|
| :- |
|![todo:image_alt_text](working-with-text_4.png)|
The process for changing the shape's text:

1. Load a diagram.
1. Find a particular text of a shape.
1. Replace text of this shape
1. Save the diagram.
### **Find and Replace Text Programming Sample**
The code snippets below show how to modify the shape's text. The code iterate through the shapes of a page.

{{< gist "aspose-diagram" "cce69e51f567ea17ef24bc35fef0f689" "Examples-CSharp-Working-with-Text-FindAndReplaceShapeText-FindAndReplaceShapeText.cs" >}}
## **Extract Plain Text from the Visio Diagram Page**
Aspose.Diagram API allows developers to extract plain text from the Visio diagram page. They can also iterate through the Visio diagram pages to cover the whole Visio diagram text.

Microsoft Office Visio adds the text to the shapes. The [Shape](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class contains an element called Text, which contains the characters of the text and special elements (cp, pp, tp, and fld) that mark the end of one run and the beginning of the next.
### **Extract Plain Text Programming Sample**
The following piece of code iterates through the shapes of the Visio Page and filter plain text without formatting information.

{{< gist "aspose-diagram" "cce69e51f567ea17ef24bc35fef0f689" "Examples-CSharp-Working-with-Text-GetPlainTextOfVisio-GetPlainTextOfVisio.cs" >}}
