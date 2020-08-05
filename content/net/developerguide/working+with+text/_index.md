---
title : "Working with Text" 
description : "" 
weight : 8041 
toc : false
type: docs
url: /net/developerguide/working+with+text/
---

# Aspose.Diagram for .NET : Working with Text


{{< panel title="Contents Summary" style="primary" >}}
*   1 [Insert a Text Shape in the Visio Page](#insert-a-text-shape-in-the-visio-page)
    *   1.1 [Insert a Text Shape Programming Sample](#insert-a-text-shape-programming-sample)
*   2 [Update Visio Shape Text](#update-visio-shape-text)
    *   2.1 [Update Shape Text Programming Sample](#update-shape-text-programming-sample)
*   3 [Apply Built-in or Custom Stylesheet to a Visio Shape](#apply-built-in-or-custom-stylesheet-to-a-visio-shape)
    *   3.1 [Custom Styles in Microsoft Visio](#custom-styles-in-microsoft-visio)
        *   3.1.1 [Apply Custom Styles Programming Sample](#apply-custom-styles-programming-sample)
*   4 [Apply Different Style on the Each Text Value of a Shape](#apply-different-style-on-the-each-text-value-of-a-shape)
    *   4.1 [Adding Shape Text and Styles](#adding-shape-text-and-styles)
        *   4.1.1 [Adding Text and Styles Programming Sample](#adding-text-and-styles-programming-sample)
*   5 [Find and Replace the Text of a Shape](#find-and-replace-the-text-of-a-shape)
    *   5.1 [Find and Replace Text Programming Sample](#find-and-replace-text-programming-sample)
*   6 [Extract Plain Text from the Visio Diagram Page](#extract-plain-text-from-the-visio-diagram-page)
    *   6.1 [Extract Plain Text Programming Sample](#extract-plain-text-programming-sample)
{{< /panel >}}
 

 

## Insert a Text Shape in the Visio Page

Aspose.Diagram API lets developers to insert a text shape anywhere in the Visio page. To achieve this, the `AddText` method of the [Page](http://www.aspose.com/api/net/diagram/aspose.diagram/page) class takes PinX, PinY, width, height and text parameters.

### Insert a Text Shape Programming Sample

The following piece of code adds a text shape in the Visio diagram.

## Update Visio Shape Text

As well as [creating diagrams](https://docs2.aspose.com/diagram/net/developerguide/ld-sv-cvt/load+or+create+a+visio+drawing), Aspose.Diagram for .NET lets you work with shapes in different ways. This article looks at how to access and update text in shapes. The `Text` property, exposed by the [Shape](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class, supports the `Aspose.Diagram.Text` object. The property can be used to retrieve or update a shape's text. The process for updating a shape's text is straightforward:

1.  Load a diagram.
2.  Find a particular shape.
3.  Set the new text.
4.  Save the diagram.

### Update Shape Text Programming Sample

The following piece of code updates a shape's text. Shapes are identified by their IDs. The code segments below look for a shape called process and with the ID 1 and changes its text.

## Apply Built-in or Custom Stylesheet to a Visio Shape

Microsoft Visio style sheets store formatting information that can be applied to shapes for a consistent look and feel. Aspose.Diagram for .NET allows you to apply style sheets from inside an application.

The `TextStyle`, `FillStyle` and `LineStyle` properties exposed by the [Shape](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class support the [Aspose.Diagram.StyleSheet](http://www.aspose.com/api/net/diagram/aspose.diagram/stylesheet) object. The property can be used to retrieve style information and apply custom text, line and fill styles to a diagram.

### Custom Styles in Microsoft Visio

To apply custom styles to shapes in Microsoft Visio:

1.  Open a diagram in Microsoft Visio.
2.  Select **Define Styles** from the **Format** menu (Visio 2007), or right-click **Styles** in the **Drawing Explorer** window, and select **Define Styles** (Visio 2010).
3.  In the **Define Styles** dialog, type a new name for your custom style sheet. For example, CustomStyle1.
4.  Click the **Text**, **Line** and **Fill** buttons to set text, line and fill styles respectively.
5.  Click **OK**.

After defining custom style sheets in Microsoft Visio, use the following code in a .NET application to apply custom styles to your shapes. Note that the code samples below call the custom style sheet defined above: you need to know the name and location of the sheet you apply. To apply custom styles programmatically:

1.  Load a diagram.
2.  Find the shape you want to apply a style to.
3.  Load the stylesheet.
4.  Apply styles.
5.  Save the diagram.

#### Apply Custom Styles Programming Sample

## Apply Different Style on the Each Text Value of a Shape

As well as [creating diagrams](https://docs2.aspose.com/diagram/net/developerguide/ld-sv-cvt/load+or+create+a+visio+drawing), Aspose.Diagram for .NET lets you work with shapes in different ways. This article helps to add multiple text values to a shape and apply different style on each text value.

The Shape element contains an element called Text, which contains the characters of the text and special elements (cp, pp, tp, and fld) that mark the end of one run and the beginning of the next. Char Element contains the formatting attributes for the shape's text, such as font, color, text style, case, position relative to the baseline, and point size.

### Adding Shape Text and Styles

{{< table style="table-striped" >}}
|Input diagram|
|:----|
|![image](https://docs2.aspose.com/diagram/net/attachments/18350112/18547154.png)|
{{< /table >}}

{{< table style="table-striped" >}}
|Diagram after adding various text values to a shape with different style on each text value|
|:----|
|![image](https://docs2.aspose.com/diagram/net/attachments/18350112/18547155.png)|
{{< /table >}}

#### Adding Text and Styles Programming Sample

The following piece of code add a shape's text and different styles.

## Find and Replace the Text of a Shape

The [Txt](http://www.aspose.com/api/net/diagram/aspose.diagram/txt) Class allows you to edit the shape's text. The Replace method, exposed by the [Txt](http://www.aspose.com/api/net/diagram/aspose.diagram/txt) class, support changing the text of a shape.  
The code examples in this article find and replace the shape's text on the page.

{{< table style="table-striped" >}}
|Input diagram|
|:----|
|![image](https://docs2.aspose.com/diagram/net/attachments/18350112/18547225.png)|
{{< /table >}}

{{< table style="table-striped" >}}
|The diagram after the shape is edited|
|:----|
|![image](https://docs2.aspose.com/diagram/net/attachments/18350112/18547224.png)|
{{< /table >}}

The process for changing the shape's text:

1.  Load a diagram.
2.  Find a particular text of a shape.
3.  Replace text of this shape
4.  Save the diagram.

### Find and Replace Text Programming Sample

The code snippets below show how to modify the shape's text. The code iterate through the shapes of a page.

## Extract Plain Text from the Visio Diagram Page

Aspose.Diagram API allows developers to extract plain text from the Visio diagram page. They can also iterate through the Visio diagram pages to cover the whole Visio diagram text.

Microsoft Office Visio adds the text to the shapes. The [Shape](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class contains an element called Text, which contains the characters of the text and special elements (cp, pp, tp, and fld) that mark the end of one run and the beginning of the next.

### Extract Plain Text Programming Sample

The following piece of code iterates through the shapes of the Visio Page and filter plain text without formatting information.

