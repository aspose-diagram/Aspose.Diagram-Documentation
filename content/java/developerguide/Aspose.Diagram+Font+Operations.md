+++
title = "Aspose.Diagram Font Operations" 
description = "" 
weight = 8050 
+++

Aspose.Diagram for Java : Aspose.Diagram Font Operations  

# Aspose.Diagram for Java : Aspose.Diagram Font Operations


{{< panel title="Contents Summary" style="primary" >}}
*   1 [Working with Fonts](#Aspose.DiagramFontOperations-WorkingwithFonts)
    *   1.1 [Where Aspose.Diagram Looks for TrueType Fonts on Windows](#Aspose.DiagramFontOperations-WhereAspose.DiagramLooksforTrueTypeFontsonWindows)
    *   1.2 [How to Explicitly Specify a Font Folder](#Aspose.DiagramFontOperations-HowtoExplicitlySpecifyaFontFolder)
    *   1.3 [Programming Sample](#Aspose.DiagramFontOperations-ProgrammingSample)
*   2 [Receive Notification of Missing Fonts and Font Substitution during Rendering](#Aspose.DiagramFontOperations-ReceiveNotificationofMissingFontsandFontSubstitutionduringRendering)
    *   2.1 [Notification of Missing Fonts and Font Substitution Programming Sample](#Aspose.DiagramFontOperations-NotificationofMissingFontsandFontSubstitutionProgrammingSample)
    *   2.2 [Implementing the IWarningCallback](#Aspose.DiagramFontOperations-ImplementingtheIWarningCallback)
{{< /panel >}}
 

Aspose.Diagram lets developers to set the font directories for rendering in Visio diagrams. This article shows how to utilize fonts from custom directories.

### Working with Fonts

#### Where Aspose.Diagram Looks for TrueType Fonts on Windows

Aspose.Diagram searches for fonts in the **Windows\\Fonts** folder. This default setting works most of the time so only specify your own fonts folders if you really need to.

#### How to Explicitly Specify a Font Folder

Aspose.Diagram APIs has exposed `setFontDirs` method for the [`Diagram`](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/Diagram) class to specify the fonts folders as described below.

1.  The `Diagram.setFontDirs` method takes a string array as a parameter, so developer may specify many font directories using this approach.

When specifying the fonts folder using the above mentioned approach, we recommend setting the font location at the start of the application otherwise you may receive poorly formatted results.

Setting the fonts folder using any of the above methods does not ensure that the Aspose.Diagram API will not look for the fonts on default locations such as system's font folder.

Demonstrates how to set Aspose.Diagram to look in multiple folders for TrueType fonts when rendering or embedding fonts.

#### Programming Sample

The code example below demonstrates how to set Aspose.Diagram to look in multiple folders for TrueType fonts when rendering or embedding fonts.

### Receive Notification of Missing Fonts and Font Substitution during Rendering

Aspose.Diagram API requires access to the accurate font in order to properly render the drawing to PDF format. If the required font is not available on the machine, then Aspose.Diagram API renders any instance of that font using the default font or the closest available font on the machine, since this substitution can change the look of the rendered drawing, developers may need to be notified when a font is missing and with what font it will be replaced.

#### Notification of Missing Fonts and Font Substitution Programming Sample

To be notified of font substitution during rendering:

1.  Create a class that implements the [IWarningCallback](https://apireference.aspose.com/java/diagram/com.aspose.diagram/IWarningCallback)
2.  Pass it to the PdfSaveOptions.setWarningCallback(com.aspose.diagram.IWarningCallback) property.

During saving of the drawing the instance of [IWarningCallback](https://apireference.aspose.com/java/diagram/com.aspose.diagram/IWarningCallback) is called if there are any potential fidelity issues with the drawing. In this case, we choose to only process warnings that are of font substitution and print the warning to the screen. The below example demonstrates how to receive notifications of font substitutions by using [IWarningCallback](https://apireference.aspose.com/java/diagram/com.aspose.diagram/IWarningCallback).

**Java**

{{< code lang="java" >}}
// load the document to render.
Diagram diagram = new Diagram("C:\\temp\\Output.vsdx");


// initialize PdfSaveOptions object
com.aspose.diagram.PdfSaveOptions saveOp = new com.aspose.diagram.PdfSaveOptions();
// create a new class implementing IWarningCallback which collect any warnings produced during drawing save.
HandleDocumentWarnings callback = new HandleDocumentWarnings();
saveOp.setWarningCallback(callback);
 
// pass the save options along with the save path to the save method.
diagram.save("C:\\temp\\Rendering.MissingFontNotification Out.pdf", saveOp);
{{< /code >}}

#### Implementing the IWarningCallback

The last step is to create the class implementing the [IWarningCallback](https://apireference.aspose.com/java/diagram/com.aspose.diagram/IWarningCallback) interface. This class will print out any warnings of font substitution to the console. The below example demonstrates how to implement the IWarningCallback to be notified of any font substitution during document save.

**Java**

{{< code lang="java" >}}
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
{{< /code >}}

## Attachments:

![](https://docs2.aspose.com/diagram/java/images/icons/bullet_blue.gif) [Retrieving Visio page information-001.png](https://docs2.aspose.com/diagram/java/attachments/18612534/18809093.png) (image/png)  

