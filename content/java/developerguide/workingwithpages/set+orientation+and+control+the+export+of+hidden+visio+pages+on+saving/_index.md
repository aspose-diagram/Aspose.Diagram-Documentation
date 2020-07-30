---
title : "Set Orientation and Control the Export of Hidden Visio Pages on Saving" 
description : "" 
weight : 12027 
toc : false
type: docs
url: /java/developerguide/workingwithpages/set+orientation+and+control+the+export+of+hidden+visio+pages+on+saving/
---

# Aspose.Diagram for Java : Set Orientation and Control the Export of Hidden Visio Pages on Saving


{{< panel title="Contents Summary" style="primary" >}}
*   1 [Change a Visio Page Layout to Portrait or Landscape](#change-a-visio-page-layout-to-portrait-or-landscape)
    *   1.1 [Set Orientation Programming Sample](#set-orientation-programming-sample)
*   2 [Control the Export of Hidden Visio Pages on Saving](#control-the-export-of-hidden-visio-pages-on-saving)
    *   2.1 [Hide a Page in the Visio Diagram and Set Export Option](#hide-a-page-in-the-visio-diagram-and-set-export-option)
        *   2.1.1 [Set the Export Option for PDF](#set-the-export-option-for-pdf)
        *   2.1.2 [Set the Export Option for HTML](#set-the-export-option-for-html)
        *   2.1.3 [Set the Export Option for Image](#set-the-export-option-for-image)
        *   2.1.4 [Set the Export Option for SVG](#set-the-export-option-for-svg)
{{< /panel >}}
 

 

## Change a Visio Page Layout to Portrait or Landscape

[Aspose.Diagram for Java](https://products.aspose.com/diagram/java) API allows developers to set the orientation of the Visio drawing page programmatically. This help topic explains how to accomplish this task.

Aspose.Diagram for Java API has the [Page](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/Page) class that represents a Visio drawing page. The `PageSheet` property exposed by the `Page` class also exposes the print properties. The `PrintPageOrientation` field of the print properties allows to rotate the page. It offers three options as Portrait, Landscape and same as on the printer. The `PrintPageOrientation` field can be set programmatically using Aspose.Diagram API.

This example work as follows:

1.  Load an existing Visio diagram into the Diagram class object.
2.  Extract a Visio page
3.  Set its orientation as Portrait, Landscape or same as on the printer.
4.  Save the Visio diagram.

### Set Orientation Programming Sample

The code example below shows how to set the orientation of the Visio page.

## Control the Export of Hidden Visio Pages on Saving

[Aspose.Diagram for Java](https://products.aspose.com/diagram/java) API allows developers to include or exclude hidden Visio pages on saving diagram to PDF, HTML, Image (PNG, JPEG, GIF), SVG, and XPS files. Even they may hide Visio pages using Aspose.Diagram API because its option is already available through the cell UIVisibility in the page ShapeSheet.

### Hide a Page in the Visio Diagram and Set Export Option

Aspose.Diagram for Java API has the [Page](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/Page) class that represents a Visio drawing page. The `PageSheet` property exposed by the `Page` class also exposes the page properties. The UIVisibility field of the page properties allows to hide the page. Developers can then use ExportHiddenPage property which is added in the SVGSaveOptions, XPSSaveOptions, ImageSaveOptions, HTMLSaveOptions and PdfSaveOptions classes.

#### Set the Export Option for PDF

The code below shows how to set save options before saving a diagram to PDF format.

#### Set the Export Option for HTML

The code below shows how to set save options before saving a diagram to HTML format.

#### Set the Export Option for Image

The code below shows how to set save options before saving a diagram to image format.

#### Set the Export Option for SVG

The code below shows how to set save options before saving a diagram to SVG format.

