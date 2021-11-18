---
title: Public API Changes in Aspose.Diagram 6.3.0
type: docs
weight: 40
url: /java/public-api-changes-in-aspose-diagram-6-3-0/
---

{{% alert color="primary" %}} 

This document describes changes to the Aspose.Diagram API from version 6.0.0 to 6.3.0, that may be of interest to module/application developers. It includes not only new and updated public methods, but also a description of any changes in the behaviour behind the scenes in Aspose.Diagram. 

{{% /alert %}} 
### **Detect the Format of a Visio File**
##### **Various Classes, Methods and Properties are added to detect the format**
- **Add FileFormatUtil and FileFormatInfo Classes** 
  - These classes give programmatic access to detect the Visio file type.
- **Adds detectFileFormat Method in FileFormatUtil Class** 
  - It detects and returns the information about the format of a stored Visio diagram in a file.
- **Adds FileFormatType Property in FileFormatInfo Class** 
  - It gets the detected file format.
- **Adds LoadFormat Property in FileFormatInfo** 
  - It gets the detected load format.

Developers can easily detect the format of any Visio file. This help topic illustrates how to detect the Visio file format (using a file path or stream) and check its extension: [Detect the Format of Visio File](/diagram/java/introduction/#Introduction-DetecttheFormatofVisioFile)
### **Control the Export of Hidden Visio Pages on Saving**
##### **Adds setExportHiddenPage in SVGSaveOptions, XPSSaveOptions, ImageSaveOptions, HTMLSaveOptions and PdfSaveOptions Classes**
- It defines whether need to export the hidden Visio pages or not.

Developers may include or exclude hidden Visio pages on saving a Visio diagram to PDF, HTML, Image (PNG, JPEG, GIF), SVG, and XPS files. This help topic illustrates how to do so: [Control the Export of Hidden Visio Pages on Saving](/diagram/java/set-orientation-and-control-the-export-of-hidden-visio-pages-on-saving/#control-the-export-of-hidden-visio-pages-on-saving)
