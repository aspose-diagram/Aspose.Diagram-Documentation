---
title : "Introduction" 
description : "" 
weight : 8016 
toc : false
type: docs
url: /java/developerguide/introduction/
---

# Aspose.Diagram for Java : Introduction


{{< panel title="Contents Summary" style="primary" >}}
*   1 [Get the Version of the Aspose.Diagram for Java Library](#get-the-version-of-the-aspose.diagram-for-java-library)
    *   1.1 [Determining the Version of Microsoft Visio that's Created, Edited and Saved a Document](#determining-the-version-of-microsoft-visio-that's-created,-edited-and-saved-a-document)
        *   1.1.1 [Programming Sample](#programming-sample)
*   2 [Writing Microsoft Visio Document Summary Info](#writing-microsoft-visio-document-summary-info)
    *   2.1 [Writing Microsoft Visio Document Summary Info](#writing-microsoft-visio-document-summary-info)
        *   2.1.1 [Programming Sample](#programming-sample)
*   3 [Detect the Format of a Visio File](#detect-the-format-of-a-visio-file)
    *   3.1 [Detect Format Programming Sample](#detect-format-programming-sample)
*   4 [Detect the Format of a Visio File from an InputStream](#detect-the-format-of-a-visio-file-from-an-inputstream)
    *   4.1 [Detect Format from an InputStream Programming Sample](#detect-format-from-an-inputstream-programming-sample)
{{< /panel >}}
 

 

Microsoft Visio saves information about actions taken on a diagram within the file. For example, the time and date that the document was created, the last time it was edited, printed or saved, is saved with the file. Information about which version of Microsoft Visio created and last edited the file is also saved.

This article explains how to retrieve that information.

## Get the Version of the Aspose.Diagram for Java Library

The `getVersion()` memthod exposed by the [`Diagram`](https://apireference.aspose.com/java/diagram/com.aspose.diagram/Diagram) class and the `getBuildNumberCreated()` method exposed by the [`DocumentProperties`](https://apireference.aspose.com/java/diagram/com.aspose.diagram/DocumentProperties) class are used to determine the version and full build number of the Microsoft Visio instance used to create the document.

### Determining the Version of Microsoft Visio that's Created, Edited and Saved a Document

The `getBuildNumberEdited()` method exposed by the [`DocumentProperties`](https://apireference.aspose.com/java/diagram/com.aspose.diagram/DocumentProperties) class is used to determine the full build number of the Microsoft Visio instance used to edit the document.

The `getTimeCreated()`, `getTimeEdited()`, `getTimePrinted()` and `getTimeSaved()` methods exposed by the [`DocumentProperties`](https://apireference.aspose.com/java/diagram/com.aspose.diagram/DocumentProperties) class are used to determine the time that the Microsoft Visio document was created, last edited, last printed and last saved.

You can also set these properties to change the information in the file.

The code samples below show how to retrieve information about what created the file as well as when it was created, edited, printed and saved.

**The code output in a console window**  
![](https://docs2.aspose.com/diagram/java/attachments/18612593/18809083.png)

#### Programming Sample

## Writing Microsoft Visio Document Summary Info

Microsoft Visio lets you define a number of document summary information properties to help you and your colleagues identify a diagram. Summary properties, for example title, subject, author and description, makes the file easier to find when searching, and easier to recognize when browsing files.

The [`DocumentProperties`](https://apireference.aspose.com/java/diagram/com.aspose.diagram/DocumentProperties) class exposes a number of properties to set or get a Microsoft Visio diagram's summary information. Aspose.Diagram for Java can update the drawing summary information and then write the drawing file back to VDX.

Please note that you cannot set values against the **Application** and **Producer** fields, because Aspose Ltd. and Aspose.Diagram for Java x.x.x will be displayed against these fields.

### Writing Microsoft Visio Document Summary Info

To update the drawing summary information of an existing VDX or VSD file:

1.  Create an instance of the [`Diagram`](https://apireference.aspose.com/java/diagram/com.aspose.diagram/Diagram) class.
2.  Set properties exposed by `Diagram.getDocumentProps()` method to define the summary information for the Visio drawing file.
3.  Call the `Diagram` class' `save()` method to write the Visio drawing file to VDX.

Check the summary information:

1.  Open the output VDX file in Microsoft Visio.
2.  Selecting **Info** from the **File** menu.

**The Info dialog showing the updated summary information**  
![](https://docs2.aspose.com/diagram/java/attachments/18612593/18809080.png)

#### Programming Sample

## Detect the Format of a Visio File

Using [Aspose.Diagram for Java](https://products.aspose.com/diagram/java) API, developers can detect the format of Visio file before opening it because the file extension does not guarantee that the file content is appropriate.

### Detect Format Programming Sample

The following sample code illustrates how to detect a file format (using the file path or stream) and check its extension.

## Detect the Format of a Visio File from an InputStream

Using Aspose.Diagram for Java API, developers can detect the format of a Visio file by passing an input stream. The `detectFileFormat` method of `FileFormatUtil` class can be used to achieve this.

### Detect Format from an InputStream Programming Sample

The following sample code illustrates how to detect a file format using an input stream.

