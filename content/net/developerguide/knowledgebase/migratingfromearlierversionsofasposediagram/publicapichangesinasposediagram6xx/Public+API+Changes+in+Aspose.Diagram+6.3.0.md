+++
title = "Public API Changes in Aspose.Diagram 6.3.0" 
description = "" 
weight = 20075 
+++

Aspose.Diagram for .NET : Public API Changes in Aspose.Diagram 6.3.0  

# Aspose.Diagram for .NET : Public API Changes in Aspose.Diagram 6.3.0


This document describes changes to the Aspose.Diagram API from version 6.0.0 to 6.3.0, that may be of interest to module/application developers. It includes not only new and updated public methods, but also a description of any changes in the behavior behind the scenes in Aspose.Diagram.

### Detect the Format of a Visio File

##### Various Classes, Methods and Properties are added to detect the format

*   **Add FileFormatUtil and FileFormatInfo Classes**
    *   These classes give programmatic access to detect the Visio file type.
*   **Adds DetectFileFormat Method in FileFormatUtil Class**
    *   It detects and returns the information about the format of a stored Visio diagram in a file.
*   **Adds FileFormatType Property in FileFormatInfo Class**
    *   It gets the detected file format.
*   **Adds LoadFormat Property in FileFormatInfo**
    *   It gets the detected load format.

Developers can easily detect the format of any Visio file. This help topic illustrates how to detect the Visio file format (using a file path or stream) and check its extension: [Detect the Format of Visio File](http://www.aspose.com/docs/display/diagramnet/Introduction#Introduction-DetecttheFormatofVisioFile)

### Control the Export of Hidden Visio Pages on Saving

##### Adds ExportHiddenPage Property in SVGSaveOptions, XPSSaveOptions, ImageSaveOptions, HTMLSaveOptions and PdfSaveOptions Classes

*   It defines whether need to export the hidden Visio pages or not.

Developers may include or exclude hidden Visio pages on saving a Visio diagram to PDF, HTML, Image (PNG, JPEG, GIF), SVG, and XPS files. This help topic illustrates how to do so: [Control the Export of Hidden Visio Pages on Saving](http://www.aspose.com/docs/display/diagramnet/Set+Orientation+and+Control+the+Export+of+Hidden+Visio+Pages+on+Saving#SetOrientationandControltheExportofHiddenVisioPagesonSaving-ControltheExportofHiddenVisioPagesonSaving)

