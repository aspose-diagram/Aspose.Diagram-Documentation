---
title: Introduction
type: docs
weight: 10
url: /net/introduction/
---

## **Get the Version of the Aspose.Diagram for .NET Library**
Microsoft Visio saves information about actions taken on a diagram within the file. For example, the time and date that the document was created, the last time it was edited, printed or saved, is saved with the file. Information about which version of Microsoft Visio created and last edited the file is also saved.

This article explains how to retrieve that information.
### **Determining the Version of Microsoft Visio that's Created, Edited and Saved a Document**
The Version property exposed by the [Diagram](https://apireference.aspose.com/diagram/net/aspose.diagram/diagram/) class and the BuildNumberCreated property exposed by the DocumentProperties class is used to determine the version and full build number of the Microsoft Visio instance used to create the document.

The BuildNumberEdited property exposed by the [DocumentProperties](https://apireference.aspose.com/diagram/net/aspose.diagram/documentproperties) class is used to determine the full build number of the Microsoft Visio instance used to edit the document.

The TimeCreated, TimeEdited, TimePrinted and TimeSaved properties exposed by the DocumentProperties class is used to determine the time that the Microsoft Visio document was created, last edited, last printed and last saved.

You can also set these properties to change the information in the file. The code samples below show how to retrieve information about what created the file as well as when it was created, edited, printed and saved.
#### **Programming Sample**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Introduction-GetLibraryVersion-GetLibraryVersion.cs" >}}
## **Writing Visio Document Summary Information**
Microsoft Visio lets you define a number of document summary information properties to help you and your colleagues identify a diagram. Summary properties, for example, title, subject, author and description, makes the file easier to find when searching, and easier to recognize when browsing files.
### **Writing Microsoft Visio Document Summary Info**
The DocumentProperties class exposes a number of properties to set or get a Microsoft Visio diagram's summary information. Aspose.Diagram for .NET can update the drawing summary information and then write the drawing file back to VDX.

{{% alert color="primary" %}} 

Please note that you cannot set values against the **Application** and **Producer** fields, because Aspose Ltd. and Aspose.Diagram for .NET x.x.x will be displayed against these fields.

{{% /alert %}} 

To update the drawing summary information of an existing VDX or VSD file:

1. Create an instance of the [Diagram](https://apireference.aspose.com/diagram/net/aspose.diagram/diagram/) class.
1. Set properties exposed by [Diagram.DocumentProps](https://apireference.aspose.com/diagram/net/aspose.diagram/diagram/properties/documentprops) to define the summary information for the Visio drawing file.
1. Call the Diagram class' Save method to write the Visio drawing file to VDX.

Check the summary information:

1. Open the output VDX file in Microsoft Visio.
1. Selecting Info from the File menu.
#### **Writing Visio Document Summary Information Programming Sample**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Introduction-SetVisioProperties-SetVisioProperties.cs" >}}
## **Detect the Format of Visio File**
Using Aspose.Diagram for .NET API, developers can detect the format of the Visio file before opening it because the file extension does not guarantee that the file content is appropriate.
### **Detect Format Programming Sample**
The following sample code illustrates how to detect a file format (using the file path or stream) and check its extension.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Introduction-DetectVisioFileFormat-DetectVisioFileFormat.cs" >}}
