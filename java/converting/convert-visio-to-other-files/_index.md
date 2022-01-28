---
title: Convert Visio to other formats 
linktitle: Convert Visio to other formats 
type: docs
weight: 40
url: /java/convert-visio-to-other-files/
description: This topic show you how to Aspose.Diagram allows to convert Visio to SVG,XPS,XML,XAML formats. Convert VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM to SVG,XPS,XML,XAML with a few lines of code.
---

## **Exporting to XML**
This article explains how to export a Microsoft Visio diagram to XML using [Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) API.

- VDX defines an XML diagram.
- VTX defines an XML template.
- VSX defines an XML stencil.

The [Diagram](https://apireference.aspose.com/diagram/java/com.aspose.diagram/Diagram) class' constructors read a diagram and the Save method is used to save, or export, a diagram in a different file format. The code snippets in this article show how to use the Save method to save a Visio file to [VDX](/diagram/java/how-to-convert-a-visio-diagram/), [VTX](/diagram/java/how-to-convert-a-visio-diagram/) and [VSX](/diagram/java/how-to-convert-a-visio-diagram/).

The image below shows the diagram that is exported in the code snippets below. The exported file is shown before each code snippet.

**A Microsoft Visio diagram about to be exported.**

![todo:image_alt_text](http://i.imgur.com/XWajazh.png)
### **Exporting VSD to VDX**
VDX is a schema-based XML file format that lets you save diagrams in a format that products other than Microsoft Visio can read. It's a useful format for transferring diagrams between software applications and retaining editable data.

To export a VSD diagram to VDX:

1. Create an instance of the Diagram class.
1. Call the Diagram class' Save method to write the Visio drawing file to VDX.

**The exported VDX file.**

![todo:image_alt_text](http://i.imgur.com/OJ1jpgh.png)
### **Exporting from VSD to VSX**
VSX is an XML format for defining stencils, the basic objects from which a diagram is built up. When a Visio file is converted to VSX, only the stencils are exported.

To export a VSD diagram to VSX:

- Create an instance of the Diagram class.
- Call the Diagram class' Save method to write the Visio drawing file to VSX.

The image below shows the output VSX file. Note that the stencils used in the diagram, not the diagram itself, are exported.

**The exported VSX file.**

![todo:image_alt_text](http://i.imgur.com/gkZrxCN.png)
### **Export VSD to VTX**
TVX is an XML representation of a template file and stores the settings for the document.

To export a VSD diagram to VTX:

1. Create an instance of the Diagram class.
1. Call the diagram class' Save method to write the Visio drawing file in the VTX format.

The image below shows the output VTX file.

**The output VTX file.**

![todo:image_alt_text](http://i.imgur.com/E6pUvGD.jpg)
### **Exporting to XML Programming Sample**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-ExportToXML-ExportToXML.java" >}}
## **Exporting to XPS**
This article explains how to export a Microsoft Visio diagram to XPS using [Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) API.
Use the [Diagram](https://apireference.aspose.com/diagram/java/com.aspose.diagram/diagram) class' constructor to read the diagram files and the Save method to export the diagram to any supported image format.

The code snippets in this article takes the diagram below as an input. You can use other diagram formats (VSS, VSSX, VSSM, VDX, VST, VSTX, VSTM, VDX, VTX or VSX) as well.

**The source document.**

![todo:image_alt_text](http://i.imgur.com/P3gaA34.png)

To export VSD diagram to XPS:

1. Create an instance of the Diagram class.
1. Call the Diagram class' Save method and set XPS as the output format.

The image below shows the output XPS file.

**The output XPS.**

![todo:image_alt_text](http://i.imgur.com/1ESRxSy.png)
### **Exporting to XPS Programming Sample**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-ExportToXPS-ExportToXPS.java" >}}
## **Exporting a Diagram to SVG**
This article explains how to export a Microsoft Visio diagram to SVG (Scalable Vector Graphics) using [Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) API.

Use the [Diagram](https://apireference.aspose.com/diagram/java/com.aspose.diagram/Diagram) class' constructor to read the diagram files and the Save method to export the diagram to any supported image format.

To export VSD diagram to SVG, perform the following steps:

1. Create an instance of the Diagram class.
1. Call the class' Save method and set SVG as the export format.
### **Exporting Diagram to SVG Programming Sample**
The code samples show how to export a diagram to SVG using Java.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-ExportToSVG-ExportToSVG.java" >}}
## **Exporting a Diagram to XAML**
This article explains how to export a Microsoft Visio diagram to XAML (Extensible Application Markup Language) using [Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) API.

Use the [Diagram](https://apireference.aspose.com/diagram/java/com.aspose.diagram/Diagram) class' constructor to read the diagram files and the Save method to export the diagram to any supported image format.

To export a VSD diagram to XAML:

1. Create an instance of the Diagram class.
1. Call the class' Save method and set XAML as the export format.
### **Exporting to XAML Programming Sample**
The code sample show how to export a diagram to XAML using Java.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-ExportToXAML-ExportToXAML.java" >}}

## **Convert Visio Drawing with Selective Shapes**
Using Aspose.Diagram API, developers can select a group of shapes to convert a Visio drawing into any other supported format. RenderingSaveOptions class offers a Shapes member to maintain the group of shapes. Each save option class is the extended form of RenderingSaveOptions class.

To export a Visio drawing with selective shapes:

1. Create an instance of the Diagram class.
1. Create an instance of any SaveOption class to specify settings as narrated here: [Specify Visio Save Options](https://docs.aspose.com/diagram/java/save-a-visio-drawing-to-pdf-html-and-other-formats/#specifying-visio-save-options)
1. Call save method of the Diagram class object and pass save option class object as parameter.
### **Convert Visio Drawing with Selective Shapes Programming Sample**
The code sample shows how to export a drawing with selective Visio shapes.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-ConvertVisioWithSelectiveShapes.Java" >}}