---
title: Set Orientation and Control the Export of Hidden Visio Pages on Saving
type: docs
weight: 20
url: /net/set-orientation-and-control-the-export-of-hidden-visio-pages-on-saving/
---

## **Change a Visio Page Layout to Portrait or Landscape**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net) API allows developers to set the orientation of the Visio drawing page programmatically. This help topic explains how to accomplish this task.

Aspose.Diagram for .NET API has the [Page](http://www.aspose.com/api/net/diagram/aspose.diagram/page) class that represents a Visio drawing page. The PageSheet property exposed by the Page class also exposes the print properties. The PrintPageOrientation field of the print properties allows to rotate the page. It offers three options as Portrait, Landscape and same as on the printer. The PrintPageOrientation field can be set programmatically using Aspose.Diagram API.

This example work as follows:

1. Load an existing Visio diagram into the Diagram class object.
1. Extract a Visio page
1. Set its orientation as Portrait, Landscape or same as on the printer.
1. Save the Visio diagram.
### **Set Orientation Programming Sample**
The code example below shows how to set the orientation of the Visio page.

{{< gist "aspose-diagram" "cce69e51f567ea17ef24bc35fef0f689" "Examples-CSharp-Working-with-Pages-SetVisioPageOrientation-SetVisioPageOrientation.cs" >}}
## **Control the Export of Hidden Visio Pages on Saving**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net) API allows developers to include or exclude hidden Visio pages on saving diagram to PDF, HTML, Image (PNG, JPEG, GIF), SVG, and XPS files. Even they may hide Visio pages using Aspose.Diagram API because its option is already available through the cell UIVisibility in the page ShapeSheet.
### **Hide a Page in the Visio Diagram and Set Export Option**
Aspose.Diagram for .NET API has the [Page](http://www.aspose.com/api/net/diagram/aspose.diagram/page) class that represents a Visio drawing page. The PageSheet property exposed by the Page class also exposes the page properties. The UIVisibility field of the page properties allows to hide the page. Developers can then use ExportHiddenPage property which is added in the SVGSaveOptions, XPSSaveOptions, ImageSaveOptions, HTMLSaveOptions and PdfSaveOptions classes.
#### **Set the Export Option for PDF**
The code below shows how to set save options before saving a diagram to PDF format.

{{< gist "aspose-diagram" "cce69e51f567ea17ef24bc35fef0f689" "Examples-CSharp-Working-with-Pages-ExportOfHiddenVisioPagesToPDF-ExportOfHiddenVisioPagesToPDF.cs" >}}
#### **Set the Export Option for HTML**
The code below shows how to set save options before saving a diagram to HTML format.

{{< gist "aspose-com-gists" "9dfca011648b40c82e13a8d894532819" "Examples-CSharp-Working-with-Pages-ExportOfHiddenVisioPagesToHTML-ExportOfHiddenVisioPagesToHTML.cs" >}}
#### **Set the Export Option for Image**
The code below shows how to set save options before saving a diagram to image format.

{{< gist "aspose-com-gists" "9dfca011648b40c82e13a8d894532819" "Examples-CSharp-Working-with-Pages-ExportOfHiddenVisioPagesToImage-ExportOfHiddenVisioPagesToImage.cs" >}}
#### **Set the Export Option for SVG**
The code below shows how to set save options before saving a diagram to SVG format.

{{< gist "aspose-com-gists" "9dfca011648b40c82e13a8d894532819" "Examples-CSharp-Working-with-Pages-ExportOfHiddenVisioPagesToSVG-ExportOfHiddenVisioPagesToSVG.cs" >}}
#### **Set the Export Option for XPS**
The code below shows how to set save options before saving a diagram to XPS format.

{{< gist "aspose-diagram" "cce69e51f567ea17ef24bc35fef0f689" "Examples-CSharp-Working-with-Pages-ExportOfHiddenVisioPagesToXPS-ExportOfHiddenVisioPagesToXPS.cs" >}}
