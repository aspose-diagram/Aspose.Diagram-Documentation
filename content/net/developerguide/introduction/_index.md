---
title : "Introduction" 
description : "" 
weight : 8013 
toc : false
type: docs
url: /net/developerguide/introduction/
---

# Aspose.Diagram for .NET : Introduction


{{< panel title="Contents Summary" style="primary" >}}
*   1 [Get the Version of the Aspose.Diagram for .NET Library](#get-the-version-of-the-aspose.diagram-for-.net-library)
    *   1.1 [Determining the Version of Microsoft Visio that's Created, Edited and Saved a Document](#determining-the-version-of-microsoft-visio-that's-created,-edited-and-saved-a-document)
        *   1.1.1 [Programming Sample](#programming-sample)
*   2 [Writing Visio Document Summary Information](#writing-visio-document-summary-information)
    *   2.1 [Writing Microsoft Visio Document Summary Info](#writing-microsoft-visio-document-summary-info)
        *   2.1.1 [Writing Visio Document Summary Information Programming Sample](#writing-visio-document-summary-information-programming-sample)
*   3 [Detect the Format of Visio File](#detect-the-format-of-visio-file)
    *   3.1 [Detect Format Programming Sample](#detect-format-programming-sample)
{{< /panel >}}
 

 

## Get the Version of the Aspose.Diagram for .NET Library

Microsoft Visio saves information about actions taken on a diagram within the file. For example, the time and date that the document was created, the last time it was edited, printed or saved, is saved with the file. Information about which version of Microsoft Visio created and last edited the file is also saved.

This article explains how to retrieve that information.

### Determining the Version of Microsoft Visio that's Created, Edited and Saved a Document

The `Version` property exposed by the [Diagram](https://apireference.aspose.com/net/diagram/aspose.diagram/diagram/) class and the `BuildNumberCreated` property exposed by the [`DocumentProperties`](https://apireference.aspose.com/net/diagram/aspose.diagram/documentproperties/) class is used to determine the version and full build number of the Microsoft Visio instance used to create the document.

The `BuildNumberEdited` property exposed by the [`DocumentProperties`](http://www.aspose.com/api/net/diagram/aspose.diagram/documentproperties) class is used to determine the full build number of the Microsoft Visio instance used to edit the document.

The `TimeCreated`, `TimeEdited`, `TimePrinted` and `TimeSaved` properties exposed by the [`DocumentProperties`](http://www.aspose.com/api/net/diagram/aspose.diagram/documentproperties) class is used to determine the time that the Microsoft Visio document was created, last edited, last printed and last saved.

You can also set these properties to change the information in the file. The code samples below show how to retrieve information about what created the file as well as when it was created, edited, printed and saved.

#### Programming Sample

## Writing Visio Document Summary Information

Microsoft Visio lets you define a number of document summary information properties to help you and your colleagues identify a diagram. Summary properties, for example, title, subject, author and description, makes the file easier to find when searching, and easier to recognize when browsing files.

### Writing Microsoft Visio Document Summary Info

The [DocumentProperties](http://www.aspose.com/api/net/diagram/aspose.diagram/documentproperties) class exposes a number of properties to set or get a Microsoft Visio diagram's summary information. Aspose.Diagram for .NET can update the drawing summary information and then write the drawing file back to VDX.

Please note that you cannot set values against the **Application** and **Producer** fields, because Aspose Ltd. and Aspose.Diagram for .NET x.x.x will be displayed against these fields.

To update the drawing summary information of an existing VDX or VSD file:

1.  Create an instance of the [Diagram](https://apireference.aspose.com/net/diagram/aspose.diagram/diagram/) class.
2.  Set properties exposed by [Diagram.DocumentProps](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram/properties/documentprops) to define the summary information for the Visio drawing file.
3.  Call the `Diagram` class' `Save` method to write the Visio drawing file to VDX.

Check the summary information:

1.  Open the output VDX file in Microsoft Visio.
2.  Selecting Info from the File menu.

#### Writing Visio Document Summary Information Programming Sample

## Detect the Format of Visio File

Using Aspose.Diagram for .NET API, developers can detect the format of the Visio file before opening it because the file extension does not guarantee that the file content is appropriate.

### Detect Format Programming Sample

The following sample code illustrates how to detect a file format (using the file path or stream) and check its extension.

## Attachments:

![](https://docs2.aspose.com/diagram/net/images/icons/bullet_blue.gif) [Determining Visio version-001.png](https://docs2.aspose.com/diagram/net/attachments/18350195/18546815.png) (image/png)  
![](https://docs2.aspose.com/diagram/net/images/icons/bullet_blue.gif) [Writing Visio document summary information-001.png](https://docs2.aspose.com/diagram/net/attachments/18350195/18546814.png) (image/png)  
![](https://docs2.aspose.com/diagram/net/images/icons/bullet_blue.gif) [Writing-Visio-document-summary-information.001.png](https://docs2.aspose.com/diagram/net/attachments/18350195/18546817.png) (image/png)  

