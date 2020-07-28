+++
title = "Set Orientation and Control the Export of Hidden Visio Pages on Saving" 
description = "" 
weight = 12033 
+++

Aspose.Diagram for .NET : Set Orientation and Control the Export of Hidden Visio Pages on Saving  

# Aspose.Diagram for .NET : Set Orientation and Control the Export of Hidden Visio Pages on Saving


{{< panel title="Contents Summary" style="primary" >}}
*   1 [Change a Visio Page Layout to Portrait or Landscape](#SetOrientationandControltheExportofHiddenVisioPagesonSaving-ChangeaVisioPageLayouttoPortraitorLandscape)
    *   1.1 [Set Orientation Programming Sample](#SetOrientationandControltheExportofHiddenVisioPagesonSaving-SetOrientationProgrammingSample)
*   2 [Control the Export of Hidden Visio Pages on Saving](#SetOrientationandControltheExportofHiddenVisioPagesonSaving-ControltheExportofHiddenVisioPagesonSaving)
    *   2.1 [Hide a Page in the Visio Diagram and Set Export Option](#SetOrientationandControltheExportofHiddenVisioPagesonSaving-HideaPageintheVisioDiagramandSetExportOption)
        *   2.1.1 [Set the Export Option for PDF](#SetOrientationandControltheExportofHiddenVisioPagesonSaving-SettheExportOptionforPDF)
        *   2.1.2 [Set the Export Option for HTML](#SetOrientationandControltheExportofHiddenVisioPagesonSaving-SettheExportOptionforHTML)
        *   2.1.3 [Set the Export Option for Image](#SetOrientationandControltheExportofHiddenVisioPagesonSaving-SettheExportOptionforImage)
        *   2.1.4 [Set the Export Option for SVG](#SetOrientationandControltheExportofHiddenVisioPagesonSaving-SettheExportOptionforSVG)
        *   2.1.5 [Set the Export Option for XPS](#SetOrientationandControltheExportofHiddenVisioPagesonSaving-SettheExportOptionforXPS)
{{< /panel >}}
 

 

## Change a Visio Page Layout to Portrait or Landscape

[Aspose.Diagram for .NET](http://www.aspose.com/.net/diagram-component.aspx) API allows developers to set the orientation of the Visio drawing page programmatically. This help topic explains how to accomplish this task.

Aspose.Diagram for .NET API has the [Page](http://www.aspose.com/api/net/diagram/aspose.diagram/page) class that represents a Visio drawing page. The `PageSheet` property exposed by the `Page` class also exposes the print properties. The `PrintPageOrientation` field of the print properties allows to rotate the page. It offers three options as Portrait, Landscape and same as on the printer. The `PrintPageOrientation` field can be set programmatically using Aspose.Diagram API.

This example work as follows:

1.  Load an existing Visio diagram into the Diagram class object.
2.  Extract a Visio page
3.  Set its orientation as Portrait, Landscape or same as on the printer.
4.  Save the Visio diagram.

### Set Orientation Programming Sample

The code example below shows how to set the orientation of the Visio page.

## Control the Export of Hidden Visio Pages on Saving

[Aspose.Diagram for .NET](http://www.aspose.com/.net/diagram-component.aspx) API allows developers to include or exclude hidden Visio pages on saving diagram to PDF, HTML, Image (PNG, JPEG, GIF), SVG, and XPS files. Even they may hide Visio pages using Aspose.Diagram API because its option is already available through the cell UIVisibility in the page ShapeSheet.

### Hide a Page in the Visio Diagram and Set Export Option

Aspose.Diagram for .NET API has the [Page](http://www.aspose.com/api/net/diagram/aspose.diagram/page) class that represents a Visio drawing page. The `PageSheet` property exposed by the `Page` class also exposes the page properties. The UIVisibility field of the page properties allows to hide the page. Developers can then use ExportHiddenPage property which is added in the SVGSaveOptions, XPSSaveOptions, ImageSaveOptions, HTMLSaveOptions and PdfSaveOptions classes.

#### Set the Export Option for PDF

The code below shows how to set save options before saving a diagram to PDF format.

#### Set the Export Option for HTML

The code below shows how to set save options before saving a diagram to HTML format.

#### Set the Export Option for Image

The code below shows how to set save options before saving a diagram to image format.

#### Set the Export Option for SVG

The code below shows how to set save options before saving a diagram to SVG format.

#### Set the Export Option for XPS

The code below shows how to set save options before saving a diagram to XPS format.

