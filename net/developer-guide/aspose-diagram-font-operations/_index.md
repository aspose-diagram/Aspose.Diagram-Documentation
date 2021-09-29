---
title: Aspose.Diagram Font Operations
type: docs
weight: 180
url: /net/aspose-diagram-font-operations/
---

## **How to Specify TrueType Fonts Location**
Aspose.Diagram lets developers to set the font directories for rendering in Visio diagrams. This article shows how to utilize fonts from custom directories.
### **Working with Fonts**
#### **Where Aspose.Diagram Looks for TrueType Fonts on Windows**
Aspose.Diagram searches for fonts in the **Windows\Fonts** folder. This default setting works most of the time so only specify your own fonts folders if you really need to.
#### **How to Explicitly Specify a Font Folder**
Aspose.Diagram APIs has exposed FontDirs property for the [Diagram](https://apireference.aspose.com/diagram/java/com.aspose.diagram/diagram) class to specify the fonts folders as described below.

1. The Diagram.FontDirs property accepts a string array so developer may specify many font directories using this approach.

{{% alert color="primary" %}} 

When specifying the fonts folder using the above mentioned approach, we recommend setting the font location at the start of the application otherwise you may receive poorly formatted results.

{{% /alert %}} {{% alert color="primary" %}} 

Setting the fonts folder using any of the above methods does not ensure that the Aspose.Diagram API will not look for the fonts on default locations such as system's font folder.

{{% /alert %}} 
#### **Programming Sample**
The code example below demonstrates how to set Aspose.Diagram to look in multiple folders for TrueType fonts when rendering or embedding fonts.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-OS-Fonts-Location-SpecifyFontLocation-SpecifyFontLocation.cs" >}}
### **Receive Notification of Missing Fonts and Font Substitution during Rendering**
Aspose.Diagram API requires access to the accurate font in order to properly render the drawing to PDF format. If the required font is not available on the machine, then Aspose.Diagram API renders any instance of that font using the default font or the closest available font on the machine, since this substitution can change the look of the rendered drawing, developers may need to be notified when a font is missing and with what font it will be replaced.
#### **Notification of Missing Fonts and Font Substitution Programming Sample**
To be notified of font substitution during rendering:

1. Create a class that implements the [IWarningCallback](https://apireference.aspose.com/net/diagram/aspose.diagram/IWarningCallback)
1. Pass it to the PdfSaveOptions.WarningCallback property.

During saving of the drawing the instance of [IWarningCallback](https://apireference.aspose.com/net/diagram/aspose.diagram/IWarningCallback) is called if there are any potential fidelity issues with the drawing. In this case, we choose to only process warnings that are of font substitution and print the warning to the screen. The below example demonstrates how to receive notifications of font substitutions by using [IWarningCallback](https://apireference.aspose.com/net/diagram/aspose.diagram/IWarningCallback).

**C#**

{{< highlight java >}}

 // The path to the documents directory.

string dataDir = RunExamples.GetDataDir_Intro();

// load the document to render.

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// initialize PdfSaveOptions object

PdfSaveOptions saveOp = new PdfSaveOptions();

// create a new class implementing IWarningCallback which collect any warnings produced during drawing save.

HandleDocumentWarnings callback = new HandleDocumentWarnings();

saveOp.WarningCallback = callback;

// pass the save options along with the save path to the save method.

diagram.Save(dataDir + "NotificationofMissingFonts_Out.pdf", saveOp);

{{< /highlight >}}
#### **Implementing the IWarningCallback**
The last step is to create the class implementing the [IWarningCallback](https://apireference.aspose.com/net/diagram/aspose.diagram/IWarningCallback) interface. This class will print out any warnings of font substitution to the console. The below example demonstrates how to implement the IWarningCallback to be notified of any font substitution during document save.

**C#**

{{< highlight java >}}

 class HandleDocumentWarnings : IWarningCallback

{

    /**

    * Our callback only needs to implement the "Warning" method. This method is

    * called whenever there is a potential issue during document processing.

    * The callback can be set to listen for warnings generated during document

    * load and/or document save.

    */

    public void Warning(WarningInfo info)

    {

        // We are only interested in fonts being substituted.

        if (info.WarningType == WarningType.FontSubstitution)

        {

            Console.WriteLine("Font substitution: " + info.Description);

        }

    }

}

{{< /highlight >}}
