---
title: Aspose.Diagram Font Operations
type: docs
weight: 170
url: /java/aspose-diagram-font-operations/
---

{{% alert color="primary" %}} 

Aspose.Diagram lets developers to set the font directories for rendering in Visio diagrams. This article shows how to utilize fonts from custom directories.

{{% /alert %}} 
### **Working with Fonts**
#### **Where Aspose.Diagram Looks for TrueType Fonts on Windows**
Aspose.Diagram searches for fonts in the **Windows\Fonts** folder. This default setting works most of the time so only specify your own fonts folders if you really need to.
#### **How to Explicitly Specify a Font Folder**
Aspose.Diagram APIs has exposed setFontDirs method for the [Diagram](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/Diagram) class to specify the fonts folders as described below.

1. The Diagram.setFontDirs method takes a string array as a parameter, so developer may specify many font directories using this approach.

{{% alert color="primary" %}} 

When specifying the fonts folder using the above mentioned approach, we recommend setting the font location at the start of the application otherwise you may receive poorly formatted results.

{{% /alert %}} {{% alert color="primary" %}} 

Setting the fonts folder using any of the above methods does not ensure that the Aspose.Diagram API will not look for the fonts on default locations such as system's font folder.

{{% /alert %}} 

Demonstrates how to set Aspose.Diagram to look in multiple folders for TrueType fonts when rendering or embedding fonts.
#### **Programming Sample**
The code example below demonstrates how to set Aspose.Diagram to look in multiple folders for TrueType fonts when rendering or embedding fonts.

{{< gist "aspose-diagram" "92a05cb833bad6d60de2968c96b40ee4" "Examples-src-main-java-com-aspose-diagram-examples-Fonts-SpecifyFontLocation-SpecifyFontLocation.java" >}}
### **Receive Notification of Missing Fonts and Font Substitution during Rendering**
Aspose.Diagram API requires access to the accurate font in order to properly render the drawing to PDF format. If the required font is not available on the machine, then Aspose.Diagram API renders any instance of that font using the default font or the closest available font on the machine, since this substitution can change the look of the rendered drawing, developers may need to be notified when a font is missing and with what font it will be replaced.
#### **Notification of Missing Fonts and Font Substitution Programming Sample**
To be notified of font substitution during rendering:

1. Create a class that implements the [IWarningCallback](https://apireference.aspose.com/java/diagram/com.aspose.diagram/IWarningCallback)
1. Pass it to the PdfSaveOptions.setWarningCallback(com.aspose.diagram.IWarningCallback) property.

During saving of the drawing the instance of [IWarningCallback](https://apireference.aspose.com/java/diagram/com.aspose.diagram/IWarningCallback) is called if there are any potential fidelity issues with the drawing. In this case, we choose to only process warnings that are of font substitution and print the warning to the screen. The below example demonstrates how to receive notifications of font substitutions by using [IWarningCallback](https://apireference.aspose.com/java/diagram/com.aspose.diagram/IWarningCallback).

**Java**

{{< highlight java >}}

 // load the document to render.

Diagram diagram = new Diagram("C:\\temp\\Output.vsdx");


// initialize PdfSaveOptions object

com.aspose.diagram.PdfSaveOptions saveOp = new com.aspose.diagram.PdfSaveOptions();

// create a new class implementing IWarningCallback which collect any warnings produced during drawing save.

HandleDocumentWarnings callback = new HandleDocumentWarnings();

saveOp.setWarningCallback(callback);



// pass the save options along with the save path to the save method.

diagram.save("C:\\temp\\Rendering.MissingFontNotification Out.pdf", saveOp);

{{< /highlight >}}
#### **Implementing the IWarningCallback**
The last step is to create the class implementing the [IWarningCallback](https://apireference.aspose.com/java/diagram/com.aspose.diagram/IWarningCallback) interface. This class will print out any warnings of font substitution to the console. The below example demonstrates how to implement the IWarningCallback to be notified of any font substitution during document save.



**Java**

{{< highlight java >}}

 public class HandleDocumentWarnings implements IWarningCallback {

     /**

     * Our callback only needs to implement the "Warning" method. This method is

     * called whenever there is a potential issue during document processing.

     * The callback can be set to listen for warnings generated during document

     * load and/or document save.

     */

     public void warning(WarningInfo info) {

         // We are only interested in fonts being substituted.

         if (info.getWarningType() == WarningType.FONT_SUBSTITUTION) {

         System.out.println("Font substitution: " + info.getDescription());

     }

 }

}

{{< /highlight >}}
