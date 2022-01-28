---
title: Convert Visio to Images formats 
linktitle: Convert Visio to Images
type: docs
weight: 20
url: /java/convert-visio-to-image/
description: This topic show you how to Aspose.Diagram allows to convert Visio to various images formats. Convert Visio,VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM to PNG, JPEG, BMP images with a few lines of code.
---

## **Exporting Diagrams to Image File Formats**
This article explains how to export a Microsoft Visio diagram to an image using [Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) API.

Use the [Diagram](https://apireference.aspose.com/diagram/java/com.aspose.diagram/diagram) class' constructor to read the diagram files and the Save method to export the diagram to any supported image format.The image below shows a VSD file about to be saved to PNG format. You can use other diagram formats (VSS, VSSX, VSSM, VDX, VST, VSTX, VSTM, VDX, VTX or VSX) as well.
**The source file. Note that the Arrow and Triangle labels are in bold.**

![todo:image_alt_text](http://i.imgur.com/WOV36ek.png)

To export a diagram to an image:

- Create an instance of the Diagram class.
- Call the Diagram class' Save method and set the image format you want to export to.The output image file looks like the original file.

**The output PNG file.**

![todo:image_alt_text](http://i.imgur.com/WOV36ek.png)
### **Exporting to Image File Programming Sample**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-ExportToImage-ExportToImage.java" >}}

It is also possible to save a particular page to image, instead of the entire document:

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-ExportPageToImage-ExportPageToImage.java" >}}