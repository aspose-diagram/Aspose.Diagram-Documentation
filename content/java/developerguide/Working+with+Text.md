+++
title = "Working with Text" 
description = "" 
weight = 8045 
+++

Aspose.Diagram for Java : Working with Text  

# Aspose.Diagram for Java : Working with Text


{{< panel title="Contents Summary" style="primary" >}}
*   1 [Insert a Text Shape in the Visio Page](#WorkingwithText-InsertaTextShapeintheVisioPage)
    *   1.1 [Insert a Text Shape Programming Sample](#WorkingwithText-InsertaTextShapeProgrammingSample)
*   2 [Update Visio Shape Text](#WorkingwithText-UpdateVisioShapeText)
    *   2.1 [Update Shape Text Programming Sample](#WorkingwithText-UpdateShapeTextProgrammingSample)
*   3 [Apply Built-in or Custom Stylesheet to a Visio Shape](#WorkingwithText-ApplyBuilt-inorCustomStylesheettoaVisioShape)
    *   3.1 [Custom Styles in Microsoft Visio](#WorkingwithText-CustomStylesinMicrosoftVisio)
        *   3.1.1 [Apply Custom Styles Programming Sample](#WorkingwithText-ApplyCustomStylesProgrammingSample)
*   4 [Apply Different Style on the Each Text Value of a Shape](#WorkingwithText-ApplyDifferentStyleontheEachTextValueofaShape)
    *   4.1 [Adding Shape Text and Styles](#WorkingwithText-AddingShapeTextandStyles)
        *   4.1.1 [Adding Text and Styles Programming Sample](#WorkingwithText-AddingTextandStylesProgrammingSample)
*   5 [Find and Replace the Text of a Shape](#WorkingwithText-FindandReplacetheTextofaShape)
    *   5.1 [Find and Replace Text Programming Sample](#WorkingwithText-FindandReplaceTextProgrammingSample)
*   6 [Extract Plain Text from the Visio Diagram Page](#WorkingwithText-ExtractPlainTextfromtheVisioDiagramPage)
    *   6.1 [Extract Plain Text Programming Sample](#WorkingwithText-ExtractPlainTextProgrammingSample)
{{< /panel >}}
 

 

## Insert a Text Shape in the Visio Page

Aspose.Diagram API lets developers to insert a text shape anywhere in the Visio page. To achieve this, the `addText` method of the [Page](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/Page) class takes PinX, PinY, width, height and text parameters.

### Insert a Text Shape Programming Sample

The following piece of code adds a text shape in the Visio diagram.

## Update Visio Shape Text

As well as [creating diagrams](https://docs2.aspose.com/diagram/java/developerguide/loadingsavingandconverting/load+or+create+a+visio+drawing), Aspose.Diagram for Java lets you work with shapes in different ways. This article looks at how to access and update text in shapes.

The `Text` property, exposed by the [Shape](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/shape) class, supports the `Aspose.Diagram.Text` object. The property can be used to retrieve or update a shape's text.

**Input diagram**  
![](http://i.imgur.com/6aEp7h0.png)

**Diagram after the text in the central shape has been changed from Process to New Text**  
![](http://i.imgur.com/o977cxw.png)

The process for updating a shape's text is straightforward:

1.  Load a diagram.
2.  Find a particular shape.
3.  Set the new text.
4.  Save the diagram.

### Update Shape Text Programming Sample

The following piece of code updates a shape's text. Shapes are identified by their IDs. The code segments below look for a shape called process and with the ID 1 and changes its text.

## Apply Built-in or Custom Stylesheet to a Visio Shape

Microsoft Visio style sheets store formatting information that can be applied to shapes for a consistent look and feel. Aspose.Diagram for Java allows you to apply style sheets from inside an application.

The `TextStyle`, `FillStyle` and `LineStyle` properties exposed by the [Shape](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/shape) class support the [Aspose.Diagram.StyleSheet](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/stylesheet) object. The property can be used to retrieve style information and apply custom text, line and fill styles to a diagram.

**Input diagram**  
![](http://i.imgur.com/feV1x2N.png)

**The diagram after applying a custom style sheet that defines text, line and fill styles**  
![](http://i.imgur.com/Xk9W0wN.png)

### Custom Styles in Microsoft Visio

To apply custom styles to shapes in Microsoft Visio:

1.  Open a diagram in Microsoft Visio.
2.  Select **Define Styles** from the **Format** menu (Visio 2007), or right-click **Styles** in the **Drawing Explorer** window, and select **Define Styles** (Visio 2010).
3.  In the **Define Styles** dialog, type a new name for your custom style sheet. For example, CustomStyle1.
4.  Click the **Text**, **Line** and **Fill** buttons to set text, line and fill styles respectively.
5.  Click **OK**.

After defining custom style sheets in Microsoft Visio, use the following code in a Java application to apply custom styles to your shapes. Note that the code samples below call the custom style sheet defined above: you need to know the name and location of the sheet you apply.

To apply custom styles programmatically:

1.  Load a diagram.
2.  Find the shape you want to apply a style to.
3.  Load the stylesheet.
4.  Apply styles.
5.  Save the diagram.

#### Apply Custom Styles Programming Sample

## Apply Different Style on the Each Text Value of a Shape

As well as [creating diagrams](https://docs2.aspose.com/diagram/java/developerguide/loadingsavingandconverting/load+or+create+a+visio+drawing), Aspose.Diagram for Java lets you work with shapes in different ways. This article helps to add multiple text values to a shape and apply different style on each text value.

The Shape element contains an element called Text, which contains the characters of the text and special elements (cp, pp, tp, and fld) that mark the end of one run and the beginning of the next. Char Element contains the formatting attributes for the shape's text, such as font, color, text style, case, position relative to the baseline, and point size.

### Adding Shape Text and Styles

**Input diagram**  
![](http://i.imgur.com/ZqgQPQC.png)

**Diagram after adding various text values to a shape with different style on each text value**  
![](http://i.imgur.com/7UWhFbU.png)

#### Adding Text and Styles Programming Sample

The following piece of code add a shape's text and different styles.

## Find and Replace the Text of a Shape

The [Txt](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/txt) Class allows you to edit the shape's text. The Replace method, exposed by the [Txt](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/txt) class, support changing the text of a shape.  
The code examples in this article find and replace the shape's text on the page.

**Input diagram**  
![](http://i.imgur.com/lW5xaP0.png)  
**The diagram after the shape is edited**  
![](http://i.imgur.com/m33W1Tk.png)

The process for changing the shape's text:

1.  Load a diagram.
2.  Find a particular text of a shape.
3.  Replace text of this shape
4.  Save the diagram.

### Find and Replace Text Programming Sample

The code snippets below show how to modify the shape's text. The code iterate through the shapes of a page.

## Extract Plain Text from the Visio Diagram Page

Aspose.Diagram API allows developers to extract plain text from the Visio diagram page. They can also iterate through the Visio diagram pages to cover the whole Visio diagram text.

Microsoft Office Visio adds the text to the shapes. The [Shape](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/shape) class contains an element called Text, which contains the characters of the text and special elements (cp, pp, tp, and fld) that mark the end of one run and the beginning of the next.

### Extract Plain Text Programming Sample

The following piece of code iterates through the shapes of the Visio Page and filter plain text without formatting information.

## Attachments:

![](https://docs2.aspose.com/diagram/java/images/icons/bullet_blue.gif) [Updating-shape-text.003.png](https://docs2.aspose.com/diagram/java/attachments/18612570/18809017.png) (image/png)  
![](https://docs2.aspose.com/diagram/java/images/icons/bullet_blue.gif) [Updating-shape-text.004.png](https://docs2.aspose.com/diagram/java/attachments/18612570/18809014.png) (image/png)  
![](https://docs2.aspose.com/diagram/java/images/icons/bullet_blue.gif) [Apply Different Style on the Each Text Value of a Shape-01.png](https://docs2.aspose.com/diagram/java/attachments/18612570/18809015.png) (image/png)  
![](https://docs2.aspose.com/diagram/java/images/icons/bullet_blue.gif) [Apply Different Style on the Each Text Value of a Shape-02.png](https://docs2.aspose.com/diagram/java/attachments/18612570/18809012.png) (image/png)  
![](https://docs2.aspose.com/diagram/java/images/icons/bullet_blue.gif) [Find and Replace the Text of a Shape-01.png](https://docs2.aspose.com/diagram/java/attachments/18612570/18809013.png) (image/png)  
![](https://docs2.aspose.com/diagram/java/images/icons/bullet_blue.gif) [Find and Replace the Text of a Shape-02.png](https://docs2.aspose.com/diagram/java/attachments/18612570/18809010.png) (image/png)  
![](https://docs2.aspose.com/diagram/java/images/icons/bullet_blue.gif) [Applying-custom-style-sheets-001.png](https://docs2.aspose.com/diagram/java/attachments/18612570/18809009.png) (image/png)  
![](https://docs2.aspose.com/diagram/java/images/icons/bullet_blue.gif) [Applying-custom-style-sheets-002.png](https://docs2.aspose.com/diagram/java/attachments/18612570/18809006.png) (image/png)  

